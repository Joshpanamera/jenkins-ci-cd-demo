pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-demo .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh '''
                docker rm -f jenkins-demo-container || true
                docker run -d --name jenkins-demo-container -p 80:80 jenkins-demo
                '''
            }
        }

    }
}