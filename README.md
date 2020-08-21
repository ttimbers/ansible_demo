# Ansible demo

Demo to get to know ansible.

1. Clone this repo to your laptop

2. Install Ansible on your local computer via `conda install -c conda-forge ansible`

3. Set-up an EC2 instance. Add the ansible machine's (e.g., your laptop's) public key to `~/.ssh/authorized_keys` on the EC2 instances.

4. Open the `anisible/inventory` file in a plain text editor and replace `<STUDENT_HUB_IP>` with the IP address for your EC2 instance (this is the value for the IPv4 Public IP address found under the “Description” tab for your EC2 instance on the AWS EC2 Dashboard). Note: this demo assumes you used Ubuntu as OS on your EC2 instance, if you used another OS (e.g., Centos) then you would also have to replace `ubuntu` in the `anisible/inventory` file with `centos`, for example.

5.  To test this is all setup correctly you can try pinging one of the hubs via running the following on your laptop: 
  ```
  cd ansible
  ansible studentHub -m ping
  ```

6. And you can test running ansible play in this directory via running the following on your laptop: 
  ```
  ansible-playbook -i inventory-ad-hoc hello.yml
  ```
