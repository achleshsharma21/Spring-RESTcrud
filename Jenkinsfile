pipeline {
    agent any
    tools {
        jdk "jdk1.8.0_221"
        maven "MAVEN_HOME"
    }
    stages {
        stage('git repo & clean') {
            steps {
            	bat "mvn clean"
            }
        }
        stage('install') {
            steps {
                bat "mvn install"
            }
        }
        stage('test') {
            steps {
                bat "mvn test"
            }
        }
        stage('package') {
            steps {
                bat "mvn package"
            }
        }
    }
}