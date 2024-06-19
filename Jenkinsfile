pipeline {  
    agent any
    triggers {
    cron('H/2 * * * *')
    }
    stages {

        stage("Parallel"){
            steps{
                parallel{
                    "Taskone" : {echo 'This is task one'},
                        "Tasktwo" : {echo 'This is task two'}
                }
            }
        }
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
            bat 'C:/Jenkinstest.bat'
                }
            }
 
       post {
       failure {mail to: 'neutralor@gmail.com',
       subject: "Pipeline has failed: ${currentBuild.fullDisplayName}",
       body: "Error in ${env.BUILD_URL}"
       }
    }
    }
}
