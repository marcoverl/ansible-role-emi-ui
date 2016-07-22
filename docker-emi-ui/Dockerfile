# docker build -t docker-emi-ui .

FROM centos:6
MAINTAINER Marco Verlato <Marco.Verlato@pd.infn.it>
LABEL description="Container image to run emi-ui"
RUN yum -y install ansible \
    openssh \
    openssh-clients \
    openssh-server

RUN ansible-galaxy install marcoverl.emi-ui && \
    ansible-playbook /etc/ansible/roles/marcoverl.emi-ui/tests/emiui.yml

EXPOSE 22
CMD    ["/usr/sbin/sshd", "-D"]
