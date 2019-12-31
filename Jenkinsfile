node
{
  def mavenHome=tool name: "maven 3.6.3"
stage('CodeCheckout')
{
git credentialsId: '60fdad13-c534-47e7-af04-8527fab64727', url: 'https://github.com/venkataramana-s/my.app.com.git'
}
  stage("Build")
  {
    sh "${mavenHome}/bin/mvn clean package"
  }
  stage('SonarQubeReport')
  {
    sh "${mavenHome}/bin/mvn sonar:sonar"
  }
}
