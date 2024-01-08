pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Use the credentials for Git checkout
                    checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'git', url: 'https://github.com/QuickpropTechnologies/qptrader.git']]])
                }
            }
        }

        stage('Hello World') {
            steps {
                echo 'Hello, World!'
                // Your additional build steps go here
            }
        }
    }
}

