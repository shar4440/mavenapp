pipeline{
  agent any

  tools{
    maven 'Maven'
  }

  stages{
    stage('checkout'){
      steps{
        git branch: 'master', url: 'https://github.com/shar4440/mavenapp.git'
      }
    }

    stage('build'){
      steps{
        sh 'mvn clean package'
      }
    }

    stage('test'){
      steps{
        sh 'mvn test'
      }
    }

    stage('run'){
      steps{
        sh 'java -jar target/mavenapp-1.0-SNAPSHOT.jar '
      }
    }
  }

  post{
    success{
      echo 'yesss'
    }
    failure{
      echo 'noooooo'
    }
  }
}
