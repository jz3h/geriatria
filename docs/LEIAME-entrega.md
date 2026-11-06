# Pós-graduação em Geriatria 2.0 — Afya Educação Médica
## Documento de entrega · Conteúdo autoral e arquitetura de produção

**Conteudista:** Dr. José Dias Linhares Júnior — CRM-RS 49835 · RQE 41886
**Escopo sob responsabilidade do conteudista:** Módulos 01, 02, 03, 04, 05, 06, 13 e 16, além das 30 aulas de Nivelamento.
**Data desta entrega:** 5 de novembro de 2026.

---

## 1. O que esta entrega contém

Cada aula é uma peça de dez minutos construída sobre uma divisão fixa de tela: a metade esquerda carrega o recurso gráfico, a metade direita carrega a base teórica destinada ao docente que gravará a aula. O formato foi desenhado para funcionar como ponte — a aula-pílula provoca, situa clinicamente e devolve o aluno às aulas teóricas do curso com uma pergunta na cabeça.

Os assuntos abordados no escopo do conteudista percorrem o eixo clínico da Geriatria contemporânea: síndromes geriátricas e iatrogenia; incapacidade cognitiva, do comprometimento cognitivo leve às demências; instabilidade postural, quedas, imobilidade e incontinência urinária; doença de Alzheimer; demência vascular e demais etiologias; neurologia geriátrica, incluindo doença de Parkinson, acidente vascular encefálico e tonturas; psicogeriatria; fragilidade, sarcopenia e fraturas; e bioética e cuidados paliativos aplicados à pessoa idosa. O Nivelamento cobre os fundamentos que precedem esse percurso.

---

## 2. Autoria e método de escrita

O texto é autoral. Foi escrito pelo conteudista, médico com atuação clínica em Clínica Médica e Medicina de Família e Comunidade, e submetido a um ciclo de assistência e revisão por sistemas de inteligência artificial de última geração, operados pelo próprio autor sob supervisão clínica direta.

O método seguiu três tempos, em todas as aulas:

**Primeiro tempo — concepção clínica.** A situação-problema de cada aula parte da prática: um caso construído pelo conteudista a partir de atendimentos reais, desidentificado e recomposto para fim didático. Esses casos são creditados nas aulas em formato Vancouver, com autoria explícita, porque constituem produção intelectual própria e não citação de terceiros.

**Segundo tempo — assistência de redação e verificação cruzada.** A redação contou com modelos de linguagem distintos, escolhidos por competência específica: **Claude Fable** (Anthropic) na arquitetura textual, no encadeamento argumentativo e na revisão de consistência clínica; **Gemini Argon** (Google) na geração de cenas e na exploração de alternativas narrativas; e o **motor de inteligência artificial do Whitebook** (PEBMED) no cruzamento das condutas com a base de referência usada à beira do leito no Brasil. Somou-se a esses um **modelo de inferência local**, executado em ambiente próprio, empregado nas tarefas de visão computacional descritas na seção 4 — segmentação semântica de imagem por rede neural convolucional, sem dependência de serviço externo.

**Terceiro tempo — revisão em três camadas.** Cada aula passou por dois agentes de revisão treinados com diretrizes específicas do projeto — um voltado à exatidão clínica e à rastreabilidade das fontes, outro voltado à coerência didática, à densidade de informação por slide e à conformidade com a identidade visual — e, ao final, pela revisão do próprio conteudista, que reescreveu a maior parte do material produzido na assistência. Nenhum trecho foi entregue sem leitura humana final.

---

## 3. Fontes: atualização e literatura consolidada

A entrega adota uma regra de bibliografia explícita: toda afirmação com consequência clínica é sustentada por fonte localizável, e cada aula fecha com suas referências em formato Vancouver, com PMID ou DOI sempre que existentes.

As aulas passaram por um rigoroso cruzamento de fontes. Buscando atualização, o material conta com artigos altamente atualizados publicados nos últimos 48 meses, verificados individualmente em base indexada, combinados à literatura consolidada que sustenta a disciplina — diretrizes de sociedades, protocolos oficiais do Ministério da Saúde, instrumentos validados em português e os marcos clássicos da Geriatria, que não envelhecem.

Além disso, todas as aulas foram cruzadas com a ferramenta de inteligência artificial do Whitebook e com bases literárias sólidas, tanto as disponibilizadas pelo Dr. Leonardo quanto o material de Avaliação Geriátrica Ampla e as ferramentas utilizadas por padrão pelo Grupo.

