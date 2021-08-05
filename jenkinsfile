pipeline {
    agent any
    stages {
        stage('Compile stage') {
        
        steps {
           withMaven(maven : 'maven_3_8_1') {
           sh 'mvn clean compile'
           
           }
           
           }
           
        }
    }
}