pipeline {
    agent { 
        node {
            label 'docker-agent-python'
            }
      }

      triggers{
        pollSCM '*/5 * * * *'
        // pull code once in evry five minutes
      }
      
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                echo "Install fire module"
                pip install -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                python3 myapp.py
                python3 myapp.py --name=Raghib
                '''
		echo "Testing Finsh"
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
