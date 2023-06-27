pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               bat "rmdir  /s /q Teamazure1"
                bat "git clone https://github.com/Mahajayanthi/Teamazure1.git"
                bat "mvn clean -f Teamazure1"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Teamazure1"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f Teamazure1"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f Teamazure1"
            }
        }
    }
}
