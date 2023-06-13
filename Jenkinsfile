pipeline{
    agent any
    Stages{
        Stage('One'){
            Steps{
                echo 'Hi! This is sai from netcracker running 1st pipeline from Github'
                 }
            }
        Stage('Two'){
            Steps{
                input('Do you want to proceed ?')
                 }
            }
        Stage('Three'){
            when{
                not{
					branch 'master';
                   }
            Steps{
                echo 'Hello  .. dear !'
                }
            }
        Stage('Four'){
            parallel{
                Stage('Unit Test'){
                    Steps{
                        echo 'Running the Unit Test ..'
                        }
                    }
                Stage('Integration Test'){
                    agent{
                        docker{
                            reuseNode false
                            image 'ubuntu'
                            }
                        }
                    Steps{
                        echo 'Running the Integration Test'
                        }
                     }
                 }
             }
         }
    }
}
