pipeline {
    agent{
        node{
            label 'AGENT-1'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
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
