@Library('java_demo_pipeline@main') _
pipeline {
  agent {label 'slave2'}
   /* parameters {
      string(name:'cmd1',description:'give build the command',defaultValue:'clean')
      string(name:'cmd2',description:'give build the command',defaultValue:'install')
      //string(name:'cmd3',description:'give build the command',defaultValue:'spring-boot')
      //string(name:'cmd4',description:'give build the command',defaultValue:'run')
       // choice(choices:['package','compile','install'],name:'cmd2')
                }*/
    stages {
      stage('checkout') {
        steps {
        //  sh "rm -rf petclicnicnew"
          //sh "git clone https://github.com/Prasadik/petclicnicnew.git"
          //sh "cd petclicnicnew"
          checkoutcode()
              }      
            }
   /*   stage('Set up Environment') {
            steps {
                sh 'export JAVA_HOME=$(dirname $(dirname $(readlink -f $(which java))))'
                sh 'export MAVEN_HOME=/usr/share/maven'
            }
        }*/
        stage('build') {
        steps {
        //  sh "mvn $cmd1 $cmd2"
          buildartifact('install')
              }      
            }
        stage('deploy') {
        steps {
        //  sh "mvn spring-boot:run"
          deploy()
              }      
            }
          }
      }
