# Development Environment
I set up my local Mac as my Ansible Controller and using DigitalOcean as cloud provider.

# Ansible Project​
*Roles*:
    - mysql_db: A role to install and configure MySQL
    - flask_web: A role to install and configure Flask app on webapp droplets
    - python: install dependencies for python on webapp servers
*Tasks*: 
    - networks: Configure firewall rules, managed load balancer, send email notification
    - servers: Create 3 droplets for webapp1, webapp2, and db1
    - apps: Setup servers with roles provided

# Group Variables
- instance_list: An array containing list of servers to deploy
- region: deployed server location
- image: server OS
- size: server specificaions
- project: project name on DigitalOcean
- db_name: Database name
- db_user: Database user to create
- db_user_password: Password for the Database user