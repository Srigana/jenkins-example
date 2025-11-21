pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                withMaven(maven: 'Maven') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage('Test') {
            steps {
                withMaven(maven: 'Maven') {
                    sh 'mvn test'
                }
            }
        }

        stage('Package / Install') {
            steps {
                withMaven(maven: 'Maven') {
                    sh 'mvn clean install'    // or 'mvn package'
                }
            }
        }
    }
}
