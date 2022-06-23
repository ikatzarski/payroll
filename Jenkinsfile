pipeline {

    agent any

    stages {
        stage('Test') {
            steps {
                sh "./mvnw test"
            }
        }

        stage('Build') {
            steps {
                sh "./mvnw package"
            }
        }

        stage('Find shared files') {
            steps {
                sh "ls -lah target"
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: "target/*.jar"
        }
    }

}
