pipeline {
        agent any
                stages {
                       stage('One') {
                                steps {
                                                                                                                                                                     echo 'hello'
                                       }
                                      } 
                        stage('Two') {
                                steps {
                                                                                                                                                                    input('Do you want to proceed?') 
                                       }
                                      } 
                stage('Three') {
                      when {
                        not{ 
                            branch "master"                                                                                                                    
                                           }
                                       }
                                        steps {
                                                echo "HI"
                                            }
                                      }

                        stage('Four') {
                                        parallel {
                                                stage('Unit Test') {
                                                                   steps {
                                                                          echo "Running the unit test..."
                                                                         }
                                                                   }
                                                stage('Integration test') {
                                                                     agent { 
                                                                           docker { 
                                                                                    reuseNode false
                                                                                    image 'Ubuntu'
                                                                                  }
                                                                     steps {
                                                                            echo 'Running the integration test..'
                                                                           }
                                                                     }
                                                      }

                     }                
                      
                 }
}
}           
