stage('Build') {
   node {
        sh 'pwd;ls'
        properties([pipelineTriggers([pollSCM('H * * * *')])])
        git url: 'git@github.com:sitUboo/basicpipeline.git'
        sh 'pwd;ls;pwd'
   }
}          
        //stage('Test') {
        //    agent {
        //        label 'linux'
        //    }
        //    steps {
        //        git credentialsId: 'b13463b7-4f76-40e0-9f40-c1669db337a0', url: 'git@github.com:buildit/jenkins-pipeline-examples.git'
        //    }
       // }
    //}
//}
