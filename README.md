# Problema-2672-URI

Máscara de Rede

No protocolo IP (Internet Protocol) de endereçamento de rede, um endereço IP conta, também, com um número chamado "Máscara de Rede". A máscara de rede serve para que, dentro do universo de endereços IPs possíveis, uma rede seja isolada em um grupo fechado. Considere o seguinte endereço de rede: IP: 192.168.79.74 Máscara: 255.255.252.0.

O endereço em si é um endereço de 32 bits, que aqui separamos em 4 blocos de 8 bits para uma leitura mais fácil, o mesmo vale para o endereço da máscara. Vamos escrever estes endereços na forma binária:

IP:      11000000.10101000.01001111.01001010


Máscara: 11111111.11111111.11111100.00000000

Podemos ver que os primeiros 22 bits da máscara de rede são 1s, e os 10 bits restantes, são 0s. Muitas vezes este endereço é representado como: 192.168.79.74/22, por conta de seus 22 bits 1s da máscara de rede. Para este exemplo a rede exclusiva a qual este endereço pertence é definida pelos 22 primeiros bits do endereçamento, todas as máquinas pertencentes a esta rede tem nos seus primeiros 22 bits os mesmos valores. Cada máquina pertencente à rede irá utilizar cada um dos 10 bits finais para definir um endereço exclusivo para si mesmo. Neste caso, esta rede poderá definir 210 endereços para suas máquinas (na realidade 210 - 2, pois 2 deles são reservados), que vão desde: 11000000.10101000.01001100.00000000 (192.168.76.0) a 11000000.10101000.01001111.11111111 (192.168.79.255). Estes dois endereços específicos são reservados, o primeiro representa endereço da rede em si, e o último representa o endereço de broadcast, restando, portanto, 1022 endereços possíveis para cada uma das máquinas.

A você foi pedido que, a partir de um endereço IP com máscara (que pode ser em ambos formatos), apresente as informações da rede: seu endereço, endereço de broadcast e quantidade possível de máquinas na rede.

Entrada


A entrada contém vários casos de testes, cada caso de teste ocupa uma linha e representa um endereço IP e sua máscara de rede, podendo ser em dois formatos. Endereço e máscara na forma de 4 blocos de bytes com um espaço separando o IP e a máscara: "IP1.IP2.IP3.IP4 M1.M2.M3.M4" com 0 ≤ IP1,IP2,IP3,IP4,M1,M2,M3 ≤ 255 e 0 ≤ M4 ≤ 252, com a restrição de que o número formado pelos blocos da máscara de rede represente um número de 32 bits onde os bits 1s (todos) estão à esquerda dos bits 0s (todos); ou no formato "IP1.IP2.IP3.IP4/M", os mesmos limites impostos aos blocos do IP, e 0 ≤ M ≤ 30. Os casos de teste terminam com o fim das entradas.

Saída


Para cada caso de teste, a saída será apresentada em três linhas, a primeira linha contendo a frase: "Endereco de rede: " seguido do endereço da rede no formato de 4 blocos decimais; na segunda linha a frase: "Endereco de broadcast: " seguido do endereço de broadcast para a rede no formato de 4 blocos decimais; na terceira linha a frase: "Numero de maquinas: " seguido do número que representa a quantidade de endereços que podem ser atribuídos às máquinas desta rede. Após as três linhas impressas de um caso de teste deve ser impressa uma linha em branco, inclusive após o último caso de teste.
