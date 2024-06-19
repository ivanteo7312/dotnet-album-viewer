pipeline {   /*declarative */
    agent any
    triggers{
        cron('H/2 * * * *')
    }
    stages {
        stage('Build') {
            steps {
            bat 'C:/Jenkins/test.bat'
                }
            }
        stage('Test') {
            steps {
            bat 'C:/Jenkins/test.bat'
                }
        }
        stage('Package') {
            steps {
            bat 'C:/Jenkins/test.bat'
                }
        }
        stage('Deploy') {
            steps {
            bat 'C:/Jenkins/test.bat'
                }
        }
    } 
}
