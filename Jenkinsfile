pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                stage ('Print') {
            steps {
                echo "Hello Devops Engineers"
            }
                checkout scm
        }
    }

        stage('Build') {
            steps {
                // Build the application using Maven
                echo 'Building the application'
                sh 'mvn clean install'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application to a server
                echo 'Deploying the application'
                
                // Example: Copy the built JAR file to a server
                sh 'scp target/your-app.jar user@your-server:/path/to/deployment/'

                // Additional deployment steps as needed
            }
        }
    }

    post {
        success {
            echo 'Build and deployment succeeded!'
        }
        failure {
            echo 'Build or deployment failed. Take necessary actions.'
        }
    }
}
}
