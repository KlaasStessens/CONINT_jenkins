pipeline {

    agent any 
    
    tools {
        nodejs 'NodeJS'
    }

    environment {

        NPM_TOKEN = credentials('NPM_TOKEN')

    }

    stages {

        stage('Build') {
            steps {
                nodejs('NodeJS') {
                    sh 'npm install'
                }
            }
        }

        stage('Test') {
            steps {
                nodejs('NodeJS') {
                    sh 'npm test'
                }
            }
        }


        stage('Publish') {
            steps {
                nodejs('NodeJS') {
                    sh 'npm publish'
                }
            }
        }
    }


}
