<div align='center'>

<img src= "https://i0.wp.com/wordpress.org/files/2023/02/allversions.png?w=500&ssl=1" width=300 />

<h1>Helm Wordpress chart</h1>
<p>A Helm chart for the deployment of "Wordpress" server with "MariaDB" database.</p>

<h4> <span> · </span> <a href="https://github.com/eli-pavlov/helm-wordpress-mariadb/blob/master/README.md"> Documentation </a> <span> · </span> <a href="https://github.com/eli-pavlov/helm-wordpress-mariadb/issues"> Report Bug </a> <span> · </span> <a href="https://github.com/eli-pavlov/helm-wordpress-mariadb/issues"> Request Feature </a> </h4>


</div>

# :notebook_with_decorative_cover: Table of Contents

- [About the Project](#star2-about-the-project)
- [License](#warning-license)
- [Contact](#handshake-contact)
- [Acknowledgements](#gem-acknowledgements)


## :star2: About the Project
The purpose of this project is to deploy a Wordpress server in the cloud as a microservice
in an easy and automated way. It is not intended to be used in production environment since 
many features like security, high availablity and scaling are absent in this release. 
However it is a perfect base for a start or as a personal project.

Components:
1. Wordpress image.
2. MariaDB image.
3. Kubernetes cluster depoyed on AWS.
4. AWS CLI, Helm, Kubectl and EKSCTL installed.

Notes:
1. All relevant values are defined in the values.yaml file.
2. For this project 2GB of disk space were defined for each service, for real use you would like to define 20GB+.
3. The password for the database is Base64 encoded as Kubernetes secret.



### :space_invader: Tech Stack
<details> <summary>Client</summary> <ul>
<li><a href="https://wordpress.com/he/">WordPress</a></li>
</ul> </details>
<details> <summary>Server</summary> <ul>
<li><a href="https://httpd.apache.org/">Apache</a></li>
</ul> </details>
<details> <summary>Database</summary> <ul>
<li><a href="https://mariadb.org/">MariaDB</a></li>
</ul> </details>

## :toolbox: Getting Started

### :bangbang: Prerequisites

- Tested on AWS EKS platform.
- Not for production environment! For testing purposes only.
- AWS Kubernetes cluster with "Helm" installed.
- Hosted zone in "Route53" with domain for Wordpress server


### :gear: Installation

Clone the repo:
```bash
git clone https://github.com/eli-pavlov/helm-wordpress-mariadb.git
```
Install the chart using "Helm":
```bash
helm install wordpress helm-wordpress-mariadb/
```
Add "A" record in the hosted zone pointing to "Alias" of the "wordpress" LoadBalancer service.

Login to "Wordpress" and create your website.

Enjoy!!!


## :warning: License

Distributed under the GPLv3 License. See LICENSE.txt for more information.

## :handshake: Contact

Eli Pavlov - www.weblightenment.com - admin@weblightenment.com

Project Link: [https://github.com/eli-pavlov/helm-wordpress-mariadb.git](https://github.com/eli-pavlov/helm-wordpress-mariadb.git)

## :gem: Acknowledgements


- [Kubernetes.io Documentation](https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)
- [Awesome Github Readme File Generator](https://www.genreadme.cloud/)
