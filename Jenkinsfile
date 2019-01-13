pipeline {
  agent any
  stages {
    stage('build1') {
      parallel {
        stage('build1') {
          steps {
            echo 'build1'
            archiveArtifacts(artifacts: 'build', allowEmptyArchive: true, onlyIfSuccessful: true)
          }
        }
        stage('build2') {
          steps {
            echo 'build2'
            addGitLabMRComment(comment: 'build2')
          }
        }
      }
    }
    stage('build3') {
      steps {
        echo 'build3'
      }
    }
  }
}