pipeline {
   agent any
 
stages {

stage ("clone github") {
   steps {
    git "https://github.com/tarush12/Nodee.git"
}
}

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

stage ("deploy") {
  steps {
    sh 'kubectl apply -f deployment.yaml'
    sh 'kubectl apply -f service.yaml'
}
}
}
}
