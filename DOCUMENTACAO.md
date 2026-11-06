# Documentação completa — Hemocentro Vida

**Projeto acadêmico APS II · Sprints 1 e 2**

Este documento reúne os registros do projeto para facilitar a consulta em um único arquivo no GitHub. O código executável está em `index.html`. As datas de conclusão dos compromissos são declarações da equipe; o relatório original da Sprint 1 preserva o retrato parcial produzido anteriormente.

**Atenção:** protótipo acadêmico, não validado para uso clínico real. Não inserir dados pessoais reais.

## Sumário

1. Sprint 1
2. Sprint 2
3. Requisitos e escopo
4. Arquitetura
5. Regras de negócio
6. Testes e demonstração
7. Evidências e rastreabilidade
8. Limitações e próximos passos

---

# Sprint 1 — Organização e definição inicial

**Período:** 17/09 a 30/09/2026, conforme a apresentação da equipe.

## Objetivo documentado
Definir a identidade visual, a metodologia de trabalho e a distribuição de responsabilidades; discutir o público-alvo e o alcance do sistema.

## Decisões registradas
- **Método:** Scrum; **quadro:** Trello.
- **Fluxo do quadro:** Product Backlog → Sprint Backlog → A Fazer → Em andamento → Concluído.
- **Tecnologias escolhidas:** HTML, CSS e JavaScript.
- **Identidade visual:** branco predominante, vermelho de destaque e preto para textos/detalhes.
- **Responsabilidades:** programação (Tiago, Diego, Miguel e Guilherme); documentação (Beatriz, Rickelme e Kauê); design (todos).

## Situação do relatório original
O relatório descreveu **4 cartões comprometidos e 0 concluídos naquele momento**, classificou o objetivo como parcialmente atingido e apontou indefinição sobre atendimento a uma unidade ou a várias unidades.

## Atualização informada pela equipe
Posteriormente, um integrante confirmou **conclusão dos quatro compromissos da Sprint 1**. A conclusão final não está registrada no relatório inicial. Para evitar contradições, o resultado final é identificado como **confirmação da equipe**, enquanto o número 0/4 é preservado como retrato documental anterior.

## Evidências
- [Relatório original](docs/fontes/relatorio-sprint-1-original.pdf).
- [Código da versão disponibilizada](index.html), que evidencia a materialização posterior do projeto, sem datar cada implementação.

## Aprendizado
Registrar o aceite e a data de conclusão de cada compromisso no momento do encerramento, sem depender exclusivamente do status posterior do quadro.

---

# Sprint 2 — Escopo, primeira página e documentação

**Período planejado:** 08/10 a 21/10/2026. **Capacidade estimada:** 10 horas de trabalho da squad.

## Objetivo do planejamento
Definir público-alvo e escopo inicial, iniciar uma página HTML/CSS e organizar documentação e atividades.

| Compromisso | Responsáveis | Critério previsto |
|---|---|---|
| Definir público e escopo | Toda a equipe | Escopo documentado e aprovado |
| Criar a primeira página | Tiago, Diego, Miguel e Guilherme | Página executável e organizada |
| Organizar a documentação | Beatriz, Rickelme e Kauê | Documentação disponível |
| Atualizar e acompanhar o Trello | Toda a equipe | Quadro atualizado conforme progresso |

## Resultado informado pela equipe
Um integrante confirmou que **os quatro compromissos foram concluídos** e que o **protótipo já estava funcional até 21/10/2026**, incluindo cadastro, triagem, coleta, fracionamento, estoque e requisições.

**Precisão documental:** o arquivo de origem é um **planejamento**, não uma ata de aceite. O código atual comprova a implementação dos módulos na versão entregue, mas não permite verificar a data exata de cada um. O quadro Trello, segundo a equipe, não era atualizado regularmente; portanto, suas datas não são tomadas como medição exclusiva de entrega.

## Planejado versus demonstrável
A primeira página executável é sustentada pelo arquivo [`index.html`](index.html). O sistema atual vai além de uma página estática. A confirmação do prazo e do encerramento dos compromissos foi fornecida pela equipe.

