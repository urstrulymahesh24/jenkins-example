pipeline {
    agent any

    stages {
       
    stage ('slack notification') {
               slackSend channel: 'rivet-jenkins', 
                   color: 'red', iconEmoji: '', 
                   message: 'Welcome to Jenkins slack', 
                   teamDomain: 'kaay', 
                   tokenCredentialId: 'Jenkins-slack', 
                   username: ''  
    }
    } 
}
