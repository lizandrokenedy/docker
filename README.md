# docker
Configurações para xdebug VSCode

Instale a extensão Xdebug helper

https://chrome.google.com/webstore/detail/xdebug-helper/eadndfjplgieldjbigjakmdgkmoaaaoc

Acesse as configurações da extensão em IDE key, selecione Other e coloque o valor: VSCODE

No VSCODE, instale PHP Debuger, irá criar uma pasta .vscode dentro dela haverá um arquivo chamado .launch.json. Neste arquivo coloque as seguintes configurações

"configurations": [
    {
        "name": "Docker Xdebug VS",
        "type": "php",
        "request": "launch",
        "port": 9000,
        "pathMappings": {
            "/var/www/html": "${workspaceRoot}/html"
        },
    }

A variável ${workspaceRoot}, representa o diretório atual onde o VSCODE está aberto, caso seu projeto esteja em uma subpasta, acrestar ${workspaceRoot}/pasta_do_projeto.