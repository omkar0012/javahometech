node{
  stage('SCM Checkout'){
    git 'https://github.com/omkar0012/javahometech'
  }
  stage('Compile-package'){
    // Get the mvn home path
    def mvnHome = tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
}  
