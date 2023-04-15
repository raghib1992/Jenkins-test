pipeline {

    agent any

    stages {
        stage ('Clean SCM'){
            steps {
                cleanWs()
            }
        }

        stage ('Checkout Source Code') {
            steps {
                script {
                    SourceCodeCheckout this
                }
            }
        }
    }
}
