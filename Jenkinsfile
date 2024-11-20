pipeline {
    agent any
    
    tools {
        maven "M398"
    }
    stages {
        stage('Echo version') {
            steps {
                sh 'echo Maven version'
                sh 'mvn --version'
            }
        }
         stage('Build') {
            steps {
                // git branch: 'main', url: 'https://github.com/jenkins-kk-demo/parameterized-pipeline-job-init.git'
                sh 'mvn clean package -DskipTests=true'
            }
        }
         stage('Unit test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
