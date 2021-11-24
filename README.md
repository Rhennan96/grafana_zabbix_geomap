# grafana_zabbix_geomap
Coleta de dados geográficos de Hosts do zabbix para o plugin geomap do grafana

1º Adicione a base de dados do Zabbix como datasource no grafana

![Alt text](/DataSource.png?raw=true)

2º Adicione um painel do tipo geomap

![Alt text](/painel_geomap.png?raw=true)

3º Selecione o datasource da base de dados e adicione a segunte query sql no painel


**SELECT h.name, location, location_lat, location_lon, site_country
FROM host_inventory as i, hosts as h 
WHERE i.hostid=h.hostid**


![Alt text](/query.png?raw=true)


4º Preencha o inventário dos hosts no zabbix com a latitude e longitude.

![Alt text](/coordenadas.png?raw=true)
