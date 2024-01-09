# DNS

## Instalação
Primeiro: instalar o **Bind9**

$apt-get update

$apt-get install bind9

Segundo: Configurar o arquivo *Interfaces*

$nano /etc/network/interfaces
![Alt text](<fotos dns/interfaces dns.png>)

Terceiro: Colocar VM em Internal Network

![Alt text](<fotos dns/internal.png>)

Quarto: Reiniciar o networking

$systemctl restart networking.service

Quinto: Trocar nome da maquina

$nano /etc/hostname

$init 6
## Configuração
Configurar o arquivo *named.conf.default-zones*

$nano /etc/bind/named.conf.default-zones

Primeiro: Adicionar zona
![Alt text](<fotos dns/adicionar zona.png>)
            apartir de: zone "leandro.com.br" {  OBS:falta um ; na penultima linha, depois de "leandro.com.br"

Segundo: Criar o Banco de dados

$cd /etc/bind

Copiar o arquivo "db.empty" para "db.leandro.com.br

$cp db.empty db.leandro.com.br 

Terceiro: Configurar Banco de dados

$nano db.leandro.com.br

![Alt text](<fotos dns/configurarr.png>)

Quarto: Apontar para o servidor

$nano /etc/resolv.conf

![Alt text](<fotos dns/apontar.png>)

## Configuração no Windowns

![Alt text](<fotos dns/xp apontar pro serve linux.png>)

desativar firewall do win
![Alt text](<fotos dns/desativar firewall do win.png>)


Comandos úteis: systemctl restart bind9,systemctl status bind9


Incluir o(s) nome(s) e o conteúdo do(s) arquivo(s) de configuração.

Cinco registros (4 pontos cada):

- 3 do tipo A (Endereços);
- 2 do tipo CNAME (`www` e `docs`);

## Teste

$ping ns1.leandro.com.br 
![Alt text](<fotos dns/teste ping.png>)




