pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
                echo 'GitHub source code downloaded successfully'
            }
        }

        stage('Build and Test') {
            steps {
                bat 'call "C:\\Program Files\\Apache\\apache-maven-3.9.16\\bin\\mvn.cmd" -B clean package'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline completed successfully!'
        }

        failure {
            echo 'CI Pipeline failed. Check the Console Output.'
        }
    }
}