pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS451-1'
                sh 'g++ hello.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './shoutput'
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
