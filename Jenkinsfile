## added slave configuration
node('slave18') {
    stage('Download the code from git') 
               {
    git branch: 'dev', url: 'https://github.com/venkat9822891/oct8th-code.git'
               }
    stage('Convert into artifacts') 
               {
    sh 'mvn package'
               }
    }
