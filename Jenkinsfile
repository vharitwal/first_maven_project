pipeline {
    agent any
    
    stages {
        stage('Preparation') {
            steps {
                git changelog: false, poll: false, url: 'https://gitlab.com/vharitwal/first-maven-java-project.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install -DskipTests'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }   
}
