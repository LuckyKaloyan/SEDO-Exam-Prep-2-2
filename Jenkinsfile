pipeline {
    agent any

    stages {
        stage('Restore the project') {
            steps {
                bat 'dotnet restore'
            }
        }

        stage('Build the project up') {
            steps {
                bat 'dotnet build'
            }
        }

        stage('Test the project') {
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}