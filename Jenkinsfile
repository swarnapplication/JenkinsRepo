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
  sh "aws s3 cp /var/lib/jenkins/workspace/SpringBootApplication-Jenkins-Job/target/SpringBootDBAppTest-0.0.1-SNAPSHOT.jar s3://swarn-repo-bucket/"
   sh "wget https://swarn-repo-bucket.s3.ap-south-1.amazonaws.com/SpringBootDBAppTest-0.0.1-SNAPSHOT.jar"
   sh "java -jar SpringBootDBAppTest-0.0.1-SNAPSHOT.jar"
  }
}
