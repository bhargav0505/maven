node ('slave')
{
    stage ('cd')
    {
        git 'https://github.com/rushi222/maven.git'
    }
    stage ('build')
    {
        sh label: '', script: 'mvn package'
    }
    stage ('deploy')
    {
        sh label: '', script: 'scp /var/lib/jenkins/workspace/rushi/webapp/target/webapp.war ubuntu@172.31.87.102:/var/lib/tomcat8/webapps/ravi.war'
    }
}
