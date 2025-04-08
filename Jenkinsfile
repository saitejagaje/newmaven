node('slave')  {
    stage('continous download'){
        git 'https://github.com/IntelliqDevops/maven.git'
    }
    stage('continous build'){
        sh 'mvn package'
    }
    stage('continous deploy'){
       deploy adapters: [tomcat9(credentialsId: 'new-credentials1', path: '', url: 'http://172.31.82.28:8080')], contextPath: 'testapp1', war: '**/*.war'
    }
     stage('continous testing'){
        git 'https://github.com/IntelliqDevops/FunctionalTesting.git'
        sh 'java -jar /var/lib/jenkins/workspace/scriptedJango/jango/testing.jar'
           }
}
