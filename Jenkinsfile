pipeline {
  agent any
  stages {
    stage('Git Checkout') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'This is build'
      }
    }

    stage('Deploy Dev') {
      parallel {
        stage('Deploy Dev') {
          steps {
            echo 'This is deploy to dev'
            sleep 5
            echo 'Success'
          }
        }

        stage('Deploy to Prod') {
          steps {
            echo 'Deploy to prod'
            sleep 10
            echo 'Success'
          }
        }

      }
    }

    stage('Post Actions') {
      steps {
        echo 'Post actions'
      }
    }

  }
}
