pipeline {
    agent{
        node{
            label 'AGENT-1'
        }
    }
        environment   { 
           GREETING = 'HELLO JENKINS'
        }
             options  {
        timeout(time: 1, unit: 'HOURS') 
        }
    stages {
        stage('Build') {
            steps {
                echo 'Building the application'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the application'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application'
                echo "$GREETING"
            }
        }
    }
    //post build
        post { 
        always { 
            echo 'I will always say Hello again!'
        }
         failure { 
            echo 'the agent is failed ra'
        }
        success{
            echo'the pipeline is success'
        }
    }

}
