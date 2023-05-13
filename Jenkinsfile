pipeline {
    agent {
        docker {
            image 'node:lts-bullseye-slim' 
            args '-p 3000:3000' 
            args '--network host'
        }
    }
    stages {
        stage('remove proxy in npm') { 
            steps {
                sh 'npm config rm proxy'
                sh 'npm config rm https-proxy --tried removing npm proxy'
                sh 'npm install' 
            }
        }
    }
}