pipeline {
    agent any
    stage('init') {
      checkout scm
   }
    stages { 
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'MAVEN_HOME') {
                    sh 'mvn compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'MAVEN_HOME') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'MAVEN_HOME') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
