node() {
    stage('Download the code from git') 
               {
    git branch: 'test', url: 'https://github.com/venkat9822891/oct8th-code.git'
               }
    stage('Convert into artifacts') 
               {
    sh 'mvn package'
               }
    stage('Deployment into Container') 
               {
    deploy adapters: [tomcat9(credentialsId: '2a53241c-d402-4598-9b53-8637877f6767', path: '', url: 'http://43.204.96.158:8080')], contextPath: '/jenkinstestapp', war: '**/*.war'
               }
}
