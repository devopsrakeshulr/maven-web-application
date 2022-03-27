node{

def mavenHome = tool name: "maven3.8.5"

//Checkout Stage
stage('CheckoutCode'){
git branch: 'development', credentialsId: '8a4c46c2-4497-41f8-8a73-bfe2967cebcc', url: 'https://github.com/rakesh-devops-janbatch/maven-web-application.git'
}

//Build Stage
stage('Build'){
sh "$mavenHome/bin/mvn clean package"
}
/*
//Generate SonarQube Report
stage('SonarQubeReport'){
sh "$mavenHome/bin/mvn sonar:sonar"
}

//Upload Artifact into Artifactory repo
stage('SonarQubestageUploadArtifactIntoNexus'){
sh "$mavenHome/bin/mvn deploy"
}

//Deploy App into Tomcat Server
stage('DeployAppTomcat'){
sshagent(['ba9b495d-61ad-4cc2-8287-31f7a47da096']) {
   sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.110.185.110:/opt/apache-tomcat-9.0.59/webapps"
}
}
*/
   
}//Node Closing
