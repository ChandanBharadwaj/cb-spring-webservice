pipeline{
  agent any
  tools {
        maven 'maven_3.6.0' 
    }
  stages {
    stage('Compile Stage') {
        steps{
             maven(maven : 'maven_3.6.0'){
                 bat 'mvn clean compile'
            }
        }
    }
     stage('Testing Stage') {
        steps{
             maven(maven : 'maven_3.6.0'){
                 bat 'mvn test'
            }
        }
    }
     stage('Deployment Stage') {
        steps{
             maven(maven : 'maven_3.6.0'){
                 bat 'mvn deploy'
            }
        }
    }
  }
}
