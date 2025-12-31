pipeline {
    agent any

    tools {
        maven 'M3'
    }

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully'
        }
        failure {
            echo 'Build failed'
        }
    }
}
