# S3_Elastic_BeanstalkANDAmplify_ElasticBeanStalk_LoadBalancer

S3 + Elastic Beanstalk

![image](https://github.com/junxian428/S3_Elastic_BeanstalkANDAmplify_ElasticBeanStalk_LoadBalancer/assets/58724748/8901e63d-bcad-47a6-8906-a65fdcffc618)

no SSL issue since HTTP 

________________________________________________

Frontend: VueJS

npm run build

Then copy files under dist to S3...


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

Backend:

Create Java 17 environment 


./mvnw clean install


Then copy jar file into Elastic Bean Stalk to deploy

Make sure environment 

PORT 8080 is set 


![image](https://github.com/junxian428/S3_Elastic_BeanstalkANDAmplify_ElasticBeanStalk_LoadBalancer/assets/58724748/b49ff47e-2437-4811-a774-2aa173ca0d41)


_________________________________

Amplify + Elastic BeanStalk 

![image](https://github.com/junxian428/S3_Elastic_BeanstalkANDAmplify_ElasticBeanStalk_LoadBalancer/assets/58724748/99aa1b91-b830-4b30-98c2-3090f0e9899b)


Frontend: VueJS

Amplify can import repository from GitLab, BitBucket etc...


It will be HTTPS, Therefore the application will face the HTTPS over HTTP insecure API there
![Untitled design (1)](https://github.com/junxian428/S3_Elastic_BeanstalkANDAmplify_ElasticBeanStalk_LoadBalancer/assets/58724748/b8bbe676-a4ab-45df-9ced-416960362beb)
fore requires Load Balancer to make the endpoint as HTTPS.
But I have encouter privacy error from browser (Going to solve)



Requires Load Balancer (SSL)

-> 

![Untitled Diagram drawio (9)](https://github.com/junxian428/S3_Elastic_BeanstalkANDAmplify_ElasticBeanStalk_LoadBalancer/assets/58724748/c519c4a8-3ad1-456a-8e3f-016b06f7857b)



