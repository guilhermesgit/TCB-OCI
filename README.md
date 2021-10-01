Implementação de IAC utilizando Ansible e enviando emails usando sendgrid.

1) Pré-requisitos :
 ansible-vault
 ansible-galaxy
 sendgrid
 
 2)Dentro do cloud shell da OCI já possui o ansible instalado e as seguintes versões desse cenário:
 ansible [core 2.11.5] 
 jinja version = 3.0.1
 python version = 3.6.8 
 
 3)Instalar o collection do sendgrid necessário para envio de email via API.
 ansible-galaxy collection install community.general
 
 4)Dentro de cada role existem as VARS, logo após editar cada VAR em cada role criada pelo ansible-galaxy, criptografá-la usando:
 ansible-vault encrypt nomedarole/vars/main.yml
 
 5)Criar a conta no sendgrid e salvar a API, editar a role: users/vars/main.yml e colocar a API.
 Criptograr a VAR utilizando ansible-vault.
 
 6) Rodando o playbook : Pode rodar separado , utilizando TAGs criado no main.yml raiz ou poderá utilizar sem TAGS rodando o projeto inteiro.
  ansible-playbook main.yml --tags='compartment' --ask-vault-password