A verificação das referências foi feita por acesso programático a bases primárias — PubMed, registros de ensaios clínicos e repositórios de acesso aberto — e não por memória de modelo. Referências que não resistiram à verificação foram descartadas e substituídas.

---

## 4. Esteira de produção dos recursos gráficos

Os recursos visuais não são ilustração decorativa: cada um responde a uma função didática definida antes do desenho. A esteira combina quatro estágios e é inteiramente reprodutível.

**Estágio 1 — especificação.** Para cada slide o conteudista define o que a imagem precisa fazer: nomear um conflito, sustentar uma comparação, ordenar um fluxo, fixar um número. Dessa especificação nasce o prompt da cena.

**Estágio 2 — geração.** As gravuras de abertura são geradas em **Gemini Argon**, sob prompts autorais com estilo fixo: retrato editorial de pessoa idosa brasileira, luz natural, acentos de cor restritos à paleta institucional, sem texto embutido. Os recursos esquemáticos — fluxogramas, comparações, linhas do tempo, mapas de aula — são construídos em código, não em editor gráfico, o que garante alinhamento tipográfico exato e permite regeneração em lote.

**Estágio 3 — acabamento assistido por visão computacional.** Cada gravura passa por um pipeline próprio, escrito em Python sobre OpenCV, NumPy e Pillow, com inferência de rede neural em ONNX Runtime executada localmente. O pipeline mede o tom da cena e escolhe entre cinco acabamentos calibrados — óleo por filtro de Kuwahara anisotrópico orientado pelo tensor de estrutura, impressão editorial com curva S e split-tone, tratamento cinematográfico, serigrafia por quantização em espaço LAB e luz dirigida com vinheta —, sempre com proteção do tom de pele por máscara de matiz, para que a dignidade da pessoa retratada nunca se perca no efeito. O objeto que carrega o sinal clínico recebe realce magenta de baixa dose, restrito ao maior componente conexo da máscara de cor.

**Estágio 4 — animação de disparo único.** Onde a animação ensina, ela existe: o sinal sobe em pouco mais de meio segundo e congela. Não há repetição, não há movimento de fundo, não há elemento que compita com a fala do professor. Cada recurso é entregue em duas formas, lado a lado na pasta de recursos gráficos: **PNG em alta resolução** e, quando o recurso tem movimento, **GIF de disparo único** com quadro-pôster na primeira posição. Dentro dos arquivos PPTX, o recurso animado já vem embutido onde existe animação e o estático onde o recurso não se move — **e, sempre que o docente precisar da animação em outra peça, a versão animada pode ser puxada da pasta de recursos gráficos, com o mesmo nome do arquivo estático e extensão `.gif`**. A dupla entrega existe porque nem todo ambiente de exibição reproduz animação.

A ferramenta que organiza essa esteira, da especificação ao arquivo final, é o **AuraMed**, desenvolvida pelo próprio conteudista para este projeto.

---

## 5. Tecnologia empregada

A produção é um sistema de software, não um conjunto de arquivos montados à mão. O inventário técnico:

| Camada | Tecnologia |
|---|---|
| Linguagens | Python 3.13, JavaScript (Node), HTML5, CSS3, SVG, Markdown |
| Composição dos slides | python-pptx com layout paramétrico; tipografia Hanken Grotesk variável |
| Renderização dos recursos | Chromium headless via Playwright, captura em resolução dupla |
| Visão computacional | OpenCV, NumPy, Pillow; segmentação semântica ISNet em ONNX Runtime, inferência local |
| Códigos QR | codificador próprio em Python (modo byte, correção de nível M, versões 1 a 10), com verificação por decodificação automática de cada código gerado |
| Modelos de linguagem | Claude Fable (Anthropic), Gemini Argon (Google), motor de IA do Whitebook (PEBMED) |
| Verificação bibliográfica | conectores programáticos a PubMed, registros de ensaios clínicos, repositórios de pré-publicação e bases de acesso aberto |
| Automação de revisão | agentes especializados com diretrizes próprias, executados em paralelo sobre o acervo |
| Conversão e validação | LibreOffice headless para prova de renderização; verificação automática de cada arquivo entregue |

**Aprendizado de máquina e aprendizado profundo** entram na esteira em dois pontos concretos e verificáveis: na segmentação semântica das gravuras, por rede neural convolucional profunda treinada para separação de sujeito, executada localmente; e nos modelos de linguagem de grande porte usados na assistência de redação e na revisão cruzada, cuja arquitetura transformer é, ela própria, aprendizado profundo aplicado a linguagem natural.

