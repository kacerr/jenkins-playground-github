#!groovy

stage 'checkout & build'

node() {

  checkout scm

  workDir = pwd()
  

  sh 'git rev-parse --abbrev-ref HEAD > BRANCH'
  branch=readFile('BRANCH').toString().replace("\n","")
  sh 'git rev-parse HEAD > GIT_COMMIT'
  git_commit=readFile('GIT_COMMIT').toString().replace("\n","")

  sh 'git status > _GIT_STATUS'
  echo readFile('_GIT_STATUS')

  echo "branch: ${branch}, git commit: ${git_commit}"
  
  echo "Any changes ?"
  echo "another change"
  
  echo "Hohooooo"
  
  
}
