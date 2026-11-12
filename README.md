# Análise Exploratória do Mercado Imobiliário

## Objetivo do Projeto
Este projeto tem como objetivo realizar a limpeza, tratamento e análise exploratória de uma base de dados de aluguéis de imóveis. O foco principal é extrair insights valiosos que auxiliem na tomada de decisão de clientes em busca do melhor custo-benefício, traduzindo dados brutos em inteligência de negócio. 

## Ferramentas e Tecnologias
- **Python** (Linguagem principal)
- **Pandas** (Limpeza, manipulação e agregação de dados)
- **Google Colab** (Ambiente de desenvolvimento)

## Sobre os Dados
Os dados originais contêm informações sobre o mercado imobiliário, incluindo tipo de imóvel, bairro, área, valor do aluguel, condomínio e IPTU.
- **Fonte:** [Base de Dados - Alura](https://raw.githubusercontent.com/alura-cursos/pandas-conhecendo-a-biblioteca/main/base-de-dados/aluguel.csv)
- **Registros iniciais:** 32960 linhas.
- **Registros após limpeza:** 19532 linhas.

## Etapas de Tratamento e Limpeza (Data Cleaning)
Para garantir a qualidade da análise, as seguintes regras de negócio foram aplicadas:
1. **Tratamento de Nulos:** Valores ausentes nas colunas `Condominio` e `IPTU` foram preenchidos com `0`.
2. **Remoção de Inconsistências:** Imóveis com o `Valor` de aluguel nulo foram removidos da base.
3. **Engenharia de Recursos (Feature Engineering):**
   - Criação da métrica `Valor_Bruto` (Aluguel + Condomínio + IPTU).
   - Criação da métrica `Valor_m2` (Valor / Area).
   - Classificação dos imóveis em **Alto Padrão** e **Padrão** com base na média global do mercado.
4. **Filtro de Escopo:** A análise final foi restrita apenas a imóveis do tipo "Apartamento".

*Desenvolvido como parte do portfólio para posições de análise de dados, com foco em unir precisão técnica e atendimento às necessidades de negócio.*
