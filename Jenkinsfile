pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/*']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[ url: 'https://github.com/ikatzarski/payroll.git' ]]])
            }
        }

        stage('Build') {
            steps {
                sh "./mvnw package"
            }
        }

        stage('Test') {
            steps {
                sh "./mvnw test"
            }
        }

    }

}
