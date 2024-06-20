pipeline {  
    agent {lable 'Linux_Node2'}
    triggers {
    cron('H/2 * * * *')
    }
    stages {
 
        stage("Parallel") {
        steps {
          parallel (
          "Taskone" : { echo 'This is task One'},
          "Tasktwo" : { echo 'This is task two'})
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
            bat 'C:/Jenkins/test.bat'
                }
            }
}
}
