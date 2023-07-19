# S3_Elastic_BeanstalkANDAmplify_ElasticBeanStalk_LoadBalancer

S3 + Elastic Beanstalk

no SSL issue since HTTP 

________________________________________________

S3

   {
   
      "Version": "2012-10-17",
      
      "Statement": [
      
        {
        
          "Sid": "PublicReadGetObject",
          
          "Effect": "Allow",
          
          "Principal": "*",
          
          "Action": [
          
            "s3:GetObject"
            
          ],
          
          "Resource": [
          
            "arn:aws:s3:::**YOUR-BUCKET-NAME**/*"
            
          ]
          
        }
        
      ]
      
    }


_________________________________

Amplify + Elastic BeanStalk 

Requires Load Balancer (SSL)

-> 


