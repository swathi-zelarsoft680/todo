@Library('todoshop') _

pipeline{

    agent any

    stages {

        stage('Download Dependencies') {
            steps {
                sh '''
                npm install
            '''
            }
        }
        stage('prepare Artifacts') {
            steps {
                sh '''
                zip -r todo.zip *
            '''
            }

        }
        stage('upload Artifacts') {
            steps {
                script {
                    nexus
                }
           
        
            }
        }
    }
}