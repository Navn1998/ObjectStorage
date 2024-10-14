# ObjectStorage
Fine tuning Linode object storage for production
The following set of procedures and configurations will help you make sure you have granular access to make Linode object storage production grade. 
Configurations covered: 
     a. Size of Indivual folders using s3cmd
     b. List Objects within a folder
     c. Policy to purge data within a folder in a bucket
A) Getting size of Individual Objects within a folder
     This can be achieved by simply mentioning the folder path within the bucket. 
     's3cmd du -H s3://bucketname/FolderPath'
     
     
      
