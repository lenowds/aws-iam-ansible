# ANSIBLE HERO

*Aqueles que mais resolvem problemas, são chamados de heróis.



![](https://media.giphy.com/media/ZmEgiY05sAM1yGo4nc/giphy.gif)





#### O Projeto

Neste projeto estamos considerando que a empresa possui em média 100 pessoas na equipe de TI. Após análise estratégica, a empresa decidiu migrar para seus workloads para AWS. Estes usuários terão que ser criados, pois a equipe acessará a console para realizar as operações.

Este projeto tem por objetivo propor uma solução que atinja os requisitos da empresa, levando os usuários do seu ambiente On-premises para AWS de forma 100% automatizada utilizando Ansible.

Além de migrar estes usuários de forma automatizada, deverá associar as permissões aos grupos. Como uma melhor prática de segurança os usuários terão que ter o MFA – Autenticação por dois fatores (*Multi-fator authentication*) habilitado.

#### Mas o que é o Ansible?

É uma ferramenta super *user-friendly* utilizada para fazer a automação do gerenciamento de configuração em ambientes Cloud, especialmente com uma cultura *DevOps*. Além disso, o Ansible é muito poderoso devido ter o que chamamos de *collections*, que são espécie de plugins que consegue usar para fazer automações e conectar os seus scripts ou os seus playbooks.

Para ter uma experiência parecida comigo, estou aplicando meu playbook direto na console da AWS. O playbook deste projeto, pode ser aplicado a partir de qualquer vm ou no seu próprio laptop.

![](https://media.giphy.com/media/l3V0dy1zzyjbYTQQM/giphy.gif)

#### Requisitos

Com certeza ter uma conta na AWS, estar autenticado e dentro da [AWS Console](https://console.aws.amazon.com/). 

Criar um usuário com perfil de administrador e guardar a ACCESS KEY e SECRET ACCESS KEY. Como será aplicado o playbook na console da AWS, o usuário será do tipo  programático e acesso na console.



<u>**python >= 2.6**</u>

No meu caso não foi preciso instalar, mas se precisar fica a dica: https://www.python.org/downloads/

<u>**[Ansible >= 2.9](https://docs.ansible.com/ansible/latest/installation_guide/index.html)**</u> 

```
pip3 install ansible
```

<u>**boto**</u>

```
pip3 install boto
```



#### All Ready???

Depois que os arquivos do projeto foram clonados para dentro da console, vamos ao que interessa.

Aplicando o playbook que fará a leitura do arquivo csv, criará os grupos associando as políticas de acesso, inclusive a política de MFA. Essa política também será criada pelo Ansible.

Na console da AWS executar:

```
ansible-playbook aws-users-import.yml
```



![](https://media.giphy.com/media/frBbpfHZREUfvRmPQE/giphy.gif)







Sugestões são bem vindas, e pra quem quiser me adicione no [linkedin](https://www.linkedin.com/in/leniel-dos-santos-7813a924/) e vamos batar um papo. 



Linkedin: https://www.linkedin.com/in/leniel-dos-santos-7813a924/
