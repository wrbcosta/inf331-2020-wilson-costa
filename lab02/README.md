# Tarefa sobre catálogo de componentes

Download do arquivo do notebook com a resolução das seis tarefas: 

# Tarefa Web Components 1

~~~html
<dcc-trigger label="Mundo" action="noticia/mundo/politica"
             value="Sai resultado das pesquisas eleitorais nos EUA"></dcc-trigger>
<dcc-trigger label="Brasil P" action="noticia/brasil/politica"
             value="Veja tramitação de novo projeto de lei na câmara em Brasília"></dcc-trigger>
<dcc-trigger label="Brasil E" action="noticia/brasil/esporte"
             value="Nova escalação da seleção brasileira é definida"></dcc-trigger>
<dcc-trigger label="Bahia" action="noticia/bahia/esporte"
             value="Bahia ganha de 3x1 sobre o Vitória"></dcc-trigger>

<dcc-lively-talk id="doctor" duration="0s" character="doctor" speech="">
  <subscribe-dcc topic="noticia/+/politica"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk id="nurse" duration="0s" character="nurse" speech="">
  <subscribe-dcc topic="noticia/brasil/+"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk id="patient" duration="0s" character="patient" speech="">
  <subscribe-dcc topic="#"></subscribe-dcc>
</dcc-lively-talk>
~~~

# Tarefa Web Components 2

~~~html
<dcc-trigger label="Ciência" action="botao/ciencia"></dcc-trigger>
<dcc-trigger label="Design" action="botao/design"></dcc-trigger>

<dcc-rss source="https://www.wired.com/category/science/feed" publish="rss/ciencia">
  <subscribe-dcc topic="botao/ciencia" role="step"></subscribe-dcc>
</dcc-rss>
<dcc-rss source="https://www.wired.com/category/design/feed" publish="rss/design">
  <subscribe-dcc topic="botao/design" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-aggregator publish="agregado/ciencia" quantity="2">
  <subscribe-dcc topic="rss/ciencia"></subscribe-dcc>
</dcc-aggregator>

<dcc-lively-talk id="doctor" duration="0s" character="doctor" speech="">
  <subscribe-dcc topic="agregado/ciencia"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk id="nurse" duration="0s" character="nurse" speech="">
  <subscribe-dcc topic="rss/ciencia"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk id="patient" duration="0s" character="patient" speech="">
  <subscribe-dcc topic="rss/design"></subscribe-dcc>
</dcc-lively-talk>
~~~
