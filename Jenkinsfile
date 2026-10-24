
pipeline {
    agent any

    stages {

        stage('Restore Dependencies') {
            steps {
                sh 'dotnet restore'
            }
        }

        stage('Build Application') {
            steps {
                sh 'dotnet build --configuration Release --no-restore'
            }
        }

        stage('Run All Tests') {
            steps {
                sh 'dotnet test --configuration Release --no-build --verbosity normal'
            }
        }
    }
}
