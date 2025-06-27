pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm 
            }
        }
        stage('Restore the project') {
            steps {
                bat 'dotnet restore HouseRentingSystem.sln'
            }
        }

        stage('Build the project up') {
            steps {
                bat 'dotnet build HouseRentingSystem.sln'
            }
        }

        stage('Test the project') {
            steps {
                bat 'dotnet test HouseRentingSystem.sln --no-build --verbosity normal'
            }
        }
    }
}