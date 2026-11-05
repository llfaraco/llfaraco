# Guia do portfólio e evidências

[Voltar ao perfil](../README.md) · [Decisões e aprendizado](decisoes-e-aprendizado.md)

## Projeto principal

[Sales Analytics](https://github.com/llfaraco/bi-end-to-end-sales-analytics) reúne um fluxo completo de CSV, validação em Python, modelo dimensional SQLite, consultas, indicadores e dashboard HTML com filtros. A integração com Power BI tem M, DAX e instruções; não há `.pbix` gerado neste ambiente.

## Validação local em 05/11/2026

| Projeto | Evidência disponível | Verificação local |
| --- | --- | --- |
| Sales Analytics | Dashboard, CSV mensal e relatório de hashes, totais e duração | 10 mil vendas processadas; 6 testes Python e verificação de filtros em Node |
| Churn exploratório | Resumo, gráficos, CSV por canal e notebook com saídas | 20 registros; 4 testes; 2 células executadas sequencialmente em Python |
| Churn preditivo | Métricas, baseline, coeficientes e scores de holdout | 500 registros sintéticos; 400 treino / 100 teste; 3 testes |
| Vacinação | Pipeline com janela temporal e carga dimensional SQLite | 4 testes com fixture; base original não executada localmente |
| Tom Brady | Resumo histórico com fonte e proporções calculadas | Script executado; 3 testes |
| SQL Hero Strategy | Consulta com nome corrigido e resultado verificado | 1 teste com SQLite em memória |
| ARES Performance | Aplicação React/Vite e integração Supabase | Build e fluxos não validados nesta revisão |

Foram aprovados **21 testes Python**, além da verificação de totais e filtros do dashboard em Node. [Registro da execução local](validation.json).

Os workflows acrescentados aos seis projetos executam verificações a cada push e pull request. As primeiras execuções remotas ficaram bloqueadas antes de iniciar os passos. A validação comprovada nesta revisão é local; não se declara aprovação no GitHub Actions. Os workflows ficam disponíveis para execução quando o impedimento da conta for resolvido.

## Produto com código privado

[Yardline](yardline.md): estudo de caso, [prévias públicas e roteiro de demonstração](yardline-demonstracao.md) e [visão conceitual das responsabilidades técnicas](yardline-visao-tecnica.md). A página pública foi observada; fluxos autenticados e acurácia das recomendações não foram testados nesta revisão.

## Casos de negócio

[Casos de aplicação](experiencia-profissional.md) descrevem problemas, entregas e responsabilidades informados pelo autor. Não incluem bases ou código internos de empresas.

## Como interpretar os resultados

- Bases de estudo e simulações não equivalem a impacto obtido em empresas.
- O alvo sintético do modelo de churn é construído por regra; a avaliação não comprova previsão de churn real.
- Tempo de execução é medido em uma máquina, sem constituir benchmark de desempenho.
- O material de curso Python para Não Programadores preserva a autoria original e é apresentado como estudo.
- A evolução do código, dos testes e da documentação foi implementada com assistência de IA, e está aberta à inspeção pelos arquivos e comandos de reprodução.

[LinkedIn](https://www.linkedin.com/in/lucasrfaraco) · [E-mail](mailto:lucas.rfaraco@gmail.com)
