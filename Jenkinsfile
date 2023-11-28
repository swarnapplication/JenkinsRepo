node{
stage('SCM Checkout')
{
git 'https://github.com/swarnjava/awsgitrepo'
}

stage('Compile-Package'){
  def mvnHome = tool name: 'MAVEN 3.5.2', type: 'maven'
 
  sh "/usr/share/apache-maven/bin/mvn package"
}
  stage('Deployment'){
    echo "deployment stage"
  
  }
}
