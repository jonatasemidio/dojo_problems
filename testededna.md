Teste de DNA
============

O apresentador Ratinho precisa criar um quadro em seu programa chamado de "Teste de DNA".
Esse quadro será responsável por identificar quem é o pai da criança apresentada.

Basicamente será apresentado uma criança e dois possíveis pais. Onde o Ratinho será o responsável por descobrir o pai original.
Para isso o DNA coletado de cada possível pai será comparado com o DNA coletado do filho.
As 3 sequências de DNS serão informadas ao sistema que retornará com quem é o Pai. 

Onde você será o responsável por contruir esse sistema seguindo as seguintes regras:

1 - O DNA com a maior pontuação (mais parecido) de compatibilidade será eleito o pai da vez;
Ex: Pai GILTERNEY = 'AACTG' | Pai ALAMORILDO = 'CATAG' Filho MINIOSVALDO = 'AATCG' => GILTERNEY é o Pai

2 - Somar todas as sequências identificadas.
Ex: Filho 'AATC': GILTERNEY = 'AA' + 'C' + 'T' + 'G' ou ALAMORILDO = 'C' + 'A' + 'T' + 'A' + 'G'

3 - A pontuação de cada sequência equivale a 2**<Ao número de caracteres identificados>
Ex: 
Filho 'AATC' 
GILTERNEY =  'AA' + 'C' + 'T' + 'G'      => 2**2 + 1**2 + 1**2  + 1**2       => 7
ALAMORILDO = 'C' + 'A' + 'T' + 'A' + 'G' => 1**2 + 1**2 + 1**2 + 1**2 + 1**2 => 5

Resultado GILTERNEY é o Pai
GILTERNEY  = AACTG
ALAMORILDO = CATAG
FILHO      = AATCG

Testes: quemeopai(GILTERNEY, ALAMORILDO, FILHO) == 'GILTERNEY'

Exemplo de Validação de Pontuação:
Filho:AAGGC Pai:AGACG  validação de pontos: 1**2 + 1**2 + 1**2 + 1**2 + 1**2 = Pontos: 5
Filho:AAGGC Pai:GGAAC  validação de pontos: 2**2 + 2**2 + 1**2               = Pontos: 9
Filho:AAGGC Pai:AAGCG  validação de pontos: 3**2 + 2**1 + 1**2               = Pontos: 12
Filho:AAGGC Pai:CAAGG  validação de pontos: 4**2 + 1**2                      = Pontos: 17
Filho:AAGGC Pai:AAGGC  validação de pontos: 5**2                             = Pontos: 25

No caso de empate retornar *CADIM*
