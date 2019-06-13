pipeline {
    agent { label 'Node1' }
    stages { 
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven-3_3_5') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven-3_3_5') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven-3_3_5') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
