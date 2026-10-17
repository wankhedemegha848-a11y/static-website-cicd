
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Test Website') {
            steps {
                sh 'test -f index.html'
                sh "grep -q 'Hello, I' index.html"
                echo 'Website file exists and is ready to deploy!'
            }
        }

        stage('Deploy Website') {
            steps {
                sh 'cp index.html /var/www/html/index.html'
                echo 'Website deployed to Nginx successfully!'
            }
        }
    }
}
