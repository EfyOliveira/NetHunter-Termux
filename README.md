# NetHunter-Termux
NetHunter para dispositivos não roteador (raiz)

![alt text](https://www.kali.org/docs/nethunter/nethunter-rootless/010-NH-Rootless-Installation_Start_s.png)

![alt text](https://www.kali.org/docs/nethunter/nethunter-rootless/020-NH-Rootless-KeX_s.png)

# Pré-requisito:
Dispositivo Android (dispositivo não modificado de estoque, sem necessidade de root ou recuperação personalizada)

Instale o Kali NetHunter em qualquer dispositivo Android sem root sem anular a garantia.

# Abra o terminal e digite

* `termux-setup-storage`

* `pkg install wget`

* `wget -O install-nethunter-termux https://offs.ec/2MceZWr`

* `chmod +x install-nethunter-termux`

* `./install-nethunter-termux`

# OBS: Após os procedimentos acima serem concluídos, você já pode usar o sistema NetHunter

Execute `sudo apt update && sudo apt full-upgrade -y` a primeira coisa após a instalação para atualizar o Kali . Se você tiver muito espaço de armazenamento disponível, talvez queira executar `sudo apt install -y kali-linux-default` também.
Todas as ferramentas de teste de penetração devem funcionar, mas algumas podem ter restrições, por exemplo, o metasploit funciona, mas não tem suporte a banco de dados.
Alguns utilitários como “top” não rodam em telefones sem root.
Usuários não root ainda têm acesso root no chroot. Isso é uma coisa proot. Apenas esteja ciente disso.
Os telefones Galaxy podem impedir que usuários não root usem o sudo. Basta usar “su -c” em vez disso.
Execute backups regulares de seus rootfs parando todas as sessões do nethunter e digitando o seguinte em uma sessão termux: tar -cJf kali-arm64.tar.xz kali-arm64 && mv kali-arm64.tar.xz storage/downloads Isso colocará o backup na pasta de download do Android. Nota: em dispositivos mais antigos, altere “arm64” para “armhf”


Comandos abaixo para te ajudar a ultilizar...

Abra o Termux e digite um dos seguintes:

Comandos:

* `nethunter`	iniciar a interface de linha de comando do Kali NetHunter

* `nethunter kex passwd`	configurar a senha KeX (necessária apenas antes do 1º uso)

* `nethunter kex &`	iniciar sessões de usuário do Kali NetHunter Desktop Experience

* `nethunter kex stop` parar a experiência de desktop Kali NetHunter

* `nethunter <command>`	correem ambiente NetHunter

* `nethunter -r`	inicie o Kali NetHunter cli como root

* `nethunter -r kex passwd`	configurar a senha do KeX para root

* `nethunter -r kex &`	inicie o Kali NetHunter Desktop Experience como root

* `nethunter -r kex stop`	interrompa as sessões raiz do Kali NetHunter Desktop Experience

* `nethunter -r kex kill`	Mate todas as sessões do KeX

* `nethunter -r <command>`	executado <command>no ambiente NetHunter como root


Nota: O comando `nethunter` pode ser abreviado para `nh`. Dica: Se você executar o kex em segundo plano ( &) sem ter definido uma senha, traga-o de volta ao primeiro plano primeiro quando solicitado a inserir a senha, ou seja, via `fg <job id>` - você pode enviá-lo para o segundo plano novamente via `Ctrl + zebg <job id>`

Para usar o KeX, inicie o cliente KeX, digite sua senha e clique em conectar Dica: para uma melhor experiência de visualização, insira uma resolução personalizada em “Configurações avançadas” no cliente KeX

