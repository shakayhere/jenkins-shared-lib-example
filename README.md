## Jenkins shared library example 

The code attached to this repository, is a groovy script that can be used as a Jenkins shared library. 

### Functions that this library can do

The following tasks can be performed using tis library:

- <b>dockerLogin:</b> Perform login process with docker private/public repository 
- <b>buildImage:</b> Perform build docker image process
- <b>buildJar:</b> Perform maven package process for Java application
- <b>dockerPush:</b> Start pushing newly build docker image to destination 
