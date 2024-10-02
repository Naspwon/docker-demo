pipeline{
    agent any
    tools{
        nodejs 'node'
    }
    stages{
        stage('Clone repo'){
            steps{
                git(
                    url: "https://github.com/Naspwon/docker-demo.git"
                    branch: "master"
                    )
            }
        }
        stage('Install dependencies'){
            steps{
                sh 'npm install'
            }
        }
        stage('Test'){
            steps{
                sh 'npm test'
            }
        }
        stage('run repo'){
            steps{
                sh 'npm start'
            }
        }
    }
}