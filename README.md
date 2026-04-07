# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS
- Data: 07/04/2026
- Empresa: Abstergo Industries
- Responsável: Anderson Gomes da Silva

## Introdução
Este relatório apresenta o processo de implementação de ferramentas AWS na empresa Abstergo Industries, realizado por Anderson Gomes da Silva. O objetivo do projeto foi elencar serviços AWS, com a finalidade de realizar diminuição de custos operacionais imediatos, além da possibilidade de venda de equipamentos do Data Center da organização convertendo em recursos ao caixa.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:
O modelo de serviço proposto é PaaS - Plataform as a Service (Plataforma como serviço)

### Etapa 1:

- Solução/Ferramenta: Amazon EC2 - Elastic Compute Cloud em conjunto com os serviços AWS Auto Scaling, AWS Elastic Load Balancing (ELB) e  Amazon VPC (Virtual Private Cloud).

- Foco: hospedar sites e aplicações, executar rotinas sistêmicas do ERP e outras aplicações da organização, processamento de dados (Big Data) e demais rotinas gerais.

- Descrição de caso de uso: A implantação do serviço Amazon EC2 permitirá hospedar o site de vendas; executar aplicações como APIs utilizadas para interface com clientes e fornecedores; gerenciar o ciclo operacional das rotinas do sistema ERP, assegurando a integridade e segurança dos dados transacionados, bem como garantir a conformidade com os processos operacionais internos relacionados ao ERP; processar dados (Big Data) para análises internas e tomadas de decisão da organização.

  Os modelos de instancias EC2 sugeridas para implantação são: otimizada para memória (Memory Optimized), que apresenta alto desempenho   para processamentos de dados na memória (RAM) em conjunto com a otimizada para uso geral (General Purpose) para atender as rotinas gerais da organização e para hospedar o site de vendas.

  O modelo de escala sugerido para o AWS Auto Scaling é um híbrido com o modelo Preditiva (Predictive), considerando que a empresa já tem um histórico de demanda de utilização de recursos em conjunto com a o modelo Agendada (Scheduled), para atender picos de demandas sazonais.

  Em complemento ao AWS Auto Scaling será implementado o AWS Elastic Load Balancing (ELB) para distribuir de forma otimizada as entradas de acesso a rede, considerando o modelo NLB - Network Load Balancer  para usuários internos da organização e o modelo ALB - Application Load Balancer para usuários externos.

  Será implantado também o serviço Amazon VPC (Virtual Private Cloud), que será a estrutura de rede da empresa, com a estruturação de uma sub-rede (subnet) privada para gestão dos dados e acessos de usuários internos da organização e uma sub-rede (subnet) pública para gestão dos dados e acesso de usuários externos ao site de vendas e APIs de interface com clientes e fornecedores.

  Ganho financeiro estimado a partir de 30% - anexo 1.

### Etapa 2:

- Solução/Ferramenta: Amazon RDS - Relational Database Service.

- Foco: armazenamento e gerenciamento de bancos de dados relacionais como do ERP e outras aplicações da organização que necessitem de armazenamento de dados estruturados.

- Descrição de caso de uso: Implantação para armazenamento de dados estruturados do sistema ERP e demais aplicações da organização que necessitem de armazenamento de dados estruturados, gestão do banco de dados com espelhamento, backup e restore, bem como o monitoramento e desempenho geral do banco de dados.

  O banco de dados será implantado dentro da sub-rede (subnet) privada da organização.

  Ganho financeiro estimado a partir de 30% - anexo 2.

### Etapa 3:
- Solução/Ferramenta: Amazon S3 – Simple Storage Service.
  
- Foco: armazenamento de backups, documentações técnicas e gerais, imagens, vídeos, arquivos de log e outros arquivos em geral.

- Descrição de caso de uso: Implantação para armazenamento de backups dos sistemas da organização, arquivos de registros de log de acesso aos sistemas, documentos técnicos relacionados aos medicamentos comercializados, documentos em geral, planilhas, arquivos de imagem, vídeos entre outros.

  O banco de dados será implantado dentro da sub-rede (subnet) privada da organização.

  Ganho financeiro estimado a partir de 30% - anexo 3.

## Aspectos gerais das etapas 1 a 3

- Descrição de caso de uso: Implantação dos serviços de segurança AWS IAM (Identity and Access Management) para gerenciar usuários, perfis de acesso e permissões de segurança, Security Groups (SGs) como firewall no nível das instâncias e Network ACLs (NACLs) como firewall no nível das sub-redes (subnets).
  
  Além dos ganhos financeiros estimados em cada uma das etapas são esperados benefícios intangíveis com maior escalabilidade, elasticidade, disponibilidade de recursos, confiabilidade, segurança integrada, latência da rede e flexibilidade.


