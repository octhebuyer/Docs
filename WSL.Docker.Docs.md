
# wSL


Listar várias versóes do Ubuntu online
	
	wsl --list --online

Instalar uma imagem

	wsl --install «NomeDaImagem»

Quando a máquina estiver a correr será possivel obter aceder via Windows Explorer

	\\wsl$\
	
Listar imagens instaladas

	wsl -l -v

Executar uma imagem Docker

	wsl -d «nome imagem»









# Docker - Commands

Estado do Docker

	docker stats

Para verificar as imagens baixadas:

	docker images


## Obter e instalar uma imagem do Microsoft SQL Server 2022 Express
 
 - Versão gratuita e leve do SQL Server
 - Ideal para desenvolvimento

Instalar
	docker pull mcr.microsoft.com/mssql/server:2022-latest


Executar

	docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=omdc123*#" \
	   -p 1433:1433 --name sql1 \
	   -d mcr.microsoft.com/mssql/server:2022-latest

Verificar se está execução:

	docker ps


Para validar que estamos realmente com a instancia ativa temos de conseguir aceder à BD
Para tal necessitamos de correr um cliente ou um sqlcmd. 
Neste caso vamos executar o **sqlcmd** que permite de uma maneira facil conexão:

	**Conectar ao bash do container**
	docker exec -it sql1 bash

	**Dentro do container, conectar ao SQL Server**
	/opt/mssql-tools/bin/sqlcmd -S localhost -U sa -P YourStrong@Passw0rd -C

	A opção **-C** permite fazer trust à ligação e evitar a instalação de um certificado
	


