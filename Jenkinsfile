pipeline
{
  agent any
  stages
  {
    stage('contdownload')
    {
      steps
      {
         git 'https://github.com/IntelliqDevops/maven.git'
      }
    }
  
   stage('contbuild')
        {
            steps
            {
               sh 'mvn package'
            }
        }
    }
}