## Conclusão
A implementação das ferramentas descritas nas etapas 1 a 3  na empresa Abstergo Industries tem como esperado ganhos financeiros a partir de 30%, além dos benefícios intangíveis descritos acima, o que aumentará a eficiência e a produtividade da empresa. 
Recomenda-se a implantação das ferramentas indicadas e a busca contínua por novas tecnologias que possam melhorar ainda mais os processos da empresa.

## Anexos
- [Anexo 1 - Redução estimada Amazon EC2]( https://aws.amazon.com/pt/blogs/publicsector/tco-cost-optimization-best-practices-for-managing-usage/#:~:text=While%20moving%20to%20the%20cloud,instances%20outside%20of%20work%20hours.)
  
- [Anexo 2 – Redução estimada Amazon RDS]( https://www.google.com/search?q=qual+a+estimativa+m%C3%ADnima+e+m%C3%A1xima+de+redu%C3%A7%C3%A3o+de+custo+com+implanta%C3%A7%C3%A3o+do+AWS+RDS+estudo+de+caso+da+Amazom&sca_esv=b103bd3d850b62ba&biw=1366&bih=599&sxsrf=ANbL-n6uFBWEh3joGmgLIumo-aQoBMEX5w%3A1775594765622&ei=DW3VaZ_ZJY-55OUPw_XjuQk&ved=0ahUKEwjfk5T6zdyTAxWPHLkGHcP6OJcQ4dUDCBE&uact=5&oq=qual+a+estimativa+m%C3%ADnima+e+m%C3%A1xima+de+redu%C3%A7%C3%A3o+de+custo+com+implanta%C3%A7%C3%A3o+do+AWS+RDS+estudo+de+caso+da+Amazom&gs_lp=Egxnd3Mtd2l6LXNlcnAib3F1YWwgYSBlc3RpbWF0aXZhIG3DrW5pbWEgZSBtw6F4aW1hIGRlIHJlZHXDp8OjbyBkZSBjdXN0byBjb20gaW1wbGFudGHDp8OjbyBkbyBBV1MgUkRTIGVzdHVkbyBkZSBjYXNvIGRhIEFtYXpvbUgAUABYAHAAeAGQAQCYAQCgAQCqAQC4AQPIAQD4AQGYAgCgAgCYAwCSBwCgBwCyBwC4BwDCBwDIBwCACAE&sclient=gws-wiz-serp)

- [Anexo 3 – Redução estimada Amazon S3](https://www.google.com/search?q=qual+a+estimativa+m%C3%ADnima+e+m%C3%A1xima+de+redu%C3%A7%C3%A3o+de+custo+com+implanta%C3%A7%C3%A3o+do+AWS+Amazon+S3+estudo+de+caso+da+Amazom&sca_esv=b103bd3d850b62ba&sxsrf=ANbL-n4ZBl4VfFFMXvXd-qSt9FwOECm23A%3A1775595718779&source=hp&ei=xnDVaY-zLbfR5OUPkPi80As&iflsig=AFdpzrgAAAAAadV-1nP_ik1-Zz7_QibdrN8h_Ege_kjF&ved=0ahUKEwiPrtLA0dyTAxW3KLkGHRA8D7oQ4dUDCB4&uact=5&oq=qual+a+estimativa+m%C3%ADnima+e+m%C3%A1xima+de+redu%C3%A7%C3%A3o+de+custo+com+implanta%C3%A7%C3%A3o+do+AWS+Amazon+S3+estudo+de+caso+da+Amazom&gs_lp=Egdnd3Mtd2l6InVxdWFsIGEgZXN0aW1hdGl2YSBtw61uaW1hIGUgbcOheGltYSBkZSByZWR1w6fDo28gZGUgY3VzdG8gY29tIGltcGxhbnRhw6fDo28gZG8gQVdTIEFtYXpvbiBTMyBlc3R1ZG8gZGUgY2FzbyBkYSBBbWF6b21IAFAAWABwAHgAkAEAmAEAoAEAqgEAuAEDyAEA-AEC-AEBmAIAoAIAmAMAkgcAoAcAsgcAuAcAwgcAyAcAgAgB&sclient=gws-wiz)


## Assinatura do Responsável pelo Projeto:

Anderson Gomes da Silva
