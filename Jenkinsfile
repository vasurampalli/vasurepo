pipeline {
  
  agent any
    
  tools {nodejs "Nodejs"}
    
  stages {
        
    stage('Code checkout') {
      steps {
        git 'https://github.com/gustavoapolinario/node-todo-frontend'
        sh 'node -v'
        sh 'npm -v'
      }
    }
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
     
    stage('Test') {
      steps {
         sh 'npm test'
      }
    stage('Build') {
      steps {
         sh 'npm build'
      }
    stage('deploy') {
      steps {
         sh 'npm deploy'
      }  
    }      
  }
}
