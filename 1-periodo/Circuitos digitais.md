# Materiais
[Material em video](https://www.youtube.com/playlist?list=PLXyWBo_coJnMYO9Na3t-oYsc2X4kPJBWf)
Livros:
- [Sistemas digitais: princípios e aplicações](https://plataforma.bvirtual.com.br/Leitor/Publicacao/168497/pdf/0?code=/bIOZcTOMUCKJbiikNEXeeOXmDi+XXDxeQpoSNep5EqGr4iepjXiaJ3LRwEBTq8i+2jerKw2CvChZOSp64BHBA==)
- [[Organização estruturada de computadores - Tanenbaum.pdf]]
- [[Sistemas digitais - Fundamentos e aplicacoes - Floyd Thomas.pdf]]
# Anotações
## Aula 01 - Introdução à circuitos digitais
### Circuitos digitais X Circuitos analógicos
- Circuito analógico - Assume valores infinitos de amplitude, cujas entradas e saídas são sinais analógicos
- Circuito digital - Assume valores finitos de amplitude, cuja entradas e saídas são sinais digitais

- Onde podemos encontrar circuitos digitais?
	- Computadores
	- Chips internos
	- Câmeras digitais
	- Video-games
	- Dispositivos médicos
- Os mais comuns são aqueles que arrumem apenas dois valores:
	- 1 ou 0, sendo 1 o nível lógico ALTO (ou Ligado) e 0 o nível lógico BAIXO (ou Desligado)
	- Ou seja, sinais binários
	- Os sinais devem ser representados em uma forma de onda de tensão
### Vantagens dos circuitos digitais
- Mais fáceis de projetar
- Armazenamento da informação é feita de forma mais simples
- São mais precisos
- Mais imunes a ruidos que os analógicos
- Mais versáteis
- Costumam ser mais baratos que os analógicos
- Permitem a utilização de técnicas avançadas de processamento digital de sinais
### Conversão analógico-digital (A/D)
- A maioria dos sinais encontrados na natureza são analógicos
- Circuitos digitais processam apenas sinais digitais
- Composta em 3 etapas
	- Amostragem: Amostrar o sinal analógico
	- Quantização: Quantizar as amostras
	- Codificação: Converter as amostrar quantizadas em um sinal binário
- Muitas vezes os sistemas necessitam que suas saidas sejam analógicas
### Conversão digital-analógica (D/A)
- Uma onda digital é convertida em equivalente analógica

- Os sistemas de conversão trabalham juntos
## Aula 02 - Sistemas de numeração (Parte 01)
- Número - forma de representação de quantidades
- Sistema de numeração - Conjunto de simbolos para representar números
### Base do sistema
- Indica a quantidade de dígitos que um sistema possui
- Base exponencial do peso de cada dígito para a composição do número

- Sistemas de numeração comuns
	- Decimal
	- Binário
	- Hexadecimal

- Regra geral de formação:
$$
d = dígito / b = base
$$
$$
N = (d_n \cdot b^n ) + (d_{n-1} \cdot b^{n-1} ) + ... + (d_1 \cdot b^1 ) + (d_0 \cdot b^0 ) + (d_{-1} \cdot b^{-1} ) + (d_{-2} \cdot b^{-2} ) + ...
$$
### Sistema decimal
- Possui 10 dígitos possíveis

Exemplo:
$$
47932 = (4 \cdot 10⁴) + (7 \cdot 10³) + (9 \cdot 10²) + (3 \cdot 10¹) + (2 \cdot 10⁰)
$$
$$
47932 = 40.000 + 7.000 + 900 + 30 + 2
$$
- Contagem no sistema decimal de numeração
### Sistema binário
- Base 2
- Para não acontecer confusão é necessário indicar o sistema de numeração subscrito
- O dígito binário chama "Bit"
- 8 bits = Byte
- Sistema de valor posicional
- O bit com menor peso posicional chamará LSB e o bit com maior peso posicional será o MSB 
#### Conversões
- Sistema binário para decimal
	- Apenas aplica a regra geral 
- Sistema decimal para binário
	- Soma ponderada
		- Encontra a somatória de base 2 que representa o valor no decimal 
		- Completa as lacunas de posições com 0
	- Métodos da divisão sucessiva por 2
		- Dividir o número por 2 e guardar o Quociente(Q) e o Resto(R)
		- Continue dividindo o quociente e guardando os restos até que Q=0
		- Quando Q-0, o número convertido é formado pelos restos
			- O primeiro resto é o LSB e o ultimo resto é o MSB
## Aula 03 - Sistemas de numeração (Parte 02)
### Sistema Hexadecimal
- Base 16
	- 0123456789ABCDEF
- Cada digito hexadecimal é codificado em exatamente 4 bits
#### Conversões
- Hexadecimal-decimal
	- Aplica a regra geral
- Hexadecimal-binário
	- Converte digito por digito em bits
- Binário-hexadecimal
	- Separa o numero binário em grupos de 4 bits 
	- Realiza a equivalência de digitos pra bits
- Decimal-Hexadecial
	- Divisão consecutiva por 16
	- Conversão decimal -> binário -> hexadecimal
## Aula 05 - Código binário
- Código -> Representação de números, letras, palavras, estágios, etc por um grupo especial de simbolos
- Quando descrevemos uma informação com bits, é considerado um código binário
- Codificação -> Atribuir valores de códigos para cada informação
- É necessário atribuir à essas informações a menor cadeia de bits possível
- Seja N a quantidade de elementos a serem codificados, a quantidade mínima de bits será:
 $$
L = [\log_{2}(N)]
$$
$$
2^L \geq (N) 
$$
[Relembrando logarítmo](https://www.todamateria.com.br/logaritmo/)
- Nada impede de usar mais bits, porém é uma boa prática usar a menor quantidade de bits possíveis
- Códigos de largura mínima
- Existem diversos padrões de códigos como:
	- Código BCD (Binary-Coded Decimal Code)
	- Código Gray (Código Reflexivo)
	- Código one-hot
	- Código Johnson
	- Código Excesso 3
	- Código ASCII
### Código BCD
- Cada dígito decimal vai ser representado pelo seu equivalente binário
- Converte cada dígito para binário 
- Possui 4 bits para cada digito
### Código Gray
- Código não posicional
- Não é possível fazer funções aritméticas com dados gray
- Apresenta uma mudança de um único bit quando se passa de uma palavra do código para a seguinte
- Pode ter qualquer número de bits
- Copio o código anterior, adiciono um 0 na frente, depois adiciono 1 na próxima e copio no inverso
### Código one-hot
- Código não posicional
- Não é um código de largura mínima
- Apenas um dos bits terá valor 1
### Código Johnson
- Código não posicional
- Código é montado adicionando um 1 na sequência até completar todo o código e depois adiciona o 0 até sobrar apenas um 1
### Código Excesso 3
- Conversão de decimal para binário, somando-se ao resultado 3 unidades
### Código ASCII
- Código alfanumérico
- American Standard Code for Information Interchange
- Tem 128 caracteres e simbolos
- Contém 7 bits
- 32 primeiros são caracteres de controle
- Possui símbolos gráficos
#### Código ASCII estendido
- Código de 8 bits
- 256 dígito
- Inclui caracteres estrangeiros
- Símbolos de moeda estrangeira entre outros símbolos
## Aula 06 - Aritmética binária
### Adição
- Regras da adição:
	- 0+0 = 0
	- 0+1 = 1
	- 1+0 = 1
	- 1+1 = 0 e transporta 1 para próxima posição 
### Subtração
- Regras da adição:
- 0-0=0
- 0-1=1 com empréstimo de 1
- 1-0=1
- 1-1=0
### Multiplicação
- 0x0=0
- 0x1=0
- 1x0=0
- 1x1=1
### Divisão
- Da nem pra explicar, olha no caderno da jinx
- 