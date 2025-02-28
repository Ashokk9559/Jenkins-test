pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/Ashokk9559/Jenkins-test.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building the project..."
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
            }
        }
    }

    post {
        success {
            echo "Pipeline execution successful!"
            mail to: 'ashokkreddyrp@gmail.com',
                 subject: 'Jenkins Build Successful',
                 body: 'The Jenkins pipeline execution was successful!'
        }
        failure {
            echo "Pipeline execution failed!"
            mail to: 'ashokkreddyrp@gmail.com',
                 subject: 'Jenkins Build Failed',
                 body: 'The Jenkins pipeline execution failed. Please check Jenkins logs.'
        }
    }
}
