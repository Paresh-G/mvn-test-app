pipeline {
    agent {
        label 'mvn-package'
    }

    tools {
        maven 'maven-3.9.11'
        jdk 'Java-17'
    }

    stages {
        stage('Job-details') {
            steps {
                echo "My build number is : ${env.BUILD_NUMBER}" // Jenkin Inbuild env varibales
                echo "My build name is ${env.BUILD_NAME}"
                echo "My build URL is ${env.BUILD_URL}"
                echo "My node name is ${env.NODE_NAME}"
                echo "My workspace is ${env.WORKSPACE}"
                echo "My build ID is ${env.BUILD_ID}"
                echo "My build dispaly name is ${env.BUILD_DISPLAY_NAME}"
                echo "My job name is ${env.JOB_NAME}"
                echo "My job url is ${env.JOB_URL}"
            }
        }
        stage('validating-application') {
            steps {
                sh 'mvn validate'
            }
        }
        stage('compiling-application') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Testing-application') {
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