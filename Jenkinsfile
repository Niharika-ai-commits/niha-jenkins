pipeline {
    agent{
        label 'Agent'
    }
    options{
        timeout(time: 10, unit: 'Minutes')
        disableConcurrentBuilds() 
    }
    stages {
        stage('Build') { 
            steps {
               script{
                sh 'echo This is Build'
                //sh 'sleep 10'
               }
            }
        }
        stage('Test') { 
            steps {
               script{
                sh 'echo This is Test'
               } 
            }
        }
        stage('Deploy') { 
            steps {
               script{
                sh 'echo This is Deploy'
                // error 'pipeline failed'
               }
            }
        }
    }
    post{
        always{
            echo "This section runs always"
            deleteDir()
        }
        success{
            echo  "this section runs when pipeline is success"
        }
        failure{
            echo "this section runs when pipeline is failure"
        }
    }
}