pipeline {
    agent any
    stages {
        stage('docker hub') {
            steps {
                echo "hello world"
            }
        }
        stage('docker hub') {
            steps {
                withDockerRegistry(credentialsId: 'dockerhub', url: 'https://index.docker.io/v1/') {
                    sh 'docker build -t 225702921/backend_feed'
                    sh 'docker push 225702921/backend_feed'
                }
            }
        }
    }
}