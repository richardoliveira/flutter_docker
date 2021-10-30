## RODANDO FLUTTER EM CONTAINER

- Pré Requisitos:
[(Extensão VSCode) Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)

- Buildando e rodando o container docker
  Clique no icone do Remote Development e selecione (**Remote-Containers: Open Folder in Containe**)


- Para conectar um dispositivo físico rode os seguintes comandos na máquina host:
```shell
adb kill-server
```
Será possível apenas via wireless a conexão com o dispositivo físico, rode esses comandos (XXX.XXX.XXX.XXX corresponde ao ip do seu device na sua rede)
```shell
adb tcpip 5555
adb connect XXX.XXX.XXX.XXX:5555
adb devices
```
Depois rode no shell do container:
```shell
adb connect XXX.XXX.XXX.XXX:5555
adb devices
```
Você precisará aprovar a conexão no seu dispositivo físico e depois poderá desconectar do cabo de dados