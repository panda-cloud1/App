@Library ('SHARED_LIBRARY') _
pipeline {
    agent any
    
    stages {
       
        stage ("1. Git Checkout") {
            steps {
            aGitCheckout (
                        branch: 'main',
                        url: 'https://github.com/nasirpatel1957/App.git'
                    )
                }
            }

         stage ("2. Maven Unit Testing") {
            steps {
                script{
                    bMavenUnitTest ()
                }
            }
         }           

          stage ("3. Maven Integration Testing") {
            steps {
                script{
                    cMavenIntegrationTest ()
                    }
                }
            }   

        //    stage ("4. Sonarqube Static code analysis") {
        //     steps {
        //         script{
        //             def credentialsId = 'sonar-new'
        //             dStaticCodeAnalysis (credentialsId)
        //             }
        //         }
        //    }

        //    stage ("5. Sonarqube Quality Gate Check") {
        //     steps {
        //         script{
        //             def credentialsId = 'sonar-new'
        //             eQualityGateCheck (credentialsId)
        //             }
        //         }
        //     }  

           stage ("6. Maven Build") {
            steps {
                script{
                    fMavenBuild ()
                    }
                }
            }  

    }
}   
   

    //        stage ("7. Docker Build") {
    //         steps {
    //             script{
    //                 7.DockerBuild ()
    //                 }
    //             }
    //         }  

    //        stage ("8. Trivy Scan") {
    //         steps {
    //             script{
    //                 }
    //             }
    //         }  

    //        stage ("9. Docker Push") {
    //         steps {
    //             script{
    //                 }
    //             }
    //         }  

    //        stage ("10. Docker Cleanup") {
    //         steps {
    //             script{
    //                 }
    //             }
    //         }  

    //        stage ("11. Run Terraform commands to create EKS") {
    //         steps {
    //             script{
    //                 EKSCreate ()
    //                 }
    //             }
    //         }  

    //        stage ("12. Connect to EKS through AWS CLI") {
    //         steps {
    //             script{
    //                 EKSCreate ()
    //                 }
    //             }
    //         }  

    //        stage ("13. Deploy on EKS") {
    //         steps {
    //             script{
    //                 EKSCreate ()
    //                 }
    //             }
    //         }  
    //     }
    // }