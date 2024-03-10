
# VS Code - Create Extension


## Instalar codigo Yo Code

Para instalar os pacotes temos de ter o instalador NPM

aceder ao link https://nodejs.org/en/download/ e instalar o pacote.

Reiniciar a máquina para ter efeito na linha de comandos

Depois de instalar e a máquina ser reiniciada garantir o comando npm é reconhecido apresentado a versão instalada

        npm -v

Para instalar o **Yo Code** pode-se seguir os passos que estão na página https://vscode-docs.readthedocs.io/en/stable/tools/yocode/

Comandos:

        npm install -g yo generator-code

Resultado:

        added 1041 packages in 1m

        145 packages are looking for funding
        run `npm fund` for details
        npm notice
        npm notice New minor version of npm available! 10.2.4 -> 10.4.0
        npm notice Changelog: https://github.com/npm/cli/releases/tag/v10.4.0
        npm notice Run npm install -g npm@10.4.0 to update!
        npm notice

##  Correr Yo Code

Comando:

        yo code

Se for apresentada a seguinte mensagem de erro


Abrir o Power Shell Console e excutar

        C:\> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

Mensagem a pedir confirmação:

        Execution Policy Change
        The execution policy helps protect you from scripts that you do not trust. Changing the execution policy might expose
        you to the security risks described in the about_Execution_Policies help topic at
        https:/go.microsoft.com/fwlink/?LinkID=135170. Do you want to change the execution policy?
        [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y

Voltar a executar o comando **Yo Code**

##  Iniciar o desenvolvimento


Se aparecer o erro 

        Exception has occurred: Error: Cannot find module 'vscode'

Então executar a instalação do pacote vscode:

        npm install vscode

Se aparecer uma mensage que o ficheiro package.json 


## Executar para testar

Comando a executar para executar:

        npm run compile 

Se quisermos ter sempre o programa a correr executar o comando:

        npm run watch

Isto permite que o programa esteja sempre a correr e para testar basta fazer o reload da janela. 
