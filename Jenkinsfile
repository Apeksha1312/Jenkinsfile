pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the GitHub repository
                git 'https://github.com/yourusername/your-repo.git'
            }
        }

        stage('Deploy to XAMPP') {
            steps {
                // Copy the HTML files to XAMPP htdocs directory
                bat 'xcopy /s /y .\\*.html C:\\xampp\\htdocs'
            }
        }

        stage('Post-deployment Test') {
            steps {
                // Optional: Add tests to validate the deployment
                // For example, you can use curl to test if the files are accessible
                bat 'curl http://localhost/index.html'
            }
        }
    }
}

