pipeline {
    agent any

    environment {
        NODE_HOME = tool name: 'NodeJS', type: 'NodeJS'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Jayrane03/Devops_Practical'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    sh 'npm test' // Add test scripts if necessary
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh 'npm start' // Replace with your deploy steps
                }
            }
        }
    }

    post {
        success {
            echo 'Deployment Successful!'
        }

        failure {
            echo 'Deployment Failed!'
        }
    }
}
