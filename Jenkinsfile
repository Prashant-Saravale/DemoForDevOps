pipeline {
    agent any

    tools {
        maven 'maven'  // This must match the name of Maven tool in Jenkins
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Prashant-Saravale/DemoForDevOps.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment step can go here'
            }
        }
    }
}
