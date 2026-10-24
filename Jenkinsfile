
pipeline {
    agent any

    stages {

        stage('Restore Dependencies') {
            steps {
                sh '/usr/local/share/dotnet/dotnet restore'
            }
        }

        stage('Build Application') {
            steps {
                sh '/usr/local/share/dotnet/dotnet build --configuration Release --no-restore'
            }
        }

        stage('Run All Tests') {
            steps {
                sh '/usr/local/share/dotnet/dotnet test --configuration Release --no-build --verbosity normal'
            }
        }
    }
}
