pipeline {
    agent any

    stages {
        stage('Dotnet Restore') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet restore'
            }
        }

        stage('Dotnet Build') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet build --no-restore'
            }
        }

        stage('Dotnet Test') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet test --no-build'
            }
        }
    }
}