pipeline {
    agent {
        docker {
            image 'node:lts-bullseye-slim' 
            args '-p 3000:3000' 
            args '--network host'
        }
    }
    stages {
        stage('install npm') { 
            steps {
                sh 'npm cache clean –force'
                sh 'npm install' 
            }
        }
    }
}