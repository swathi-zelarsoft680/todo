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
                sh '''
           curl -f -v -u admin:momdad007 --upload-file todo.zip http://172.31.9.76:8081/repository/todo/todo.zip
        '''
            }
        }
    }
}