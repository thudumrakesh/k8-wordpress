
<h1 align="center">Hi 👋, I'm Rakesh</h1>
<h3 align="center">A passionate AWS & DevOps Engineer from India</h3>
<(img align="right" alt="Coding" width="400" src="https://iconscout.com/lottie-animation/devops-8995909">

<p align="left"> <img src="https://komarev.com/ghpvc/?username=thudumrakesh&label=Profile%20views&color=0e75b6&style=flat" alt="thudumrakesh" /> </p>

<p align="left"> <a href="https://github.com/ryo-ma/github-profile-trophy"><img src="https://github-profile-trophy.vercel.app/?username=thudumrakesh" alt="thudumrakesh" /></a> </p>

- 🔭 I’m currently working on **DevOps Projects**

- 🌱 I’m currently learning **AWS & DevOps tools**

- 👯 I’m looking to collaborate on **DevOps Projects**

- 💬 Ask me about **AWS & DevOps tools**

- 📫 How to reach me **thudumrakesh68@gmail.com**

### Blogs posts
<!-- BLOG-POST-LIST:START -->
<!-- BLOG-POST-LIST:END -->

<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://dev.to/thudumrakesh/thudumrakesh" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/devto.svg" alt="thudumrakesh/thudumrakesh" height="30" width="40" /></a>
<a href="https://linkedin.com/in/www.linkedin.com/in/thudumrakeshh" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="www.linkedin.com/in/thudumrakeshh" height="30" width="40" /></a>
<a href="https://instagram.com/being_rakesh" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg" alt="being_rakesh" height="30" width="40" /></a>
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://aws.amazon.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="aws" width="40" height="40"/> </a> <a href="https://www.docker.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40"/> </a> <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> <a href="https://www.jenkins.io" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/jenkins/jenkins-icon.svg" alt="jenkins" width="40" height="40"/> </a> <a href="https://kubernetes.io" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/kubernetes/kubernetes-icon.svg" alt="kubernetes" width="40" height="40"/> </a> <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> <a href="https://www.selenium.dev" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/detain/svg-logos/780f25886640cef088af994181646db2f6b1a3f8/svg/selenium-logo.svg" alt="selenium" width="40" height="40"/> </a> </p>

<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=thudumrakesh&show_icons=true&locale=en&layout=compact" alt="thudumrakesh" /></p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=thudumrakesh&show_icons=true&locale=en" alt="thudumrakesh" /></p>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=thudumrakesh&" alt="thudumrakesh" /></p>

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
Build and deploy WordPress application by using Docker,
Docker-compose file and create the image push that created image into docker hub registry and host the image through k8’s (declarative manifest method).
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

•	Login to amazon console, launch instance access through git bash.
•	Install docker and start and enable it and check the status of it.
   Update package index:sudo yum update -y
   Install Docker:<sudo yum install docker -y>, <sudo service docker start>
•	Now add the ec2-user to docker group to run commands 
  <sudo usermod –aG docker ec2-user>
  
 --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- 

•	Now create docker file with command <vi dockerfile
•	Now use the command <docker build -t rakesh.>
•	Then it starts building images
•	Check the images with <docker images>.
•	Then push these images in to docker hub we need to login first with command <docker login> give the credentials login get succeeded.
•	Then push the image to docker hub with command <docker tag rakesh rakesh0305/word>.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

•	Install kops and kubectl from browser and check versions.
•	Create a s3 bucket with command of <aws mb s3://k8-rakesh>. And check the list of buckets
•	Now use command 
  <export KOPS_STATE_STORE=S3://k8-rakesh> 
  kops know where to store all retrieve state information if the k8 cluster.
  
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

•	Generate key pair with command <ssh-keygen> is a versatile tool that can be used in a Kubernetes environment to generate SSH key pairs for securely accessing and managing cluster nodes.
•	Create a file of deployment.yml, mysql.yml and service.yml  

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------•	Create a cluster with 
  <kops create cluster  --name= rakesh0305.k8s.local --state s3://k8-rakesh –zones=us-east-2a,us-east-2b –node-size=t2.micro --yes
•	Now deploy in to cluster ,
  <kutectl apply -f mqsql.yml>
  <kutectl apply -f  service.yml>
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  After 10-15min copy the DNS of elb and browse it in the browser
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 ![image](https://github.com/thudumrakesh/k8-wordpress/assets/144659414/0fd91490-bcf1-463a-bd90-b056168b71ae)
 
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  
  ![image](https://github.com/thudumrakesh/k8-wordpress/assets/144659414/12557db6-d75f-4327-84e5-2ec068e52b61)
  








