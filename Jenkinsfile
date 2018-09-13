#!groovy
@Library(value='cicd-shared-libraries@master', changelog=false) _
Library(value='cicd-shared-libraries2@master', changelog=false) _



        stage('Build') {
            node {
                sh 'pwd;ls'
                properties([pipelineTriggers([pollSCM('H/2 * * * *')])])
                git poll: true, url: 'git@github.com:sitUboo/Yui.git'

                //checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'SparseCheckoutPaths', sparseCheckoutPaths: [[path: '/app']]]], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'b13463b7-4f76-40e0-9f40-c1669db337a0', url: 'git@github.com:sitUboo/Yui.git']]])
                //checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'b13463b7-4f76-40e0-9f40-c1669db337a0', url: 'git@github.com:sitUboo/Yui.git']]])
                //checkout([$class: 'GitSCM',
                //   branches: [[name: '*/develop']],
                //   doGenerateSubmoduleConfigurations: false,
                //   extensions: [],
                //   submoduleCfg: [],
                //   userRemoteConfigs: [[
                //   credentialsId: '54822290-5f6d-4224-b2b7-038802d5b0a1',
                //   url: 'https://bitbucket.beescloud.com/scm/ce/ce-424.git'
                //]]])
                sh 'pwd;ls;mvn package -f app/pom.xml'
                //archiveArtifacts artifacts: 'app/target/*.jar'
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
