#!/usr/bin/env groovy
pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '10'))
    }
    parameters {
        string(name: 'Release Name', defaultValue: '', description: 'The release name')
        string(name: 'NFS Server Ip', defaultValue: '', description: 'The shared nfs server api address where the release folder will be placed')
        booleanParam(name: 'Full Dir', defaultValue: false, description: 'If to create a full dir')
    }
    stages {
        stage("Build archive") {
            steps {
                sh "ls -la "
            }
            post {
                always {
                    sh "ls -la"
                }
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
