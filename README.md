# Shared resources in AWS CICD Pipeline

This repository contains the library resources used in AWS CICD Pipeline. [Jenkins shared library](https://github.com/wso2/aws-cicd-shared-lib.git) contains set of functions are used in [Jenkins pipeline artifacts](https://github.com/wso2/aws-cicd-pipeline.git).


#### Prerequisites  
This library depends on following Jenkins plugins:

* [AnsiColor plugin](https://wiki.jenkins.io/display/JENKINS/AnsiColor+Plugin)
* [Pipeline AWS Plugin](https://wiki.jenkins.io/display/JENKINS/Pipeline+AWS+Plugin)
* [Pipeline Utility Steps Plugin](https://wiki.jenkins.io/display/JENKINS/Pipeline+Utility+Steps+Plugin)


#### Quick Start Guide

 **Step 1**: Configure this repository as a shared library under the name "wso2-jenkins-shared-lib"
 
 **Step 2**: Use the functions under vars folder as below.
```
@Library('wso2-jenkins-shared-lib')

node("master") {
    stage("Example") {
        log.info 'Example info'
        log.err 'Example error'
    }
}
```