pipeline {
  agent any
  stages {
    stage('script') {
      parallel {
        stage('script') {
          steps {
            sh 'pwd'
          }
        }

        stage('print message') {
          steps {
            echo 'hi'
          }
        }

      }
    }

    stage('sleep') {
      parallel {
        stage('sleep') {
          steps {
            sleep 5
          }
        }

        stage('copy code from git') {
          steps {
            git(url: 'https://github.com/coolgourav147/spring-boot-war-example.git', branch: 'master')
          }
        }

      }
    }

  }
}