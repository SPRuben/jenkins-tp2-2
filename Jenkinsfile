pipeline {
    agent any

    environment {
        DOCKER_USER = 'silvapereira.ru@gmail.com'
    }

    stages {
        stage('Login Docker') {
            steps {
                withCredentials([string(credentialsId: 'DOCKER_PASSWORD_RS', variable: 'DOCKER_PASS')]) {
                    sh 'echo $DOCKER_PASSWORD_RS | docker login -u $DOCKER_USER --password-stdin'
                }
            }
        }
    }
}
