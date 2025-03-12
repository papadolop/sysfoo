pipeline {
  
  agent any
  
  tools  {
    maven  'Maven 3.9.6'
  }
  
  stages {
    stage("build") {
      steps {
        echo  'Compiling...'
        sh 'mvn compile'
      }
    }
    stage("test") {
      steps {
        echo  'Testing...'
        sh 'mvn clean test'
      }
    }
    stage("package") {
      steps {
        echo  'Packaging...'
        sh 'mvn package -Dskiptests'
      }
    }
  }

  post {
    always {
      echo 'This pipeline is completed...'
    }
  }
  
}
