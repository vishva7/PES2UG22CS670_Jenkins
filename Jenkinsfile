pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ working.cp -o output'
                build 'PES2UG22CS670'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}