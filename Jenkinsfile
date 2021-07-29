node('slaves'){
  
def mavenHome = tool name: "maven3.6.3"    
stage('CheckoutCode'){
git branch: 'development', credentialsId: '09c70004-5a99-44cd-a934-4147152fbb6f', url: 'https://github.com/pavandevops-ec-projects/maven-web-application.git'
}

stage('Build'){
sh "${mavenHome}/bin/mvn clean package"    
}
/*
stage('ExecuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}
stage('UploadArtifactIntoNexus'){
sh "${mavenHome}/bin/mvn deploy"    
}
stage('DeployAppIntoTomcatServer')
{
  sshagent(['e180f594-429f-440e-8723-4dd62e938bcc']) {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@52.66.252.147:/opt/apache-tomcat-9.0.50/webapps"
}  
}
stage('SendEmailNotification')
{
    
    emailext body: '''Build over!...

Regards''', subject: 'build over', to: 'pavankumargurikani@gmail.com'
}
*/
}
