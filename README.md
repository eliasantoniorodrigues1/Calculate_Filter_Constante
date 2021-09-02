# Estudos básicos da Calculate - Constante x Filter

#### Exemplo Retorna uma Constante em todas as Linhas:
~~~
Planejado ADM = 
// Despresa o contexto de filtro que não seja ADM
// O desejado era 288 somente onde tinha ADM, não criar uma constante.
// Somente a linha do contexto do filtro deve ser considerado.
CALCULATE([Planejado], fDados[Gerência]="ADM")
~~~

#### Exemplo Retorna o calculo apenas na linha em que o contexto do filtro é atendido:
~~~
Planejado ADM Sem Constante = 
CALCULATE([Planejado],
// Retorna uma tabela já filtrada:
FILTER(fDados, fDados[Gerência]="ADM"))
~~~
