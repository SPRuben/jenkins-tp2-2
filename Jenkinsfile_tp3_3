pipeline {
    agent any

    environment {
        ARTIFACT_NAME = 'app.tar.gz'
    }

    stages {
        stage('Build') {
            steps {
                sh 'echo "Contenu de l\'application" > app.txt'
                sh 'tar -czf ${ARTIFACT_NAME} app.txt'
                archiveArtifacts artifacts: ARTIFACT_NAME, fingerprint: true
            }
        }

        stage('Deploy') {
            steps {
                echo "Déploiement de ${ARTIFACT_NAME}"
            }
        }
    }
}
