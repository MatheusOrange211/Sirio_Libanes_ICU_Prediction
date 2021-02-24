# Sirio_Libanes_ICU_Prediction
Predição de UTI's necessárias para pacientes internados com COVID-19 no Hospital Sírio Libanês

<img src="https://github.com/MatheusOrange211/Sirio_Libanes_ICU_Prediction/raw/main/image/image_banner.jpg">

COMO ESTE PROJETO ESTÁ ORGANIZADO 📚:
---
Para entender melhor este projeto, leia os notebooks na seguinte ordem:

1 - Leia o Notebook [VISUALIZANDO DADOS](https://github.com/MatheusOrange211/Sirio_Libanes_ICU_Prediction/blob/main/Visualizando_os_dados_Sirio_Libanes.ipynb)<br>
2 - Leia o Notebook [MATHEUS NARANJO CORREA IMPLEMENTANDO OS MODELOS](https://github.com/MatheusOrange211/Sirio_Libanes_ICU_Prediction/blob/main/Matheus_Naranjo_Correa_Implementa%C3%A7%C3%A3o_de_Modelos.ipynb)
<br>
3 - Leia o Notebook [PIPELINE PROJETO](https://github.com/MatheusOrange211/Sirio_Libanes_ICU_Prediction/blob/main/Pipeline_projeto.ipynb)


Cada Notebook serve de implementação para entender melhor o conteúdo todo.



**PROBLEMA**
Conforme mostrado pela direção do Hospital Sírio Libanês no Kaggle([link para leitura](https://www.kaggle.com/S%C3%ADrio-Libanes/covid19)), 
apresentaremos abaixo uma proposta de solução para o seguinte problema:

> A pandemia da SARS-COVID-19 (popularmente conhecido como coronavírus), vem causando grandes estresses nos sistemas de saúdes globais. 
Países com alta taxa de desenvolvimento vêm sofrendo com a falta de leitos de Unidade de Terapia Intensiva (UTI) na internação de seus pacientes, 
levando equipes médicas a terem que aplicar métodos de escolha severos, dando prioridade para os mais idosos e graves. Contudo, tais métodos não auxiliam na resolução 
do problema dado a alta taxa de contaminação existente, consequência das ondas de infecção que vêm sendo causadas em um efeito de *onda* ao redor do mundo. <br>
Tal problema afeta também países emergentes e subdesenvolvidos, que geralmente já possuem sistemas de saúde superlotados, como no caso do Brasil. 
Infelizmente a superlotação e a falta de leitos já sobrecarregou sistemas de vários estados, 
como no caso do estado do Amazonas 
([link da matéria](https://g1.globo.com/am/amazonas/noticia/2021/01/14/secretario-de-saude-do-am-fala-que-estado-vive-colapso-do-plano-logistico.ghtml)), 
onde pacientes não estão mais conseguindo acesso a UTI, assim como não possuem equipamentos básicos para a manutenção de vida, como oxigênio. <br>
Com base nesses acontecimentos e até mesmo na prevenção de sobrecarga do sistema de saúde das redes privadas, o Hospital Sírio-Libanês,
 referência internacional em saúde, busca prevenir e até mesmo predizer, 
 com base em dados clínicos de seus pacientes, conforme forem sendo admitidos no ambiente hospitalar, 
 a necessidade ou não de internação nas UTIs nas próximas horas. A ideia por trás disso é conseguir desenvolver um modelo de aprendizagem de máquina, 
 conhecido com **Machine Learning**, que consiga auxiliar a junta médica a tomar decisões referentes a necessidade ou não de internação na UTI para aquele paciente, 
 usando as boas práticas de programação e respeitando a Lei Geral da Proteção de dados, conforme indica a lei federal Lei nº 13.709/2018.
 
 Em nosso conjunto de dados, temos a seguinte janela de dados, ou como é chamado no dataset, `WINDOW`:
 |WINDOW|DESCRIÇÃO|
|:---------:|:-----------------------------------:|
| 0-2	    |  From 0 to 2 hours of the admission |
| 2-4	    | From 2 to 4 hours of the admission  |
| 4-6	    |  From 4 to 6 hours of the admission |
| 6-12    |	From 6 to 12 hours of the admission |
| Above-12|     	Above 12 hours from admission |

 Como é alertado pelo próprio hospital:

> **OBSERVAÇÃO**: **Cuidado para NÃO usar os dados quando a variável de destino estiver presente, 
pois a ordem do evento é desconhecida (talvez o evento de destino tenha acontecido antes de os resultados serem obtidos). 
Eles foram mantidos lá para que possamos aumentar este conjunto de dados em outros resultados posteriormente.**
 
 
Informações referente aos dados:
---
* Foram limpos e ajustados para uma escala de -1 até 1.

* Dados disponíveis:
  * Informações demográficas do paciente (03)
  * Doenças anteriores agrupadas de pacientes (09)
  * Resultados de sangue (36)
  * Sinais vitais (06)

* No total, são 54 recursos, expandidos quando pertinentes à média, mediana, máximo, mínimo, dif e dif.

Fórmula Usada para os cálculos feitos pela equipe do sírio libanês:
<br>
<br>
<br>
<a href="https://www.codecogs.com/eqnedit.php?latex=\dpi{200}&space;diff&space;=&space;max&space;-&space;min" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dpi{200}&space;diff&space;=&space;max&space;-&space;min" title="diff = max - min" /></a>
<br>
<br>
<a href="https://www.codecogs.com/eqnedit.php?latex=\dpi{200}&space;\begin{equation}&space;diff&space;\space&space;Relativo&space;=&space;\frac{diff}{mediana}&space;\end{equation}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dpi{200}&space;\begin{equation}&space;diff&space;\space&space;Relativo&space;=&space;\frac{diff}{mediana}&space;\end{equation}" title="\begin{equation} diff \space Relativo = \frac{diff}{mediana} \end{equation}" /></a>


---
Este projeto foi minha primeira tentativa de trabalho com Machine Learning voltada para classificação de dados. Espero que possa lhe ajudar em alguma coisa.
Muito Obrigado ! 🚀🚀🚀