**Busca profunda (deep searching).** A pesquisa bibliográfica e metodológica não se limitou a consultas pontuais. Foram conduzidas investigações multiagente, com decomposição do problema em frentes paralelas, leitura de literatura em mais de um idioma e síntese posterior — método aplicado tanto à atualização clínica quanto às decisões de desenho instrucional que sustentam o formato das aulas.

**Conectores e Skills.** A produção operou sobre conectores que dão acesso programático direto às bases bibliográficas e aos repositórios do projeto, e sobre Skills — rotinas especializadas e reutilizáveis para construção de documentos, apresentações, planilhas e peças visuais, aplicadas de forma padronizada em todo o acervo. É o que explica a uniformidade entre aulas produzidas em momentos diferentes.

---

## 6. Controle de versões e volume de ajuste

O acervo é versionado. Cada aula tem histórico de construção, e cada rodada de revisão deixa registro do que mudou e por quê. Ao longo da produção foram executadas rodadas sucessivas de correção, entre elas: padronização bibliográfica com verificação individual das referências; remoção de presunções temporais no texto; ajuste de densidade e tamanho de fonte para legibilidade em estúdio; substituição integral do parque de gravuras por geração realista em resolução superior; refatoração completa do acabamento visual, com cinco iterações de método até o padrão final aprovado; e revisão clínica dirigida, aula por aula, com correções pontuais de conduta onde o cruzamento de fontes apontou divergência.

Entre as melhorias de maior alcance está a duplicação deliberada do parque de recursos: cada peça visual passou a existir em versão estática de alta resolução e em versão animada de disparo único, o que elevou o acervo de 260 recursos distintos para 495 arquivos entregues apenas no Módulo 01, e deu ao docente liberdade de escolher a forma que melhor serve a cada momento da gravação.

O número de versões por aula varia conforme a complexidade do tema; nenhuma aula foi entregue em primeira versão. Os relatórios de auditoria e as notas de revisão acompanham o acervo e estão disponíveis ao Grupo mediante solicitação.

---

## 7. Metodologias ativas

O material incorpora recursos de metodologia ativa pensados para funcionar sem exigir que o aluno interaja com aplicativo durante a aula — o estímulo está na própria peça visual.

**Lacuna de curiosidade.** Cada aula abre com uma cena que apresenta um conflito clínico antes de oferecer a explicação, e o recurso de abertura retorna alterado no fechamento, agora com a informação que faltava.

**Sinalização visual.** Um único objeto por cena carrega a cor de alerta. É o elemento que o olho encontra primeiro e o que a memória retém.

**Animação de disparo único.** O movimento acontece uma vez, marca o ponto e congela, respeitando o tempo da fala do docente.

**Códigos QR.** As aulas trazem acessos diretos a ferramentas oficiais — calculadoras de referência, protocolos, instrumentos validados, bases governamentais —, sempre selecionados entre fontes de alta confiabilidade. O último slide de cada aula traz dois acessos: um código dinâmico, de endereço fixo e destino editável, que abre os recursos e materiais daquela aula e será ampliado ao longo do curso sem invalidar o material já entregue; e, abaixo dele, o acesso fixo ao Whitebook, para consulta à beira do leito.

As imagens, animações e peças interativas foram produzidas com o **AuraMed**, ferramenta criada pelo conteudista.

---

## 8. Natureza do material e autonomia do docente

Os recursos gráficos e os textos desta entrega constituem **base de trabalho**. Foram construídos para que o corpo docente e a Afya Educação Médica os utilizem da forma que julgarem mais adequada — na íntegra, em parte, recombinados ou adaptados ao estilo de cada professor. O texto da metade direita é apoio ao docente, não roteiro de leitura obrigatória; o recurso da metade esquerda é instrumento didático, não ilustração fechada. A decisão editorial final é do Grupo.

---

## 9. Organização das pastas

```
ENTREGAS - JOSÉ
└── Conteúdo - Módulos
    └── Aulas (Módulos Completos)
        └── Módulo 01 — Síndromes Geriátricas e Incapacidade Cognitiva
            ├── LEIAME - Módulo 01
            ├── Aulas (PPTX - COMPLETO - 18 AULAS)
            ├── Fonte de Letras
            └── Recursos Gráficos e suas Variações - M01
```

Cada módulo repete essa estrutura. A pasta de fontes traz os arquivos da tipografia oficial do projeto e as instruções de instalação, necessárias para que os arquivos abram com a tipografia correta em qualquer estação.

---

*Documento produzido em 5 de novembro de 2026 como parte da entrega de conteúdo da Pós-graduação em Geriatria 2.0 da Afya Educação Médica.*
