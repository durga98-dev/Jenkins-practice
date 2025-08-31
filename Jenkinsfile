pipeline {
    agent any  // Define the agent (can be any available node)

    stages {
        stage('Build') {
            steps {
                // Build the application (for example, a Maven project)
                script {
                    sh 'mvn clean install'  // Replace with your build tool
                }
            }
        }

        stage('Test') {
            steps {
                // Run unit tests
                script {
                    sh 'mvn test'  // Replace with your test command
                }
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application (for example, to a staging environment)
                script {
                    sh './deploy.sh'  // Replace with your deployment script/command
                }
            }
        }
    }

    post {
        always {
            // Clean up or notify team
            echo 'Pipeline complete'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
