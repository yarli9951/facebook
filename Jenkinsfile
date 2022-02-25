
pipeline {

  agent any

    parameters {
              string(name: 'Version',
              defaultValue: 'facebook-2.0',
              description: 'Facebook project')
           }

     stages{
                     stage('Checkout'){
                                steps
                                {

                                     checkout([$class: 'GitSCM', branches: [[name: '*/facebook-2.0']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/yarli9951/facebook.git']]])
                                  }

                     stage('Build'){
                       steps{
                         script{
                           sh 'mvn -f /var/lib/jenkins/workspace/Maven-Pipeline/pom.xml install'
                         }
                       }
                     }

        }



     }

}
