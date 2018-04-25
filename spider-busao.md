
Spider-busão 
============

![img](/resources/spider.jpg)
 
Historinha:
-----------
Mary Jane convida Peter Parker para conhecer um sitio de uma amiga de infância em uma cidade no interior de minas gerais (Carangola), Brasil. Devido suas responsabilidades, Peter se vê tendo que ir um dia depois, e ao chegar  na rodoviária principal se depara com uma cidade que não possui os prédio que seriam usados para locomoção com ajuda de suas teias. O problema é Peter esta  com dinheiro contado e se vê na necessidade de fazer o caminho mais econômico usando o sistema de ônibus transporte publico da cidade.
 
Regras do transporte publico:
-----------------------------
1. Ao chegar na estação principal você recebe e recarrega um cartão para o transporte publico.
2. Você pode pegar vários ônibus com o mesmo cartão e a tarifa do próximo é sempre o valor dela menos o seu gasto atual acumulado, onde no caso de resultado negativo a tarifa é zero

Problema:
---------
Dado as estações, suas conexões, seus valores e o valor de recarga do cartão do Homem aranha - Diga se será possível ele encontrar a Mary Jane no Sitio de Carangola.

---
Legenda da entrada:
primeiro parâmetro é -> 1 inteiro que faz referencia ao valor de recarga do Homem aranha
os próximos são as conexões compostas por 3 inteiros (estação inicial, estação final e valor da tarifa entre ambas)

---

* Ex1:
```python
#entrada
5
1 2 5
2 3 5
#saída: Chegou!
#OBS: Foi possível chegar pois a primeira estação deu 5 reais e na segunda o calculo foi 5 - 5 = 0. Logo não foi cobrada taxa.
```
* Ex2:
```python
#entrada
10
1 2 10
2 3 5
#saída: Chegou
#OBS: Foi possível pois o total deu 10. Já que a primeira foi 10 e a segunda o calculo (5 - 10) deu negativo, isentando o homem aranha da tarifa.
```
* Ex3:
```python
#entrada:
25
1 2 20
1 3 10
2 4 10
2 5 25
4 6 25
5 6 27
3 6 30

#saída: Chegou! na "Maria Jane"
#OBS: O total gasto foi 25 dinheiro pelo seguinte trajeto (1 -> 2 -> 4 -> 6). Calculo (20 + (10 - 20 = - 10 ou seja fica isento) + (25 - 20 = 5) ) = 25
```
