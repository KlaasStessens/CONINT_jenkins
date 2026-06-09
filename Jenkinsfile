pipeline {

    agent any 
    
    tools {
        nodejs 'NodeJS'
    }

    environment {

        NPM_TOKEN = credentials('NPM_TOKEN')
        PATH = "${tool 'NodeJS'}/bin:${env.PATH}"
    }

    stages {

        stage('Build') {
            steps {
                sh 'node --version'
                sh 'npm install'

            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }


        stage('Publish') {
            steps {
                sh 'npm publish'
            }
        }
    }


}
