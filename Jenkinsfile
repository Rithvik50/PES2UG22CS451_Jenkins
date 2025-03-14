pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM', 
                    branches: [[name: '*/main']], 
                    userRemoteConfigs: [[url: 'https://github.com/Rithvik50/PES2UG22CS451_Jenkins.git']]
                ])
            }
        }

        stage('Build') {
            steps {
                sh 'g hello.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            error 'Pipeline failed'
        }
    }
}