here we are creating a customfact to get the verion of the Git and httpd.
File name is git_httpd_v.fact. its having that script to get the version details

#To copy customfact files into all nodes.

ansible all -m copy -a "src=/etc/ansible/facts.d/git_httpd_v.fact dest=/etc/ansible/facts.d/git_httpd_v.fact mode='0755'" -b

#To run the customfacts in required servers, here i used to run my all nodes.
ansible all -m setup -a "filter=ansible_local"

