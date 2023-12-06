pipeline {

    agent any

    stages {

        stage('Echoing') {

            steps {
                sh '''
                pwd
                echo "Hi there"
                echo "Groovy Baby"
                echo "Inside Shell block"
                '''

                //This is a Groovy Comment

            }

        }

        stage('Run Script') {
            //This runs a script
            steps {
                sh'''
                #you need to use the language comments in the language
                sh ./run.sh
                '''
            }

        }

        post {
            always {
                archiveartifacts '*.zip'
            }

        }

    }

}