pipeline {
    agent any

    environment {
        PATH = "/usr/local/share/dotnet:$PATH"
    }

    stages {
        stage('Restore') { steps { sh 'dotnet restore' } }
        stage('Build')   { steps { sh 'dotnet build --no-restore' } }
        stage('Test')    { steps { sh 'dotnet test --no-build --verbosity normal' } }
        stage('Debug')   { steps { sh 'dotnet --version' } }
    }
}