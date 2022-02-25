#PIPELINE for this facebook project in jenkins.

pipeline {

  agent any

    parameters {
              string(name: 'Version',
              defaultValue: 'facebook-2.0',
              description: 'Facebook project')
           }
     stages {
                     stage('Checkout'){
                                steps
                                {

                                    checkout([$class: 'GitSCM', branches: [[name: '*/facebook-2.0']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/yarli9951/facebook.git']]])
                                  }

        }



     }

}
