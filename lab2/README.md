# Lab 2
Tarefas do laboratório 2 - Renato César Alves de Oliveira

## Tarefa sobre catálogo de componentes
[Notebook Tarefa Componentes](https://github.com/renato2808/inf331/blob/master/lab2/components-01-catalog.ipynb)

## Tarefa Web Components 1
~~~html
<dcc-trigger label="Mundo P"
             action="world/politics"
             value="Israel chega a acordo para normalizar relações com Emirados Árabes e suspende anexação de áreas na Cisjordânia
O presidente dos EUA, Donald Trump, ajudou a intermediar. Benjamin Netanyahu, premiê de Israel, disse no entanto que a anexação de territórios continua em estudo.">
</dcc-trigger>

<dcc-trigger label="Brasil P"
             action="brazil/politics"
             value="China diz que detectou coronavírus em frango importado do Brasil
Importações estão mantidas, e autoridades recomendam cuidados no preparo dos alimentos. Ministério da Agricultura disse que alimentos são seguros">
</dcc-trigger>

<dcc-trigger label="Brasil E"
             action="brazil/sports"
             value="O São Paulo homenageou Rogério Ceni com um vídeo, transmitido nos telões do Morumbi, antes do duelo contra o Fortaleza, pela segunda rodada do Campeonato Brasileiro. O treinador da equipe cearense esteve no estádio pela primeira vez após deixar o Tricolor paulista, em 2017.">
</dcc-trigger>

<dcc-trigger label="Bahia"
             action="bahia/sports"
             value="Bahia negocia empréstimo de Caio Mello e Jaques para o Joinville
Jogadores integraram elenco B que disputou o Campeonato Baiano no início do ano">
</dcc-trigger>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="doctor"
                 speech="Noticias de Política: ">
  <subscribe-dcc topic="world/politics"></subscribe-dcc>
  <subscribe-dcc topic="brazil/politics"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="nurse"
                 duration="0s"
                 character="nurse"
                 speech="Noticias do Brasil: ">
  <subscribe-dcc topic="brazil/politics"></subscribe-dcc>
  <subscribe-dcc topic="brazil/sports"></subscribe-dcc>
  <subscribe-dcc topic="bahia/sports"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="patient"
                 duration="0s"
                 character="patient"
                 speech="Noticias: ">
  <subscribe-dcc topic="world/politics"></subscribe-dcc>
  <subscribe-dcc topic="brazil/politics"></subscribe-dcc>
  <subscribe-dcc topic="brazil/sports"></subscribe-dcc>
  <subscribe-dcc topic="bahia/sports"></subscribe-dcc>
</dcc-lively-talk>
~~~

## Tarefa Web Components 2
~~~html
<dcc-trigger label="Next Item" action="next/rss">
</dcc-trigger>

<dcc-rss publish="rss/science" source="https://www.wired.com/category/science/feed">
  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-rss publish="rss/design" source="https://www.wired.com/category/design/feed">
  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-aggregator publish="aggregate/science" quantity="3">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-aggregator>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="doctor"
                 speech="Noticias Agregadas de Ciencia: ">
  <subscribe-dcc topic="aggregate/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="nurse"
                 duration="0s"
                 character="nurse"
                 speech="Noticias de Ciência: ">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="patient"
                 duration="0s"
                 character="patient"
                 speech="Noticias de Design: ">
  <subscribe-dcc topic="rss/design"></subscribe-dcc>
</dcc-lively-talk>
~~~