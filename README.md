# Referências
CMDB: https://www.opservices.com.br/cmdb/

Ansible: https://docs.ansible.com/

Curso na MUC: https://muc.mandic.com.br/mod/scorm/player.php?a=85&currentorg=j4ydU1xOlfxps_organization&scoid=198

Curso básico de ansible: https://www.udemy.com/course/ansible-essentials-simplicity-in-automation/learn/lecture/6125460#overview

Curso MASTERNING ANSIBLE: https://www.udemy.com/course/mastering-ansible/learn/lecture/3731986#overview

```
## PLAYBOOK

O projeto foi dividido em duas etapas, a de provisionamento do ambiente e a de deploy.
No provisionamento lançamos a instância do EC2 t3a.medium com o security group com os devidos protocolos abertos, e criação da zona de DNS com as entradas necessárias (com exceção da entrada "." do tipo A que será necessário setar na mão)


## ROLES

Para o provisionamento do ambiente temos a role "create" e para deploy do servidor foi dividido em 6 roles
certbot  create  instalation  magento  nginx  tomcat  wordpress


## INSTALATION
Atualização e instalação de todos os pacotes necessários para a pré configuração do servidor


## NGINX
Criação do conf do nginx com todos os VHost dos 4 sites e configurações das pastas necessárias para dar permissão ao nginx para excecutar


## WORDPRESS
Criação do banco de dados MariaDB, atualização do mesmo para a versão mais recente 10.5 e instalação do wordpress


## MAGENTO
Instalação do composer e magento, correções de permissão em alguns arquivos que perderam a devida permissão após o restart do php-fpm, necessário reatribuir as permissões do session do php


## TOMCAT
Instalação do Tomcat 9.0.37, configurado o mesmo no sustemd


## CERTBOT
Por último atribuído criptografia SSL aos sites utilizando o certbot

