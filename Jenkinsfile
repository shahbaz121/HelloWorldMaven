pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(MVN363 : 'apache-maven-3.6.3'){
                        bat "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(MVN363 : 'apache-maven-3.6.3'){
                        bat "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(MVN363 : 'apache-maven-3.6.3'){
                        bat "mvn deploy"
                }

            }
        }
    }
}
