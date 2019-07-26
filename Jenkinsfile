pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn deploy'
                }
                
            }
        }
     
    }
    stage ('slack notification') {
               slackSend channel: 'rivet-jenkins', color: 'red', iconEmoji: '', message: 'Welcome to Jenkins slack', teamDomain: 'kaay', tokenCredentialId: 'Jenkins-slack', username: ''  
                }
}
