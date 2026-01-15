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
        parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
                echo 'hello darling'
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
