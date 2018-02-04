#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               // git url: 'https://github.com/michaelpombo/demo-2.git'
                checkout scm
                sh 'echo $GIT_AUTHOR_NAME'
                sh 'echo $GIT_BRANCH'
                sh 'echo $GIT_COMMIT'
                sh 'echo $GIT_COMMITTER_EMAIL'
                sh 'echo $GIT_COMMITTER_EMAIL'
                sh 'echo $GIT_COMMITTER_NAME'
                sh 'echo $GIT_URL'
                sh 'gradle' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
            }
        }
    }
}

