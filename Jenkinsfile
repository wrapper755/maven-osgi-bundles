pipeline {
  agent {
    docker {
      image 'gizmotronic/oracle-java8'
      args '-v /root/.m2:/root/.m2 -u root'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'apt-get update; apt-get install -y maven'
        sh 'mvn -s /var/jekins_home/settings.xml clean verify'
      }
    }
  }
}