pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                checkout scm
            }
        }

        stage('Execute Script') {
            steps {
                bat 'list_files.bat'  // Make sure this points to your batch script
            }
        }
    }
}
