# check_conectividade
Checando conectividade numa e verificando sistema operacional

Depndencias: Sistema GNU/linux

Exemplo de execução:

$ /path/script  sub-rede e numeros de hosts:
							 	
	path/check_host.py  10.27.15.0     20 

Para  multiplas sub-redes separar com "-" :	
					    		
	$ path/check_host.py	        10.27.15.0-10.27.14.0                        20-10

Retorno:
lista  com o status de cada host (0 -Off, 1 -On) e sistema operacional detctado:
	
	$ /path/check_host.py  192.168.25.0-192.168.10.0  10-20
 
192.168.25.0-> 0-0/1-Linux/1-desconhecido/1-desconhecido/1-desconhecido/1-Linux/0-0/0-0/1-Microsoft/1-Linux/0-0
192.168.10.0-> 0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0/0-0

	
	
	
ordem representam hosts na forma:
posição 1 = 10.27.15.1
posição 2 = 10.27.15.2

Exemplo, considere a saida para o teste na rede 10.27.10.0 com 5 hosts :
	0-0/1-Linux/0-0/0-0/0-0

Apenas o host de ip 10.27.10.1 está online executando Linux como s.o.

Obs: Os sistemas são detctado atraves do nmap, se o mesmo não encontrar nenhuma combinação, a saida será desconhecido. 

