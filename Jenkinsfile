pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Setup .NET SDK') {
            steps {
                bat 'dotnet --version' // For Windows
            }
        }

        stage('Restore Dependencies') {
            steps {
                bat 'dotnet restore' // For Windows
            }
        }

        stage('Build') {
            steps {
                bat 'dotnet build --no-restore' // For Windows
            }
        }

        stage('Run Tests') {
            steps {
                bat 'dotnet test --no-build --verbosity normal' // For Windows
            }
        }
    }

}
