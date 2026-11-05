# Como discutir os projetos tecnicamente

[Voltar ao perfil](../README.md)

A evolução deste portfólio foi implementada com assistência de IA. Este documento descreve decisões e verificações existentes, para estudo e discussão; não inventa episódios de autoria manual ou experiências profissionais.

## Sales Analytics

**Escolha:** Python com biblioteca padrão e SQLite para executar sem serviço externo. Modelo dimensional para organizar as entidades; exportação desnormalizada para visualização.

**Decisão de negócio:** ticket por transação e receita por unidade têm denominadores diferentes. A versão revisada os distingue.

**Tratamento da lacuna:** só havia IDs de clientes na fato. A dimensão foi derivada desses IDs, sem fabricar nomes ou atributos.

**Verificação:** receita reconciliada com a entrada; rejeição de duplicidade, referência ausente e valores inválidos. Teste de reexecução sem duplicar linhas e preservação do banco anterior quando a entrada falha.

**Trade-off:** o dashboard envia 10 mil registros ao navegador. É viável para a demonstração, mas uma base grande pede agregações ou consulta no servidor. O banco usa REAL; aplicação financeira operacional pediria centavos inteiros ou tipo decimal.

[Decisões detalhadas](https://github.com/llfaraco/bi-end-to-end-sales-analytics/blob/main/docs/DECISIONS.md)

## Churn exploratório

**Escolha:** descrever uma amostra de 20 registros com contagem por grupo, em vez de transformá-la em uma afirmação geral sobre clientes.

**Verificação:** alvo binário, IDs únicos e dados obrigatórios presentes. Células do notebook executadas sequencialmente em Python, com saídas registradas.

**Discussão:** associação não implica causalidade. Grupos pequenos exigem cautela e não justificam estimativa de efeito de uma ação.

## Churn preditivo

**Escolha:** teste separado e estratificado, pré-processamento ajustado somente no treino e comparação com baseline.

**Verificação:** IDs de treino e teste não se sobrepõem, e o arquivo de scores contém apenas o teste.

**Discussão:** o alvo sintético depende das próprias variáveis. O resultado demonstra um experimento de aprendizado, não capacidade comprovada de prever cancelamentos reais.

## Vacinação

**Escolha:** preservar ausência e ordenar por país e data antes da janela temporal de sete dias.

**Verificação:** fixture com lacuna maior que sete dias e grupo sem reporte, além de carga SQL com nulos preservados.

**Discussão:** sete registros não são necessariamente sete dias. Dados acumulados também podem sofrer revisões e conter agregados territoriais.

## Perguntas para preparar uma entrevista

- Consigo explicar o grão de cada tabela e reconstruir um indicador com uma consulta?
- Sei mostrar qual entrada provoca uma falha de qualidade e por quê?
- Consigo mudar uma regra, executar os testes e interpretar o efeito?
- Sei distinguir o que defini como produto, o que foi implementado com IA e o que validei pessoalmente?
- Consigo apresentar uma limitação e uma alternativa técnica sem prometer algo que não medi?

O código e os testes são material para praticar essas respostas. Eles não substituem o entendimento do autor sobre cada entrega.
