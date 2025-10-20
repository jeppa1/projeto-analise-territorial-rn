# Enriquecimento de Mapa GeoJSON do RN com Territórios da Cidadania

## Descrição do Projeto

Este repositório contém um script em Python (`.ipynb`) dedicado ao tratamento de um arquivo geoespacial (GeoJSON) dos 167 municípios do Rio Grande do Norte. O objetivo principal é **enriquecer o mapa adicionando a cada município sua respectiva classificação de "Território da Cidadania"**, além de corrigir e padronizar nomes de municípios.

O processo utiliza um arquivo CSV mestre como "dicionário" para realizar a junção dos dados e gerar um novo arquivo GeoJSON, otimizado e pronto para ser utilizado em ferramentas de visualização de dados, SIG (Sistemas de Informação Geográfica) e outras análises.

## Objetivo

O propósito deste projeto é fornecer um **mapa base atualizado e enriquecido do RN**, que possa servir como um recurso fundamental para análises de políticas públicas, estudos socioeconômicos e projetos de desenvolvimento regional.

## Estrutura dos Arquivos

```
.
├── README.md
├── enriquecer_mapa_rn_com_territorios.ipynb
└─── data/
     ├── input/
     │   ├── geojs-24-mun.json                  # Arquivo GeoJSON original
     │   └── municipios_rn_territorio... .csv   # Arquivo mestre com o mapeamento
     └── output/
         └── RN_MUNICIPIOS_TERRITORIOS... .json # Arquivo GeoJSON final e enriquecido
```

* **`data/input/`**: Contém os arquivos brutos necessários para rodar o script.
* **`data/output/`**: Contém o resultado final gerado pelo notebook.
* **`enriquecer_mapa_rn_com_territorios.ipynb`**: Notebook Jupyter com todo o passo a passo do processo.

## Metodologia

1.  **Carregamento:** O script utiliza a biblioteca `GeoPandas` para carregar o mapa original e `Pandas` para carregar o arquivo mestre.
2.  **Junção (Merge):** Os dois conjuntos de dados são unidos utilizando o código IBGE do município como chave.
3.  **Enriquecimento e Limpeza:** A propriedade "territorio" é adicionada a cada município. As colunas são renomeadas e organizadas para maior clareza.
4.  **Otimização:** As geometrias dos polígonos são simplificadas para reduzir o tamanho do arquivo final sem perda significativa de detalhe visual.
5.  **Exportação:** O GeoDataFrame final é salvo como um novo arquivo GeoJSON.

## Como Utilizar

1.  Clone o repositório.
2.  Certifique-se de ter as bibliotecas `pandas` e `geopandas` instaladas.
3.  Execute o notebook `enriquecer_mapa_rn_com_territorios.ipynb`. O script irá gerar o arquivo final na pasta `data/output/`.

---
**Autor:** Seu Nome