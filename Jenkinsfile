pipeline{
    agent Any
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
           
          
    
