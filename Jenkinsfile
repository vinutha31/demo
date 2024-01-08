pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'git', url: 'https://github.com/vinutha31/demo.git']]])
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
