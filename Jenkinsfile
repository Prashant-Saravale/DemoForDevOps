pipeline {
    agent any

    tools {
        maven 'maven'  // This must match the name configured in Jenkins -> Global Tool Configuration
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Prashant-Saravale/DemoForDevOps.git'
            }
        }

        stage('Build') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'mvn clean install'
                    } else {
                        bat 'mvn clean install'
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment step can go here'
            }
        }
    }
}
