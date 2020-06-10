<h2>
  Deploying a high availability web application using AWS.
</h2>



<h4>
  Description:
</h4>

This template deploys infrustructure for a high availability web applcaiton through AWS Cloud Formation. It deploys a Virtual Private Cloud (VPC) with a pair of public/private subnets that span are across two Availability Zones (AZ's). In the private subnets 4 EC2 instances are created. These instances can be reached using a load balancer through a public VPC NAT Gateway. 



<img src="/Diagram/Blank Diagram.jpeg" alt="Blank Diagram" style="zoom:100%;" />





<h4>
  Deployment:
</h4>

First you'll want to create an S3 bucket within the AWS console. There you can upload the contents of your web application. Make sure to have and index.html file and note your bucket name.

Next, modify the ***network-parameters.json*** file as well as the ***server-parameters.json*** file. There you can swap out the bucket name as well as environment name. You will also be able to edit your subnets. 

Finally, run the following commands. It is recommended that you wait for each to complete in AWS before calling the next.

```bash
sh createNetwork.sh
sh createServer.sh
```

If you decide to make modificiation you can also run.

```bash
sh updateNetwork.sh
sh updateServer.sh
```



<h4>
  Acknowledgements
</h4>

[Cloud DevOps Engineer Nanodegree](https://www.udacity.com/course/cloud-dev-ops-nanodegree)

