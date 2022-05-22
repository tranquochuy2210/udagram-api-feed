pipeline {
    agent any
    stages {
        stage('start') {
            steps {
                echo "hello world"
            }
        }
        stage('docker hub') {
            steps {
                withDockerRegistry(credentialsId: 'dockerhub', url: 'https://index.docker.io/v1/') {
                    sh 'docker build -t 225702921/backend_feed .'
                    sh 'docker tag backend_feed 225702921/backend_feed:v1'
                    sh 'docker push 225702921/backend_feed:v1'
                }
            }
        }
    }
}