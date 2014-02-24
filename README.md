## Magento+Nginx+PHP-FPM Deployment

- Requires Ansible 1.2 or newer
- Expects CentOS/RHEL 6.x hosts

These playbooks deploy a simple all-in-one configuration of the popular
Magento eCommerce platform, frontend by the Nginx web server and the
PHP-FPM process manager. To use, copy the `hosts.example` file to `hosts` and 
edit the `hosts` inventory file to include the names or URLs of the servers
you want to deploy.

Then run the playbook, like this:

	ansible-playbook -i hosts site.yml

The playbooks will configure MySQL, Magento, Nginx, and PHP-FPM. When the run
is complete, you can access the server to begin the Magento configuration.

### Next Steps / TODO

Ideas for improvement:

- Parameterize the Magento deployment to handle multi-site configurations.
- Separate the components (PHP-FPM, MySQL, Nginx) onto separate hosts and 
hande the configuration appropriately.
- Add support for automatic local / development Vagrant deployment
- Add support for automatic configuration / population of sample / demo products