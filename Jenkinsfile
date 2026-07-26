pipeline {
    agent {
        label 'Test-agent'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'hostname'
                sh 'whoami'
                sh 'pwd'
                sh 'echo "Building Test Environment"'
            }
        }
    }
}
