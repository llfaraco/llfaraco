# Guia do portfólio

[Voltar ao perfil](../README.md)

## Como ler os projetos

O portfólio reúne entregas profissionais descritas sem material interno, um produto com código privado e exercícios públicos de desenvolvimento técnico.

| Categoria | Evidência | Limite |
| --- | --- | --- |
| [Casos de aplicação](experiencia-profissional.md) | Contexto, entregas e responsabilidades informados pelo autor | Sem bases ou código de empresas |
| [Yardline](yardline.md) | Produto público e estudo de caso de produto | Código privado; sem métricas de impacto declaradas |
| Projetos públicos de estudo | Arquivos, scripts, consultas e notebooks versionados | Simulações e exercícios não equivalem a experiência em produção |

## Situação observada nos arquivos

- **Sales Analytics:** há CSVs, definição de tabelas SQLite e medidas DAX. Não há arquivo de dashboard Power BI; a dimensão de clientes prevista no SQL não tem CSV correspondente.
- **Vacinação global:** o Python trata um CSV e exporta outro. A modelagem SQL é separada; o script não carrega automaticamente as tabelas.
- **Churn exploratório:** há notebook, base e imagens. O notebook não contém saídas executadas e a formatação das células precisa ser validada para reprodução.
- **Churn preditivo:** o Python gera 500 clientes sintéticos e treina regressão logística. A consulta SQL é conceitual e não alimenta automaticamente o script.
- **SQL Hero Strategy:** exercício de agregação com dados fictícios. O arquivo de consulta tem um ponto adicional no nome, documentado no README.
- **Tom Brady:** exercício com dados definidos manualmente. Listas de tamanhos diferentes impedem a criação do DataFrame; a execução precisa ser corrigida antes de apresentar resultados.
- **ARES Performance:** aplicação React/Vite com integração Supabase e registros de treino e métricas. Build, autenticação e persistência não foram validados nesta revisão.
- **Python para Não Programadores:** material de curso do LinkedIn Learning; autoria original preservada.

Esta revisão verificou estrutura e conteúdo dos arquivos. Não equivale à execução dos projetos ou à validação dos resultados analíticos.

## Critério de apresentação

Descrever o problema, mostrar o que está no repositório, informar como reproduzir e registrar limitações. Planos futuros não são apresentados como implementações concluídas.

## Contato

[LinkedIn](https://www.linkedin.com/in/lucasrfaraco) · [E-mail](mailto:lucas.rfaraco@gmail.com)
