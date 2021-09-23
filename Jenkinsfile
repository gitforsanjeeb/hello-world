pipeline {
  agent any
  stages {
    stage("Build and Unit Test") {
      steps {
        echo "building and unit testing the application..."
        sh 'mvn clean package'
      }
    }
    /*stage("test") {
        when {
            expression{
                echo "develop branch code is getting tested"
                BRANCH_NAME == "develop"
            }
        }
        steps {
        echo "testing the application..."
      }
    }*/
    stage("Deploy Application") {
      steps {
        echo "deploying the application..."
      }
    }
  }
  post {
    always {
        echo "pipeline was executed"
    }
    success {
        echo "successful execution"
    }
    failure {
        echo "failed execution"
    }
  }
}
