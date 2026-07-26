pipeline {
    agent {
        label 'Test-Agent'   // or use your actual label
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t test-web-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f test-web || true'
                sh 'docker run -d --name test-web -p 8081:80 test-web-app'
            }
        }
    }
}
