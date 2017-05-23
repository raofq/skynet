pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        parallel(
          "build": {
            sh '''#! /bin/sh

echo "build...."

exit 0'''
            
          },
          "build2": {
            sh '''#! /bin/sh

echo "build2 ....."'''
            
          }
        )
      }
    }
    stage('test') {
      steps {
        parallel(
          "test": {
            sh '''#! /bin/sh

echo "test...."

exit 0'''
            
          },
          "test2": {
            sh '''#! /bin/sh

echo "test2 ..."

exit 0'''
            
          }
        )
      }
    }
    stage('deploy') {
      steps {
        sh '''#! /bin/sh

echo "deploy...."

exit 0'''
      }
    }
  }
}