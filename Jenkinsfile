pipeline {
  agent any
  stages {
    stage("build") {
      steps {
        echo "building the application..."
      }
    }
    stage("test") {
        when {
            expression{
                echo "master branch code is getting tested"
                BRANCH_NAME == "master"
            }
        }
        steps {
        echo "testing the application..."
      }
    }
    stage("deploy") {
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
