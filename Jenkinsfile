pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''#! /bin/sh

echo "build...."

exit 0'''
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
            
          },
          "test3": {
            echo 'test3 ....'
            
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