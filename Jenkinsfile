pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'python /var/lib/jenkins/workspace/testPython/algorithm.py'
      }
    }

    stage('test') {
      steps {
        sh 'python /var/lib/jenkins/workspace/testPython/hello.py'
      }
    }

    stage('notify') {
      steps {
        mail(subject: 'pipeline result', body: 'test for email', to: 'jiangcw@dfmc.com.cn')
      }
    }

  }
}