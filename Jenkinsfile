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
        emailext(body: '{$SCRIPT}', subject: 'build result', to: 'jiangcw@dfmc.com.cn', mimeType: 'text/html', attachLog: true, compressLog: true)
      }
    }

  }
}