## Escopo inicialmente adiado
O planejamento original mencionou como itens futuros o sistema completo, integração com banco de dados, cadastro funcional, agendamento e funções administrativas. **O cadastro funcional aparece na versão atual do HTML**; a documentação não afirma que todas as funções futuras foram concluídas na Sprint 2.

## Fontes
- [Planejamento original](docs/fontes/planejamento-sprint-2-original.docx)
- [Código atual](index.html)

---

# Requisitos e escopo

## Problema abordado
Apoiar, em ambiente demonstrativo, a organização do cadastro de doadores e das etapas de triagem, coleta, processamento, estoque e atendimento de requisições.

## Público e abrangência
O relatório inicial registra uma dúvida sobre atender **uma unidade** ou **várias unidades**. A equipe informou que o compromisso de definição do escopo foi concluído, mas **não foi fornecida a decisão formal final em documento específico**. Não presumimos qual opção foi aprovada.

## Funcionalidades verificáveis na versão atual
| Área | Comportamento identificado no HTML |
|---|---|
| Doadores | Cadastro e listagem |
| Triagem | Formulário e validações demonstrativas |
| Coleta | Registro de coleta e bolsa |
| Fracionamento | Geração de hemocomponentes |
| Requisições | Registro e validações demonstrativas |
| Estoque | Consulta de itens, vencimentos e situação |
| Testes | Tela de execução de casos de teste |

## Requisitos não demonstrados como concluídos
Autenticação robusta, backend e banco remoto, integração com sistemas clínicos, interoperabilidade, auditoria institucional, agendamento completo e adequação regulatória para uso real.

## Critério de uso
O protótipo é **acadêmico**. Não utilizar decisões automatizadas como parecer médico ou validação transfusional real.

---

# Arquitetura técnica

## Visão geral
A versão fornecida é uma aplicação de página única em `index.html`, composta por HTML, CSS e JavaScript. A navegação ocorre entre seções do documento e a lógica é executada no navegador.

```text
Navegador
  ├── Interface HTML/CSS
  ├── Lógica JavaScript
  └── localStorage (dados locais do navegador)
```

## Execução
Abra `index.html` no navegador. Algumas bibliotecas e recursos visuais são carregados por **CDN**, portanto podem exigir conexão com a internet.

## Persistência
O código utiliza `localStorage`: os dados ficam no navegador utilizado e não são compartilhados entre computadores. Limpar os dados do navegador pode eliminar os registros locais.

## Limites arquiteturais
- Não foi identificado backend operacional nem banco de dados remoto no arquivo entregue.
- Não há garantia de autenticação, controle de acesso, backups ou trilha de auditoria clínica.
- Não há validação independente da segurança ou das regras clínicas.
- Não usar dados pessoais reais durante testes acadêmicos.

## Evolução recomendada
Separar camadas, criar API e persistência controlada, estabelecer testes automatizados independentes e implantar controles de privacidade e segurança antes de qualquer cenário real.

---

# Regras de negócio — versão demonstrativa

O HTML identifica regras como **RN-04** (somente candidatos aprovados podem seguir para coleta), **RN-05** (validade de hemocomponentes contada segundo evento de referência no fluxo) e **RN-08** (fracionamento uma única vez por bolsa e sem reversão).

Também há validações demonstrativas de elegibilidade e compatibilidade no fluxo de triagem e requisição.

## Cuidados de interpretação
- As regras aqui descritas são **comportamentos do protótipo**, não um parecer sobre sua conformidade clínica ou legal.
- Critérios de doação, intervalos, compatibilidade, conservação e validade exigem validação por profissionais e normas vigentes antes de qualquer uso real.
- A identificação RN-04/RN-05/RN-08 reproduz os rótulos do código; não constitui uma especificação integral de todas as regras do sistema.

## Verificação
Consultar os formulários e funções JavaScript em [`index.html`](index.html). Executar cenários apenas com dados fictícios.

---

# Testes e demonstração

## Roteiro proposto — cinco minutos
| Tempo | Ação |
|---|---|
| 00:00–00:40 | Abrir cadastro e mostrar um doador fictício |
| 00:40–01:30 | Executar triagem e mostrar resultado permitido/bloqueado |
| 01:30–02:30 | Registrar coleta de candidato apto; mostrar unidade fixa/móvel |
| 02:30–03:30 | Fracionar bolsa e exibir componentes |
| 03:30–04:30 | Consultar estoque, validade e requisição |
| 04:30–05:00 | Apresentar painel de testes e limitações |

