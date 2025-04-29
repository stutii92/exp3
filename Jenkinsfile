pipeline {
    agent any

    triggers {
        cron('H/2 * * * *')  // Run every 2 minutes
    }

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/stutii92/exp3.git'
            }
        }

        stage('Build Java Program') {
            steps {
                sh 'javac AddNumbers.java'
            }
        }

        stage('Run Program') {
            steps {
                sh 'java AddNumbers'
            }
        }
    }
}
