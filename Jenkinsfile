#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               // git url: 'https://github.com/michaelpombo/demo-2.git'
                checkout scm
                sh 'echo XXXX: $GIT_URL'
                sh 'gradle' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
            }
        }
    }
}

