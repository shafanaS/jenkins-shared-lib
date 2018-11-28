# Jenkins-shared-lib
This repository is a [Jenkins shared library](https://jenkins.io/doc/book/pipeline/shared-libraries/) which contains set of functions that can be used in a [Jenkins pipeline](https://jenkins.io/doc/book/pipeline/).


#### Prerequisites  
This library depends on following Jenkins plugins:

* [AnsiColor plugin](https://wiki.jenkins.io/display/JENKINS/AnsiColor+Plugin)
* [Pipeline AWS Plugin](https://wiki.jenkins.io/display/JENKINS/Pipeline+AWS+Plugin)
* [Pipeline Utility Steps Plugin](https://wiki.jenkins.io/display/JENKINS/Pipeline+Utility+Steps+Plugin)



#### How to use

1. Configure this repository as a shared library
2. Usage of logging functions 
```
@Library('wso2-jenkins-core')

node("master") {
    stage("Example") {
        log.info 'Example info'
        log.err 'Example error'
    }
}
```