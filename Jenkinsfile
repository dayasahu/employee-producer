pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                   def mvnHome = tool name: 'maven', type: 'maven'
                   sh "${mvnHome}/bin/mvn package"
                  
               
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_8_1') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_8_1') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}