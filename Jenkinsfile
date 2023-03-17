pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'mvn --version'
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'java -jar /var/lib/jenkins/.m2/repository/io/reflectoring/springboot/actuator/actuator-examples/0.0.1-SNAPSHOT/actuator-examples-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}
