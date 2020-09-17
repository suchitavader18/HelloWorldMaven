pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : 'mvn 3.6.3'){
                        bat "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(maven : 'mvn 3.6.3'){
                        bat "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(maven : 'mvn 3.6.3'){
                        bat "mvn deploy"
                }

            }
        }
    }
}
