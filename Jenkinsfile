pipeline {
    agent any
    
    environment {
        PYTHON_HOME = '/usr/bin/python3'  // Adjust path if needed
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from the Git repository
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Install dependencies if necessary (e.g., virtualenv, requirements.txt)
                    // Example: 
                    // sh 'pip install -r requirements.txt' 
                    // For this simple script, no dependencies are needed.
                    echo 'No dependencies for this script.'
                }
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    // Run the Python script
                    echo 'Running hello.py script...'
                    sh "${PYTHON_HOME} hello.py"  // Run the hello.py script
                }
            }
        }

        stage('Post-Build Actions') {
            steps {
                script {
                    // You can add post-build actions like archiving artifacts or notifying
                    echo 'Build complete, running post-build actions...'
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
