# Malha Municipal GeoJSON do Rio Grande do Norte (RN) com Territórios

Este repositório fornece um arquivo GeoJSON otimizado contendo os polígonos dos 167 municípios do Rio Grande do Norte.

O diferencial deste projeto é a **atualização dos nomes** dos municípios e a **inclusão da propriedade `territorio`** (baseada nos Territórios da Cidadania/SEPLAN-RN), permitindo análises de dados e visualizações agrupadas por região.

Este projeto é um *fork* de [Geodata BR - Brasil](https://github.com/tbrugz/geodata-br), com foco na limpeza de dados e enriquecimento para análise territorial e urbanística.

## 🚀 Valor e Motivação

O objetivo é fornecer um arquivo de mapa (GeoJSON) "pronto para análise" (`analysis-ready`). Arquivos GeoJSON oficiais do IBGE são excelentes, mas muitas vezes precisam de tratamento:

1.  **Nomes Atualizados:** Os nomes dos municípios foram validados e corrigidos.
2.  **Territórios Inclusos:** A adição da chave `territorio` permite que pesquisadores, analistas de dados e urbanistas agrupem dados quantitativos (como demografia, saúde, economia) em uma escala regional (territorial) de forma imediata, sem a necessidade de arquivos de mapeamento (DE-PARA) separados.

## 💾 Esquema de Dados (Properties)

Cada *Feature* (município) no arquivo `rn_mun_territorios.json` contém as seguintes `properties`:

* `municipio`: (String) O nome oficial e atualizado do município.
* `territorio`: (String) O nome do território da cidadania ao qual o município pertence (ex: "Seridó", "Mato Grande", "Potengi").
* `cod_ibge`: (String) O código IBGE completo do município, com 7 dígitos (ex: "2400109").

## 🛠️ Como Usar (Exemplo com Python)

Este arquivo é ideal para uso com bibliotecas como `geopandas` em Python para criar mapas temáticos e análises quantitativas.

**Exemplo: Criar um mapa de dados agregados por Território**

Você precisará das bibliotecas `geopandas` e `pandas`.
```bash
pip install geopandas pandas matplotlib
