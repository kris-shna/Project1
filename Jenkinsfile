pipeline {
    agent any
    
    parameters {
        choice(name: 'MODULE', choices: ['Student-Portal', 'Grading-System', 'Attendance-Tracker'], description: 'Select the system module to build')
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Clones the repository codebase into the Jenkins workspace
                git branch: 'main', url: 'https://github.com/<your-student-username>/Student-Management-System.git'
            }
        }
        
        stage('Show Parameter') {
            steps {
                // Echoes back the chosen module input at build time
                echo "Selected Module: ${params.MODULE}"
            }
        }
        
        stage('Build for Module') {
            steps {
                // Simulates building binaries or launching verification checks for the chosen application subsystem
                echo "Building application configurations for the ${params.MODULE} module..."
            }
        }
    }
}
