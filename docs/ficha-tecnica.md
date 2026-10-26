# Ficha técnica — GlobalPoint

**Status:** planejamento inicial; nenhuma funcionalidade validada no MARS.

## Objetivo
Simular o monitoramento de uma estufa espacial com decisões sobre ventilação, irrigação e iluminação, usando Assembly MIPS.

## Fluxo previsto
1. Mostrar menu.
2. Ler e validar temperatura, umidade e luminosidade.
3. Avaliar as condições e atualizar os equipamentos.
4. Calcular classificação e consumo simulados.
5. Registrar a rodada em vetores (até 10).
6. Permitir consultas e encerramento.

## Regras preliminares
| Condição | Ação |
| --- | --- |
| Temperatura > 30 °C | Ligar ventilação |
| Umidade < 40% | Ligar irrigação |
| Luminosidade < 50 | Ligar iluminação |

Valores iguais aos limites não acionam os equipamentos. Faixas de validação, classificação ambiental e cálculo de energia ainda serão definidos.

**Histórico cheio:** após dez registros, avisar e não gravar a 11ª rodada; preservar os dez registros.

## Estruturas planejadas
Vetores para as leituras e estados das rodadas; contador de rodadas; estado atual dos equipamentos; acumulador de energia simulada.

## Procedimentos propostos
- `mostrar_menu`: exibir opções e obter escolha.
- `ler_validar`: ler e verificar dados.
- `avaliar_ambiente`: atualizar equipamentos e classificação.
- `registrar_rodada`: armazenar nos vetores.
- `exibir_relatorio`: mostrar estado/histórico/resumo.

Usar `jal` e `jr $ra`, argumentos em `$a0–$a3` e retorno em `$v0` quando apropriado. Preservar registradores conforme convenções MIPS e usar a pilha justificadamente, especialmente em chamadas aninhadas.

## Checklist de requisitos
- [ ] Executar no MARS.
- [ ] Entrada e saída interativas.
- [ ] Decisões e repetições funcionais.
- [ ] Vetor/matriz/string manipulado.
- [ ] Pelo menos três procedimentos.
- [ ] Parâmetros, retornos e registradores preservados.
- [ ] Pilha utilizada e justificada.
- [ ] Entrada inválida e encerramento tratados.
- [ ] Duas ações relacionadas e estado alterado.
- [ ] Pelo menos 100 linhas úteis de instruções MIPS verificadas.

## Equipe
Alana, Julia e Fernanda. Manter a divisão de tarefas da proposta aprovada; detalhar atribuições aqui após confirmação do grupo.

## Pendências
Confirmar valores ambientais com a professora; definir faixas válidas, regra de classificação, consumo e menu definitivo. Atualizar esta ficha durante a implementação.
