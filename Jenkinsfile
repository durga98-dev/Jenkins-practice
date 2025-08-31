pipeline {
    agent { label 'nodejs-agent1'}  // Define the agent (can be any available node)
    environment{
        PROJECT = 'Expense'
        COMPONENT = 'Backend'
    }
    stages {
        stage('Build') {
            steps {
                // Build the application (for example, a Maven project)
                script {
                    sh """
                        echo "Hello, this is Build"
                        echo "Project is : $PROJECT"
                    """ 
                }
            }
        }

        stage('Test') {
            steps {
                // Run unit tests
                script {
                    sh """
                        echo "Hello, this is Test"
                    """ 
                }
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application (for example, to a staging environment)
                script {
                    sh """
                        echo "Hello, this is Deploy"
                    """ 
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
