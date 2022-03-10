pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                echo 'Build Starts!'
                bat "\"C:/Program Files/dotnet/dotnet.exe\" restore \"${workspace}/Test.sln\""
                bat "\"C:/Program Files/dotnet/dotnet.exe\" build \"${workspace}/Test.sln\""
                echo 'Build Ends'
            }
        }
		
		stage('Test') {
            steps {
                echo 'Test Starts!'
                echo 'Test Ends'
            }
        }
		
		stage('Deploy') {
            steps {
                echo 'Deploy Starts!'
                bat "\"C:/Program Files/dotnet/dotnet.exe\" publish \"${workspace}/Test\" --output \"C:/tmp/dotnetweb\""
                echo 'Deploy Ends'
            }
        }		
    }
}