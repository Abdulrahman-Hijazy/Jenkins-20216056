pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Checkout the source code from the repository
                checkout scm
            }
        }

        stage('Check Workspace') {
            steps {
                // List files in the workspace to confirm that list_files.sh exists
                sh 'ls -l'
            }
        }

        stage('Execute Script') {
            steps {
                // Run the script if it exists and is executable
                script {
                    echo "Running list_files.sh"
                    sh './list_files.sh'  // Ensure that the script is executable
                }
            }
        }
    }

    post {
        // Run cleanup or post actions after the pipeline
        always {
            echo 'Pipeline has completed'
        }
    }
}
