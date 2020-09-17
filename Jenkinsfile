pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(Maven : 'mvn 3.6.3'){
                        bat "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(Maven : 'mvn 3.6.3'){
                        bat "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(Maven : 'mvn 3.6.3'){
                        bat "mvn deploy"
                }

            }
        }
    }
}