**Este é um roteiro sugerido, não um registro de execução.** Deve ser ensaiado no navegador, com dados fictícios, antes da avaliação.

## Testes identificados
A versão atual apresenta uma seção intitulada **“Sprint 5: 10 Testes”**. A existência dessa seção no código não demonstra que os dez testes passaram em execução independente, nem que pertencem às Sprints 1 e 2.

## Checklist pré-apresentação
- [ ] Abrir `index.html` e conferir o carregamento de recursos.
- [ ] Usar exclusivamente doadores fictícios.
- [ ] Confirmar os caminhos e estados iniciais.
- [ ] Validar cada transição antes da apresentação.
- [ ] Executar o roteiro cronometrado.
- [ ] Registrar capturas de tela e resultados reais dos testes.

## Capturas de referência
![Triagem](docs/evidencias/triagem.png)
![Doadores](docs/evidencias/doadores.png)
![Estoque](docs/evidencias/estoque.png)

As imagens foram extraídas de material da apresentação fornecido; são **recortes ilustrativos da versão disponibilizada**, não prova datada de execução em 21/10.

---

# Evidências e rastreabilidade

| Afirmação | Fonte | Grau de comprovação |
|---|---|---|
| Sprint 1 definiu Scrum, Trello, responsabilidades e cores | Relatório S1 | Documental |
| Relatório inicial S1 registrava 0/4 cartões concluídos | Relatório S1 | Documental naquele momento |
| Quatro compromissos da Sprint 1 foram concluídos | Confirmação posterior da equipe | Declaração da equipe; sem ata final anexada |
| Sprint 2 planejou quatro compromissos e 10 horas | Planejamento S2 | Documental |
| Quatro compromissos da Sprint 2 foram concluídos | Confirmação posterior da equipe | Declaração da equipe; sem ata final anexada |
| Protótipo tinha módulos funcionais até 21/10 | Confirmação posterior da equipe | Prazo informado; sem histórico de versões datado |
| Módulos estão implementados na versão entregue | Código HTML | Evidência de implementação atual |
| Trello não era atualizado regularmente | Esclarecimento da equipe | Declaração da equipe |

## Nota sobre o Trello
O Trello não deve ser usado como única medida do desenvolvimento: a equipe informou que o quadro teve atualização irregular e que isso foi esclarecido ao professor. Isso **não elimina a necessidade de transparência** sobre o relatório original e as evidências disponíveis.

## Capturas e documentação
As imagens em `evidencias/` são recortes da versão apresentada. Os documentos originais permanecem preservados em `fontes/`.

## Datas
Não foram inventadas datas de commits, aceites, testes ou encerramentos. A data de publicação do GitHub será posterior à produção inicial do sistema.

---

# Limitações e próximos passos

## Dificuldades identificadas
1. Definição inicial do público-alvo e abrangência.
2. Atualização irregular do Trello, conforme informado pela equipe.
3. Ausência de registro final individualizado dos compromissos nos documentos fornecidos.
4. Dificuldade de associar funcionalidades do HTML atual a versões e datas históricas.

## Limitações do produto atual
Persistência local no navegador; ausência de backend e autenticação; uso acadêmico de regras clínicas; necessidade de validar segurança, privacidade, integridade e comportamento dos fluxos.

## Próximas ações sugeridas
- Publicar versão identificada e README.
- Criar critérios de aceite e anexar evidências por sprint.
- Documentar a decisão formal sobre unidade única ou múltiplas unidades.
- Registrar testes reproduzíveis e seus resultados.
- Avaliar banco de dados, autenticação, backups e LGPD antes de qualquer implantação real.
- Manter o quadro atualizado e vincular cartões a versões do código.

Essas ações são **recomendações de evolução**, não promessas já concluídas nas Sprints 1 e 2.

---

## Links do projeto

- [Repositório](https://github.com/Tiagox21/hemocentro-vida)
- [Trello da equipe](https://trello.com/b/Ojc84enu)

**Nota:** imagens e fontes originais referenciadas exigem que as respectivas pastas sejam publicadas; este arquivo de texto pode ser publicado sozinho.
