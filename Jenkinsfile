pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Replace with your real working GitHub Username and Repository Name
                git branch: 'main', url: 'https://github.com<your-username>/Student-Management-System.git'
            }
        }
        
        stage('Generate Report') {
            steps {
                // Runs the python program to generate the text file on a Windows agent
                bat 'python app.py'
            }
        }
        
        stage('Archive Report') {
            steps {
                // Captures and stores the generated file inside the Jenkins UI
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
