node() {
    stage('Download the code from git') 
               {
    git branch: 'dev', url: 'https://github.com/venkat9822891/oct8th-code.git'
               }
    stage('Convert into artifacts') 
               {
    sh 'mvn package'
               }
    stage('Deployment into Container') 
               {
    deploy adapters: [tomcat9(credentialsId: '336853c7-8253-4736-bbcb-a99cd9faf605', path: '', url: 'http://3.109.121.174:8080/')], contextPath: '/jenkindevapp', war: '**/*.war'
               }
}
