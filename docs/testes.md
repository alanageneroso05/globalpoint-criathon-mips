# Plano de testes — GlobalPoint

> Casos **planejados**, ainda **não executados** no MARS. Não registrar aprovação antes de testar.

## Teste 1 — Fluxo normal
**Entrada sugerida:** temperatura 32, umidade 35, luminosidade 45.

**Esperado pelas regras iniciais:** ventilação, irrigação e iluminação ligadas; uma rodada registrada. Classificação e energia dependerão das fórmulas a definir.

**Resultado observado:** pendente. **Status:** não executado.

## Teste 2 — Entrada inválida
**Entrada:** opção inexistente no menu e/ou leitura fora da faixa que o grupo definir.

**Esperado:** rejeitar a entrada, informar erro e permitir nova tentativa sem corromper o estado.

**Resultado observado:** pendente. **Status:** não executado.

## Teste 3 — Limite de capacidade
**Entrada:** dez rodadas válidas e tentativa de registrar a 11ª.

**Esperado:** manter dez registros, informar histórico cheio e não armazenar a 11ª.

**Resultado observado:** pendente. **Status:** não executado.

## Testes adicionais
- Leituras iguais aos limites (30, 40, 50).
- Encerrar sem nenhuma rodada.
- Ativar zero, um ou dois equipamentos.
- Conferir preservação de registradores e retorno de procedimentos.
- Conferir histórico e consumo acumulado.

## Registro de execução
Para cada teste: data, versão/commit, versão do MARS, entrada, saída observada, resultado (aprovado/reprovado), responsável e correção.
