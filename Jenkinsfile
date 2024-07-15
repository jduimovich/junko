@Library('RHTAP_Jenkins') _
pipeline {  
    agent any
    environment {
        ROX_API_TOKEN  = credentials('ROX_API_TOKEN')
        ROX_CENTRAL_ENDPOINT = credentials('ROX_CENTRAL_ENDPOINT')
        GITOPS_AUTH_PASSWORD = credentials('GITOPS_AUTH_PASSWORD')
        QUAY_IO_CREDS = credentials('QUAY_IO_CREDS')
    }   
    stages { 
        stage('init.sh') {
            steps {
                script { 
                    rhtap.info ("ABOUT TO libraryResource('init.sh')")
                    libraryResource('init.sh')
                    rhtap.info ("------")")
                    
                    rhtap.info ("ABOUT TO libraryResource('doesnotexist.sh')")
                    libraryResource('doesnotexist.sh')
                    rhtap.info ("------")")

                    rhtap.info ("TEST RHTAP")
                    rhtap.init() 
                }
            }
        }
    }
}