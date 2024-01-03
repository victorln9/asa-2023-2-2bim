# DNS

## Instalação
Primeiro: Instalar o *Bind9*
  $ apt-get update
  $ apt-get install bind9

## Configuração
Primeiro: Configurar o arquivo *Interfaces*
  $ nano /etc/network/interfaces

Incluir o(s) nome(s) e o conteúdo do(s) arquivo(s) de configuração.

Cinco registros (4 pontos cada):

- 3 do tipo A (Endereços);
- 2 do tipo CNAME (`www` e `docs`);

## Teste


