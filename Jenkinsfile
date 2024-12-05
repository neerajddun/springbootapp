pipeline {

    agent any

    tools {
        maven 'Maven 3.9.4' // Ensure this matches your tool configuration in Jenkins
        jdk 'jdk 17'        // Ensure this matches your tool configuration in Jenkins
    }

    stages {

        stage('Git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/neerajddun/springbootapp.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Unit Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploy"'
            }
        }
    }
}
