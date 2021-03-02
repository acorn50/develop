pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'python /var/lib/jenkins/workspace/develop_main/algorithm.py'
      }
    }

    stage('test') {
      steps {
        sh 'python /var/lib/jenkins/workspace/testPython/hello.py'
      }
    }

    stage('notify') {
      steps {
        mail(subject: 'build and test result', to: 'jiangcw@dfmc.com.cn', body: '{SCRIPT}')
      }
    }

  }
}