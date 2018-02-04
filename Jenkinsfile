#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               // git url: 'https://github.com/michaelpombo/demo-2.git'
                sh 'echo branch: $GIT_BRANCH, commit: $GIT_COMMIT; url: $GIT_URL'
                sh 'gradle' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
            }
        }
    }
}

