# check_conectividade
Checando conectividade numa rede de forma paralela

Exemplo de execução:

script subrede/lista de subredes numeros de hosts em cada subrede:
							 sub-rede	   Nºde hosts
	path/thread_check_ip.py  10.27.15.0     20 

Para teste de multiplas redes:	
							    lista de sub-redes separadas por "-"               Nºde hosts de cada redde separado por "-" 
	path/thread_check_ip.py	        10.27.15.0-10.27.14.0                                20-10

Retorno:
lista com com status de cada host (0 -Off, 1 -On):
	1 ate Nº de hosts
	0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0-0

posições representados hosts na forma:
posição 1 = 10.27.15.1
posição 2 = 10.27.15.2

Exemplo, considere a saida para o teste na rede 10.27.10.0 com 5 hosts :
	1-0-0-0-1

Apenas o host de ip 10.27.0.1 e o host de ip 10.27.10.5 estão On.

