pipeline {
    agent any 

    tools {
        nodejs "nodejs-18"
    }

    trigger{
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
    }
}