pipeline {
    agent any

    tools {
        jdk 'Java-17'
        maven 'maven-3.9.11'
    }

    stages {
        stage('validate-phase') {
            steps {
                sh 'mvn validate'
            }
        }
        stage('compile-phase') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Unit-Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('packaging-application') {
            steps {
                sh 'mvn package'
            }
        }
    }
}