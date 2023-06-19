pipeline{
  agent any 
  tools {
    maven "maven3.6.0"
  }  
  stages {
    stage('1GetCode'){
      steps{
        sh "echo 'cloning the latest application version' "
        git branch: 'feature', credentialsId: 'gitHubCredentials', url: '<your-git-url-here>'
      }
    }
    stage('3Test+Build'){
      steps{
        sh "echo 'running JUnit-test-cases' "
        sh "echo 'testing must passed to create artifacts ' "
        sh "mvn clean package"
      }
    }
   
}
