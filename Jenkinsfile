pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                   def mvnHome = tool name: 'maven', type: 'maven'
                   sh "${mvnHome}/bin/mvn package"
                  
               
            }
        }

      
    }
}