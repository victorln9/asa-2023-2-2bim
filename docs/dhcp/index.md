# DHCP

## Instalação
Primeiro: instalar o **Dnsmasq**

$apt install dnsmasq


## Configuração
Primeiro: Configurar o arquivo

$nano /etc/dnsmasq.d/asa.conf
![Alt text](<fotos_dhcp/Dnsmasq CONFIGURADO.png>)

Segundo: Configurar a Interface de redes

$nano /etc/network/interfaces
![Alt text](<fotos_dhcp/configuração interface-dhcp.png>)

REINICIAR INTERFACE

$ifdown eth1

$ifup eth1

Terceiro: restart nos serviços

$/etc/init.d/dnsmasq restart

$/etc/init.d/networking restart

## Configuração no Windowns
![Alt text](<fotos_dhcp/CONF WIN DHCP.png>)

## Teste

$ipconfig
![Alt text](fotos_dhcp/TESTE-DHCP-ifconfig.png)

$ipconfig /all
![Alt text](<fotos_dhcp/DHCP-ipconfig all.png>)


<Incluir o(s) nome(s) e o conteúdo do(s) arquivo(s) de configuração>

<Distribuir um intervalo (*range* em inglês) de endereços IP; (15 pontos)>
<Reservar 2 endereços (IP fixo) fora do intervalo do item anterior. (5 pontos)>

