node{
stage('SCM Checkout')
{
git 'https://github.com/swarnapplication/JenkinsRepo'
}

stage('Compile-Package'){
 
 
  sh "/usr/share/apache-maven/bin/mvn package"
}
  stage('Deployment'){
    echo "deployment stage"
  
  }
}
