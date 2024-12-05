pipeline {

    tools {

        maven ' Maven 3.9.4 '
        jdk ' jdk 17'
    }
    
    stages {

        stage ('Git checkout') {

            steps {

                git branch: 'main', url: 'https://github.com/neerajddun/springbootapp.git'
            }
        }

        stage ('Build') {

            steps {

                sh 'mvn clean package'
            }
        }

        stage ('Unit Test') {

            steps {

                sh 'mvn test'
            }
        }

        stage ('Deploy') {

            steps {

                sh 'echo "Deploy" '
            }
        }
    }

}