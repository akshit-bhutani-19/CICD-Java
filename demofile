pipeline {
    agent any
    stages {
        stage('Checkout') {          
            steps {
                git branch: "master", url: "https://github.com/hkshitesh/SL-MAVEN-8-FEB-BACTH.git"
            }
        }
        stage('Build') {
            steps {
                // Use Maven to build your project
                bat 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                // Run tests if applicable
                // bat 'mvn test'
            }
        }
    }
    post {
     success {
     // This block will be executed if the pipeline runs successfully
     echo 'Pipeline executed successfully!'
     }
     failure {
     // This block will be executed if the pipeline fails
     echo 'Pipeline failed!'
     }
     } 
} 
