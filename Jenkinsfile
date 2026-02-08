pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code checkout completed'
            }
        }

        stage('Build') {
            steps {
                bat 'javac Hello.java'
            }
        }

        stage('Test') {
            steps {
                bat 'java Hello'
            }
        }
        stage('Archive') {
    steps {
        archiveArtifacts artifacts: '*.class', fingerprint: true
    }
}

    }

    post {
        success {
            echo 'Mini CI Project build SUCCESS'
        }
        failure {
            echo 'Mini CI Project build FAILED'
        }
    }
}
