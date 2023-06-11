pipeline {
    agent { docker { image 'maven:3.9.0-eclipse-temurin-11' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
                sh 'mvn clean'
                sh 'mvn package'
            }
        }
    }
    post {
        always {
            archiveArtifacts 'target/*.jar'
        }
    }
}