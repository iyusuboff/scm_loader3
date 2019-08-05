#!/usr/bin/env groovy
pipeline {
    agent {
        label 'jenkins-slave-uc'
    }
    options {
        buildDiscarder(logRotator(numToKeepStr: '10'))
    }
    parameters {
        string(name: 'BUCKET_PATH', defaultValue: 'uckub-distr-unstable2', description: 'GS bucket name with folder')
        string(name: 'RELEASE_NAME', defaultValue: '', description: 'The release name')
        booleanParam(name: 'FULL_DIR', defaultValue: false, description: 'Wheather to create ')
        string(name: 'NFS_SERVER_IP', defaultValue: '', description: 'The shared nfs server api address where the release folder will be placed')

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
