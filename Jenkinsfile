<<<<<<< HEAD
=======
pipeline{
    agent{
        label "nodejs"
    }
    stages{
        stage("Install dependencies"){
            steps{
                sh "npm ci"
            }
        }

        stage("Check Style"){
            steps{
                sh "npm run lint"
            }
        }

        stage("Test"){
            steps{
                sh "npm test"
            }
        }

        stage('Deploy') {

             steps {

                  sh '''

                   oc project sefrig-greetings

                    oc start-build greeting-service --follow --wait

                     '''

             }
        }
    }
}
>>>>>>> f6feba16f27849fa8311457c829bb78f971a88b3
