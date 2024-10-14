# ObjectStorage
Fine tuning Linode object storage for production
The following set of procedures and configurations will help you make sure you have granular access to make Linode object storage production grade. 
Configurations covered: 
     a. Size of Indivual folders using s3cmd
     b. List Objects within a folder
     c. Policy to purge data within a folder in a bucket

     
A) Getting size of Individual Objects within a folder:

This can be achieved by simply mentioning the folder path within the bucket. 
     
     's3cmd du -H s3://bucketname/FolderPath'
     
"Sample output: 8M       4 objects s3://BucketName/sampleFolder/"


B) List Objects within a folder

     's3cmd ls s3://BucketName/FolderName/'
     

C) Policy to purge data within a folder in a bucket:

Refer to "purgepolicy" file to get sample of the policy. Using prefix, a purge policy can be setup at a folder level. Update policy "Days=30" to required number of days. 

Apply policy using s3cmd: 

     's3cmd setlifecycle purgepolicy.xml s3://SampleBucket'

After applying verify using

     's3cmd getlifecycle s3://SampleBucket'

     
     
      
