pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/uni-zm-codes/maven-samples-A6.git', branch: 'master')
      }
    }

    stage('start bisect - Part E') {
      steps {
        sh 'git bisect start 198644632661c67b6c32f59e9047c11a70685e15 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5'
      }
    }

    stage('run bisect - Part E') {
      steps {
        sh 'git bisect run mvn clean test'
      }
    }

  }
  tools {
    maven 'ZM_MAVEN'
    jdk 'ZM_JDK'
  }
}
