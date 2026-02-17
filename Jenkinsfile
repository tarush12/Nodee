pipeline {
   agent any
 
stages {
   
stage ("build image") {
  steps {
    sh 'docker build -t tarush79/nodee:latest .'
}
}

stage ("docker login") {
  steps {
     sh 'docker login -u tarush79 -p tarush123'
}
}

stage ("push docker hub") {
  steps {
     sh 'docker push tarush79/nodee:latest'
}
}
}
}
