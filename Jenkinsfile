pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        build 'PES1UG22CS801-1'
        sh 'g++ main/PES1UG22CS801_FILE.cpp -o output'
      }
    }
    stage('Test'){
      steps{
        sh './output'
      }
    }
    stage('Deploy'){
      steps{
        echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
