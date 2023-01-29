pipeline {
    agent any
    stages {
       stage('Checkout') {
            steps {
            checkout scmGit(branches: [[name: '**']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Atifkarim121/project.git']])
            }
       }
         stage('Clone Repository') {
            steps {
            git branch: 'DEV', url: 'https://github.com/Atifkarim121/project.git'
            }
        }
        
        stage('Build and Run Docker Compose') {
            steps {
            sh 'docker compose build'
            sh 'docker compose up -d'
        }   
        }
    }
 }    
