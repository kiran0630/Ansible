## WordPress+Nginx+PHP-FPM Deployment

- Requires Ansible 1.2 or newer
- Expects Debian 9 (Stretch) or Ubuntu 16.04 LTS or newer

These playbooks deploy a simple all-in-one configuration of the popular
WordPress blogging platform and CMS, frontend by the Nginx web server and the
PHP-FPM process manager. To use, copy the `hosts.example` file to `hosts` and
edit the `hosts` inventory file to include the names or URLs of the servers
you want to deploy.

Then run the playbook, like this:

	ansible-playbook -i hosts site.yml

The playbooks will configure WordPress, Nginx, PHP-FPM and MariaDB (or MySQL).
When the run is complete, you can access your server to begin the WordPress
configuration.

### Ideas for Improvement

Here are some ideas for ways that these playbooks could be extended:

- Parameterize the WordPress deployment to handle multi-site configurations.
- Separate the components (PHP-FPM, MariaDB, Nginx) onto separate hosts and
handle the configuration appropriately.
- Handle WordPress upgrades automatically.

We would love to see contributions and improvements, so please fork this
repository on GitHub and send us your changes via pull requests.