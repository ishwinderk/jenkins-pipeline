pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Checkout the code from the version control repository
                checkout scm
                
                // Build the web application (you can use any build tool you prefer)
                // For simplicity, we'll just copy the files to a "dist" folder.
                sh 'mkdir -p dist'
                sh 'cp index.html style.css script.js dist/'
            }
        }
        stage('Test') {
            steps {
                // Run automated tests (for simplicity, we'll just echo a message)
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy the application to a local web server (for example, using Python's SimpleHTTPServer)
                sh 'python -m http.server 8000 --directory dist'
            }
        }
    }
}

