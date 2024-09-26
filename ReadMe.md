# Setup Spark Cluster

- This repository allows setting up a spark cluster using ansible.
- You should adjust the variables in the [Var File](./vars.yml).
- The [playbook](./playbook.yml) runs the common tasks among all the nodes. Then the zookeeper is installed and configured on master nodes (for high availability). Finally, the spark tasks will be executed on all the nodes.
- To run the ansible commands follow the instructions in [Ansible file](./Ansible.md).
- When you finish copy the service files to the appropriate destination and adjust the ips then run the following:
  -     sudo systemctl enable service_name
  -     sudo systemctl start service_name
  