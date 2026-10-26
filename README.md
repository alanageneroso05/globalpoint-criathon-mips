# GlobalPoint — Estufa Espacial Inteligente

**CRIATHON MIPS | Arquitetura e Organização de Computadores | UNIFESP 2026.2**

> Status: planejamento. O programa ainda não está implementado nem validado no MARS.

## Proposta
Simulador interativo de monitoramento e controle ambiental de uma estufa espacial, escrito em Assembly MIPS para o MARS. O usuário insere temperatura, umidade e luminosidade; o sistema simula decisões de ventilação, irrigação e iluminação, apresenta a situação ambiental e mantém um histórico de até **10 rodadas**.

**Público previsto:** estudantes, laboratórios de ensino e pesquisadores interessados em automação de cultivo e ambientes controlados. É um protótipo didático, sem sensores ou atuadores reais.

## Funcionalidades planejadas
- Menu interativo: registrar rodada, consultar estado, consultar histórico e encerrar.
- Comparar leituras com limites didáticos iniciais: ventilação se temperatura > 30 °C; irrigação se umidade < 40%; iluminação se luminosidade < 50.
- Classificar o ambiente como estável, atenção ou crítico (regra a definir).
- Exibir consumo energético simulado (fórmula a definir).
- Guardar no máximo 10 rodadas, avisando quando o histórico estiver cheio.
- Validar entradas e apresentar resumo ao encerrar.

Os limites são **provisórios** e sujeitos à confirmação com a professora.

## Requisitos técnicos
Decisões e laços; manipulação de vetor/matriz/string; pelo menos três procedimentos com parâmetros, retornos e preservação de registradores; pilha com finalidade real; tratamento de entradas inválidas; estado atualizado; pelo menos **100 linhas úteis de instruções MIPS**, sem preenchimento artificial.

## Organização
```text
README.md
src/globalpoint.asm
docs/ficha-tecnica.md
docs/testes.md
docs/uso-ia.md
```

## Como executar
**Pendente:** quando a implementação estiver pronta, abrir `src/globalpoint.asm` no **MARS**, montar (Assemble) e executar (Run). As instruções e configurações exatas serão verificadas e atualizadas após os testes.

## Equipe
Alana, Julia e Fernanda. A divisão de tarefas seguirá o documento de proposta aprovado pelo grupo.

## Acompanhamento
Proposta: 26/10/2026; demonstração 1: 11/11/2026; demonstração 2 e entrega final: 07/12/2026 (conforme confirmação da professora); avaliação individual: 09/12/2026.

Veja a [ficha técnica](docs/ficha-tecnica.md), os [testes](docs/testes.md) e o [registro de IA](docs/uso-ia.md).

## Limitações
Não é um controlador físico. Leituras, limites, risco e energia são simulados. Resultados ainda não testados.
