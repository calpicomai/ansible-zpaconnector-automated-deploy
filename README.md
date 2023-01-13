# ZPA Connector Deploy Playbook for Ansible

A simple Ansible playbook to assist with deploying a mass amount of ZPA App Connectors quickly.

# How to install?

 - Add the ansible-zpa-connector-deploy-automation.yml in your project directory. Ensure that your App Connectors are defined in your hosts file as "zpa-connectors".
 - Open the file with Nano or Vi and add your App Connector provisioning key to the area that says "{add_app_connector_provisioning_key_here}" and replace the "{hostname}" varible with the templated hostname that is relevant to your organization.
 - Run the playbook with BECOME.
 - Ensure that your connectors are healthy and running after by running a bulk command on Ansible. (ie: sudo ansible zpa-connectors -b --ask-become-pass -u {insert_user} -m shell -a 'sudo systemctl status zpa-connector'
