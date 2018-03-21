Escudo anti-bruxas
==================

![img](/resources/bruxas.jpg)

Contexto:
---------
Você está com seus amigos andando em um bosque a procura de um lugar perfeito para fazer um picnic, mas vocês percebem que o lugar é amaldiçoado e tem uma bruxa se aproximando. Por sorte no meio dos alimentos vocês tem bastante sal ... mas será que esse sal é o suficiente para proteger a todos?

Problema:
---------
Dado um território e a posição das crianças, informe se a quantidade de sal que elas possuiem é o suficiente para protege-las.

Entrada:
--------
1. lista de crianças representada por lista de x e y (posição de cada criança no território)  
2. Quantidade de sal em Kg (Numero Inteiro)

Saída: 
------
se é possível ou não proteger as crianças.

![img](/resources/logica.jpg)

---
* OBS.1: o sal é representado em kg e cada kg faz um ponto (Ex: x0 até x1, x3 até x4 ou até y2 até y3)
* OBS.2: Apenas é possível utilizar o sal para norte, sul , leste e oeste. Não é possível fazer diagonais ou círculos.
* OBS3: O escudo de sal precisa sempre estar ao redor e não em cima da criança... Logo caso a criança esteja no (x3,y3) o sal precisará cercar este ponto percorrendo (2,2), (4,2), (4,4), (4,2), (2,2), on será necessário 8kg de sal para protege-la..

---

Curiosidade:
------------
Se você já assistiu [Abracadabra](https://www.imdb.com/title/tt0107120/) sabe que com sal você pode fazer um escudo anti-bruxas.

Testes:
-------
```python
test([(3, 3)], 8)
#entrada: [(3, 3)], 8
#saída: 'KIDS WINS'
#OBS: Com 8 kg de sal é possível é posível cobrir o redor da criança
```

```python
test([(3, 3)], 7)
#entrada: [(3, 3)], 7
#saída: 'BRUXA WINS'
#OBS: Faltou 1kg de sal para fechar o escudo. Logo a bruxa fez a festa.
```

```python
test([(3, 3), (3, 2)], 8)
#entrada: [(3, 3), (3, 2)], 8
#saída: 'BRUXA WINS'
#OBS: Não teve sal suficiente para fechar o escudo em volta das crianças. Logo a bruxa fez a festa.
```
```python
test([(3, 3), (3, 2)], 10)
#entrada: [(3, 3), (3, 2)],10
#saída: 'BRUXA WINS'
#OBS: Com 10 kg de sal é possível é posível cobrir o redor das crianças
```



