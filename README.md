Build and deploy WordPress application by using Docker,
Docker-compose file and create the image push that created image into docker hub registry and host the image through k8’s (declarative manifest method).
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
•	Login to amazon console, launch instance access through git bash.
•	Install docker and start and enable it and check the status of it.
   Update package index:sudo yum update -y
   Install Docker:<sudo yum install docker -y>, <sudo service docker start>
•	Now add the ec2-user to docker group to run commands 
  <sudo usermod –aG docker ec2-user>
•	Now create docker file with command <vi dockerfile
   
•	Now use the command <docker build -t rakesh.>
•	Then it starts building images
•	Check the images with <docker images>.
•	Then push these images in to docker hub we need to login first with command <docker login> give the credentials login get succeeded.
•	Then push the image to docker hub with command <docker tag rakesh rakesh0305/word>.
•	Install kops and kubectl from browser and check versions.
•	Create a s3 bucket with command of <aws mb s3://k8-rakesh>. And check the list of buckets
•	Now use command 
  <export KOPS_STATE_STORE=S3://k8-rakesh> 
  kops know where to store all retrieve state information if the k8 cluster.
•	Generate key pair with command <ssh-keygen> is a versatile tool that can be used in a Kubernetes environment to generate SSH key pairs for securely accessing and managing cluster nodes.
•	Create a file of deployment. File, mysql.file and service.yml  
•	Create a cluster with 
  <kops create cluster  --name= rakesh0305.k8s.local --state s3://k8-rakesh –zones=us-east-2a,us-east-2b –node-size=t2.micro --yes
•	Now deploy in to cluster ,
  <kutectl apply -f mqsql.yml>
  <kutectl apply -f  service.yml>
  <kutectl apply -f  service.yml>
  ![image](https://github.com/thudumrakesh/k8-wordpress/assets/144659414/12557db6-d75f-4327-84e5-2ec068e52b61)








