# Github Actions e Terraform

## Tecnologias:
Terraform: é uma ferramenta para automação de pipelines de infra, com ele é possível definir tasks que serão executadas de acordo com as necessidades de DevOps, permitindo criar instâncias, escalar recursos e controlar o funcionamento de uma infraestrutura por meio de um arquivo de controle de status.

Github Actions: é uma ferramenta do github capaz de executar diversas pipelines configuraveis, desde execução de códigos de testes para validar o código alterado (branchs, PRs e demais actions do github) à ativação de scripts externos capazes de efetuar as pipelines de CI/CD (ex: terraform).

A união dessas duas ferramentas se dá pela configuração feita no workflow do Github Actions, tal workflow é responsável por planejar e aplicar uma série de tarefas do Terraform Cloud API para que a cada PR feito no github, seja feito o deploy da instância na AWS. 

Segue abaixo o fluxo de execução:
![image](https://github.com/FelipeSaadi/terraform-github-actions/assets/54749257/1c80bf00-55e9-43d5-aecc-4b398956ed4c)

## Execução 

Definindo as variáveis de ambiente:
![image](https://github.com/FelipeSaadi/terraform-github-actions/assets/54749257/224f51c1-d54e-405e-8b5c-9e2738cfb1bc)

Definindo a Secret:
![image](https://github.com/FelipeSaadi/terraform-github-actions/assets/54749257/eb03f850-2c7c-46f9-8371-00cbabab112d)

Ajustando variaveis do Terraform:
![image](https://github.com/FelipeSaadi/terraform-github-actions/assets/54749257/7a168f20-06b4-4b83-89e0-067c2fc8b8bf)

PR acionando o Terraform Plan:
![image](https://github.com/FelipeSaadi/terraform-github-actions/assets/54749257/2bb34656-aaf8-4629-95f2-4846523d261b)

Rodando o código:
![image](https://github.com/FelipeSaadi/terraform-github-actions/assets/54749257/b34954ce-6cf2-4d0d-802e-76d7202b1f91)

Passando por todos os checks:
![image](https://github.com/FelipeSaadi/terraform-github-actions/assets/54749257/877b6d4f-c250-4473-9eae-af9afbb98edd)

Aplicando as ações:
![image](https://github.com/FelipeSaadi/terraform-github-actions/assets/54749257/a0262948-a966-4997-a982-ff951c8fe180)

Resultado no Terraform Cloud:
![image](https://github.com/FelipeSaadi/terraform-github-actions/assets/54749257/c034fb98-081e-4fbd-b92d-ec08158160f6)

Resultado na AWS:
![image](https://github.com/FelipeSaadi/terraform-github-actions/assets/54749257/9be59099-2cdd-4a52-aae4-52abe4bba96c)
