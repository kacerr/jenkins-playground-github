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
  
  echo "branch: ${env.BRANCH}"
  echo "branch_name: ${env.BRANCH_NAME}"
  
  echo "still on it"
  echo "still on it ..."
  echo "still on it ..."

  echo "This is here to see how it looks on github when jenkins has been called"
  sh 'for i in `seq 60`; do sleep 1; echo $i; done > _OUTPUT'
  echo readFile('_OUTPUT')

  
}
