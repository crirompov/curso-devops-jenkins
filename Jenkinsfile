pipeline {
    agent any 

    environment {
        FLY_API_TOKEN=credentials('FLY_API_TOKEN_TEST')
    }

    tools {
        nodejs "nodejs-18"
    }

    triggers{
        githubPush()
    }
    
    stages {
        stage('Install dependencies'){
            steps {
                echo 'Installing...'
                sh 'npm install'
            }
        }
        stage('Run test'){
            steps{
                echo 'Running test'
                sh 'npm run test'
            }
        }
        stage('Pintar credencial'){
            steps{
                echo 'Hola esta es mi credencial: $FLY_API_TOKEN'
            }
        }
    }
}