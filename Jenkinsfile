pipeline {
    agent any
    
    environment {
        APP_NAME = 'StudentPerformanceSystem'
        APP_VERSION = '1.0.0'
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Change this to your exact GitHub profile path
                git branch: 'main', url: 'https://github.com<your-username>/Student-Management-System.git'
            }
        }
        
        stage('Show App Info') {
            steps {
                // Reads custom environment variables using the env namespace
                echo "Building ${env.APP_NAME}, version ${env.APP_VERSION}"
            }
        }
        
        stage('Build') {
            steps {
                // Compiles the python code to check for syntax bugs before deployment
                bat 'python -m py_compile app.py'
                echo "${env.APP_NAME} version ${env.APP_VERSION} compiled successfully."
            }
        }
    }
}
