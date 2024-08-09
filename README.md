# DEPLOY DO SITE
## https://neurodata.onrender.com

# Sobre
Este é o Repositório tanto da Análise quanto do Website do nosso Trabalho de PI

Onde foi desenvolvido um estudo com base na Database Psicossocial do Datasus

 A NeuroData surgiu a partir da disciplina de Projeto Integrador: Ciência de Dados e Analytics, da Universidade Regional do Noroeste do Estado do Rio Grande do Sul - Unijuí. O Projeto foi desenvolvido por estudantes do 5º módulo dos cursos de Ciência da Computação e de Jornalismo.

A partir das demandas da Secretaria de Saúde do município de Ijuí, o grupo desenvolveu uma análise sobre o cenário psicossocial da população ijuiense. Para isso, foram utilizadas as bases de dados dos atendimentos realizados pelos Centros de Atenção Psicossocial (CAPS) da cidade, disponibilizadas pelo DATASUS.

O objetivo final deste projeto é apresentar às pessoas dados relacionados à saúde mental de uma forma acessível e de fácil compreensão. Além disso, as entrevistas com especialistas desta área foram realizadas para trazer embasamento teórico de pessoas que possuem experiência de atuação na promoção da saúde mental. 

# Adquirindo os Dados Brutos
> **Requisitos:** python3, wget e unzip.

Começe criando dois diretórios para armazenar os arquivos que serão baixados do DataSus, um para as bases principais e outro para as bases auxiliares:
```sh
$ mkdir data
$ mkdir data/aux
```
Agora use o utilitário **susgrep.sh** para fazer o download de todas as bases de dados necessárias para o SusCube:
```sh
$ ./susgrep.sh data data/aux
```
> A conversão dos arquivos baixados para formatos úteis (como .dbc para .dbf e .cnv para .csv) será feita automaticamente durante a execução do script.

> **Erros comuns:**
> Pacote unzip não está instalado no sistema
> WSL não reconhece cnv2csv
