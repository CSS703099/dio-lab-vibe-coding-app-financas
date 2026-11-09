# Saldo Claro — Organização de finanças pessoais

Projeto conceitual para o desafio de Vibe Coding da DIO. O Saldo Claro reúne receitas, despesas e metas em um orçamento mensal. A proposta atende pessoas que anotam informações em lugares diferentes e precisam distinguir o saldo do mês do valor que sobra depois de reservar uma meta.

## Prompt final (PRD)

> Crie o Saldo Claro, protótipo responsivo em português para organizar o orçamento mensal. Público: pessoas que anotam receitas e despesas em lugares diferentes. Problema: visualizar saldo e planejar uma meta sem misturar previsão com dinheiro disponível. MVP: seleção do mês; CRUD de lançamentos com data, valor positivo em centavos, categoria e tipo; totais e gastos por categoria; meta mensal com valor-alvo e saldo restante; dados fictícios editáveis e armazenamento local. Separe saldo realizado, gastos e meta. Exemplo de aceite: receita R$ 3.000 e gastos R$ 2.200 geram saldo de R$ 800; meta R$ 500 deixa R$ 300 após a reserva. Se os gastos superarem as receitas, mostre o déficit e suspenda a sugestão de reserva. Projete um painel de explicações com regras transparentes, exemplos fictícios e revisão pelo usuário. Na demo, identifique explicações simuladas e mantenha integração futura com IA separada dos cálculos. Não conecte bancos, não solicite credenciais e não faça transações. Use navegação por teclado, contraste legível, estados vazio e de erro. Entregue uma prévia com painel mensal, lançamentos e metas.

## Fluxo proposto

1. **Painel mensal:** escolher mês, visualizar saldo realizado e distribuição das despesas.
2. **Lançamentos:** incluir, editar ou excluir registros. Alterações afetam somente o mês da data do lançamento.
3. **Meta:** informar a reserva desejada e conferir a diferença entre saldo realizado e saldo após a reserva planejada. Uma meta não é uma despesa realizada.
4. **Explicações:** exibir os dados usados na regra e indicar quando a análise é simulada. O usuário decide se ajusta o orçamento ou a meta.

## Critérios de validação da prévia

| Cenário | Resultado esperado |
| --- | --- |
| Receitas de R$ 3.000, despesas de R$ 2.200 e meta de R$ 500 | Saldo realizado de R$ 800 e saldo após a meta de R$ 300 |
| Receitas de R$ 1.000 e despesas de R$ 1.200 | Déficit de R$ 200 e reserva suspensa |
| Mês sem lançamentos | Totais zerados e orientação para cadastrar o primeiro item |
| Valor zerado, negativo ou data inválida | Mensagem de validação sem alterar os totais |
| Editar a data para outro mês | Totais atualizados no mês de origem e no mês de destino |

## Registro da interação

O PRD foi inserido na interface do Lovable. Ao enviar, a plataforma abriu a tela de cadastro. A geração da prévia e a captura das evidências da interação ficam pendentes de acesso ao Lovable.

## Reflexão

Separar o problema de negócio da solução reduziu o escopo para três telas e um fluxo que pode ser testado. O caso numérico tornou a regra de orçamento verificável. Separar cálculos determinísticos de explicações simuladas deixa explícito de onde vem cada número e evita apresentar uma resposta gerada como saldo real.

[Repositório-base da DIO](https://github.com/digitalinnovationone/dio-lab-vibe-coding-app-financas)
