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
