+++
title = "c. Create data repository association between S3 and FSx for Lustre"
date = 2019-09-18T10:46:30-04:00
weight = 100
tags = ["tutorial", "lustre", "FSx", "S3"]
+++

In this step, you will create a [Data Repository Association](https://docs.aws.amazon.com/fsx/latest/LustreGuide/create-dra-linked-data-repo.html) (DRA) between the S3 bucket and FSx Lustre Filesystem. 

1. Navigate to the [FSx console](https://console.aws.amazon.com/fsx/home). On this console you will see the file system you created in section a. Click on the file system id with name **sc22lab2** and you will view the details of the filesystem as shown below. Make sure the status shows as **available** to make sure the create step from section a is complete 

![viewsfsxl](/images/fsx-for-lustre-hsm/viewfsxl.png)

2. Scroll down a little on this screen and click on **Data Repository** tab shown below

![datarepotab](/images/fsx-for-lustre-hsm/datarepotab.png)

3. Here click on **Create data repository association** button as shown below 

![clickdra](/images/fsx-for-lustre-hsm/clickdra.png) 

4. On the create data repository association form name the filesystem path which needs to be associated for data repository and paste the name of your S3 bucket. You can get the name of your S3 bucket with `echo ${BUCKET_NAME_DATA}` in Cloud9 terminal or navigate to the [S3 console](https://console.aws.amazon.com/s3/) and copy the name of the bucket you created and paste it in the form as shown below. 

![draform1](/images/fsx-for-lustre-hsm/draform1.png)

5. Scroll down to view the rest of the default options and do NOT change any of them for the purpose of this lab. The rest of the options indicate your export import preferences for data movement between your file system and S3 bucket. Now click on **Create** button like shown below to create the data repository action. 

![createdra](/images/fsx-for-lustre-hsm/createdra.png)

{{% notice info %}}
Step 5 is expected to take a few  minutes. You are going to check this again and you can proceed with the next section. While creating you should be able to see the status as shown below. 
{{% notice info %}}

![dracreating](/images/fsx-for-lustre-hsm/dracreating.png)
