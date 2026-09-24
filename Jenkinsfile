pipeline {
    agent any

    stages {
        
        stage('Checkout') {
            steps {
                echo "Code checked out successfully."
            }
        }

        stage('Build') {
            steps {
                echo "Compiling application..."
                
                bat 'python -m py_compile app.py'
                
                echo "Simulating a 20-second compile wait time..."
                sleep 20
                
                
                milestone(1)
            }
        }

        stage('Deploy') {
            steps {
                
                milestone(2)
                
                echo "Deploying application code securely to the server..."
            }
        }
    }
}
