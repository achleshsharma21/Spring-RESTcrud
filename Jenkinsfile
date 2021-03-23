pipeline {
    agent any
    tools {
        jdk "jdk1.8.0_221"
        maven "MAVEN_HOME"
    }
    stages {
        stage('git repo & clean') {
            steps {
            	bat "mvn clean -f Spring-RESTcrud"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Spring-RESTcrud"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f Spring-RESTcrud"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f Spring-RESTcrud"
            }
        }
    }
}