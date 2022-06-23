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

    }

}
