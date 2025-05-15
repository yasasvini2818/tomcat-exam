pipeline{
agent any
 tools{
   maven 'Maven'
   jdk 'JDK'
   }
   stages{
     stage('Checkout)
     {
       steps{
         git branch:'master',url:'https://github.com/yasasvini2818/tomcat-exam.git'
       }
      }
     stage('Build WAR')
     {
       steps{
         sh 'mvn clean package'
        }
       }
       stage('Deploy WAR')
       {
         steps
         {
           sh 'cp target/MavenWebApp-1.0-SNAPSHOT.war /opt/tomcat/webapps/'
          }
       }
     }
    }
