pipeline {
    agent any

    stages {
        stage('buils') {
            steps {
                sh 'docker build -t Durgaedev/service:v1 .'
            }
        }
        stage('push') {
            script {
                withDockerRegistry(credentialsId: 'docker-cred') {
                    sh 'docker push Durgaedev/service:v1'
                }
            }
        }
    }
}
