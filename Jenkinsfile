pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Compiling the CPP file'
                    sh 'g++ -o output PES21CS593.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'The output of the CPP file is: '
                    sh './output'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deployment steps'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
