# Wiki.js Walkthrough

## Running on local device with docker-compose

Clone the repository for docker-compose file.

```shell
git clone https://github.com/snoop2head/wiki-js-docker.git
cd ./wiki-js-docker
```

Run docker on local device && Build two separate images using docker-compose

```shell
docker-compose up --build
```

(Optional) If you want to run specific image only, run as following

``` shell
docker-compose start db
```

or 

```shell
docker-compose start wiki
```

Thereafter, access to [http://localhost:80/](http://localhost/) (or just http://localhost/ )

### Reference

- [Installation Documentation](https://docs.requarks.io/install/docker)
- [Github Repostory](https://github.com/requarks/wiki/)



## Implementing on AWS EC2 Instance

* Click "Continue to Subscribe" at [AWS Marketplace for Wiki.js](https://aws.amazon.com/marketplace/pp/B0832LDTKQ)
* Click "Continue to Configuration"
* Configure software as following
  * Choose Software version to latest version
  * Choose EC2 server region that is close to your users.
  * Click "Continue to Launch"
* Launch wiki.js as following
  * Launch from Website
  * EC2 instance type for at least micro or above
  * Select VPC (or create one if you don't have it), and subnet settings
  * Select Security Group as default
  * Select Key pair (or make one)
  * Click launch
* Wait for 3 minutes, watching cat video clips are recommended
* Go to EC2 isntance, click Security Groups.
* Select security groups for established wiki.js EC2 instance.
  * Edit Inbound rule
  * Add All traffic which are 0.0.0.0/0 and ::/0
  * Save Rules
* Copy Public DNS (IPv4) url, and access the url on web browser.
* A setup screen for Wiki.js should appear. Enter the desired email address and password for the administrator account.
* Enter the full URL to your wiki, without the trailing slash. It's recommended to point a sub-domain / domain to your public IP (e.g. wiki.example.com). If you don't have a domain setup yet, you can use your public DNS endpoint or IP as the URL (e.g. http://xx.xx.xx.xx). This can be changed later in the Adminitration Area (under the General section).
* Click on **Install** to complete the installation. You'll automatically be redirected to the login page once completed. Enter the email and password for the administrator account you entered earlier.

### Reference

* [Wiki.js Documentation for AWS EC2 implementation](https://docs.requarks.io/install/aws)

* [AWS Marketplace for Wiki.js](https://aws.amazon.com/marketplace/pp/B0832LDTKQ)

  

