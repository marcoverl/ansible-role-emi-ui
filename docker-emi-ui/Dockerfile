# docker build -t docker-emi-ui .

FROM indigodatacloud/centos-sshd:6
MAINTAINER Marco Verlato <Marco.Verlato@pd.infn.it>
LABEL description="Container image to run emi-ui"

RUN ansible-galaxy install marcoverl.emi-ui && \
    ansible-playbook /etc/ansible/roles/marcoverl.emi-ui/tests/main.yml

EXPOSE 22
