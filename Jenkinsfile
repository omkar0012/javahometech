node{
  stage('SCM Checkout'){
    git 'https://github.com/omkar0012/javahometech'
  }
  stage('Compile-package'){
    // Get the mvn home path
    def mvnHome = tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  stage('Email Notification'){
    mail bcc: '', body: 'Hiii welcome to jenkins email alert', cc: '', from: '', replyTo: '', subject: 'Jenkins job', to: 'bhadsalkaromkar@gmail.com'
  }
  stage('Slack Notification'){
    slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#jenkins-pipeline-demo', color: 'good', message: 'welcome to jenkins slack', tokenCredentialId: 'slackdemo'
  }
}  
