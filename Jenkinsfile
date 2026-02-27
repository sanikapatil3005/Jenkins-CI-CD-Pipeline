pipeline {
    agent any

    stages {

        stage('Git Checkout') {
            steps {
                git 'https://github.com/sanikapatil3005/myweb.git'
            }
        }

        stage('Maven Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t sanikapatil30/myimage:$BUILD_NUMBER .'
            }
        }

        stage('Docker Push') {
            steps {
                sh 'docker push sanikapatil30/myimage:$BUILD_NUMBER'
            }
        }

        stage('Update deployment file') {
            steps {
                sh "sed -i 's|image:.*|image: sanikapatil30/myimage:$BUILD_NUMBER|g' deployments.yml"
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f deployments.yml'
            }
        }
    }
}
