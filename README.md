# GrafanaDashboardAWS

A ideia desse projeto é criar um painel à vista que dá uma visão macro da infraestrutura AWS utilizada com alguns itens de compliance e governança. Em resumo, o Zabbix coleta as informações através de AWS CLI e as armazena em sua base de dados. Daí, o Grafana acessa essas informações e exibe em seu painel.

Vale ressaltar que será necessário ter instalado o Zabbix e o Grafana, além de conhecimento nestas ferramentas para que a estrutura fique funcional. O resultado será o painel abaixo:

![](/img/Grafana.JPG)

## Diretórios:

### Grafana

* Contém o JSON do Dashboard e deve ser importado em seu Grafana.

### Zabbix

* zbx_export_templates.xml: arquivo de Template do Zabbix com os itens a serem coletados e de acordo com as configurações feitas no Grafana.
* userparameter_aws.conf:  arquivo de UserParameter utilizado pelo Zabbix Agent para coletar métricas da AWS.
* Contém uma imagem PNG de como se deve configurar um item dentro de um Host no Zabbix para buscar através do UserParameter.
