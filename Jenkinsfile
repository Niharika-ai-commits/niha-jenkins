pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
               script{
                sh 'echo This is Build'
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
               }
            }
        }
    }
    post{
        always{
            echo "This section runs always"
        }
        success{
            echo  "this section runs when pipeline is success"
        }
        failure{
            echo "this section runs when pipeline is failure"
        }
    }
}