# Manual de continuidade — Pós-graduação em Geriatria 2.0 (Afya)
### Documento único para retomar o projeto em uma conversa nova · 5 de novembro de 2026

Este documento é autossuficiente. Quem o ler consegue continuar o trabalho sem precisar do histórico da conversa anterior.

---

## 1. O projeto em uma página

**Quem.** Dr. José Dias Linhares Júnior (CRM-RS 49835 · RQE 41886) é o conteudista. Ele escreve e assina o conteúdo; a Afya Educação Médica grava as aulas com seus próprios docentes.

**O que se entrega.** Arquivos PPTX que servem de base teórica e gráfica para aulas-pílula de até dez minutos (14 a 15 slides). Cada slide é dividido ao meio: **à esquerda o recurso gráfico**, **à direita a base teórica que o professor usa para falar**. As aulas são ponte: provocam, situam clinicamente e devolvem o aluno às aulas teóricas do curso querendo estudar mais.

**Escopo do Dr. José.** Módulos 01, 02, 03, 04, 05, 06, 13 e 16 (18 aulas cada) e mais 30 aulas de Nivelamento (5 a 10 slides cada). Total 174 aulas. Os módulos 07 e 08 são de outra conteudista (Liz) e não entram.

**Destino.** OneDrive/SharePoint da Afya, em `Pós 2.0 - Geriatria › GERIATRIA 2.0 - AFYA › ENTREGAS - JOSÉ`.

---

## 2. Situação por frente

| Frente | Situação |
|---|---|
| **Módulo 01** | **Entregue.** 18 aulas, gravuras novas, pacote montado e enviado em três zips. |
| **Módulo 02** | Gravuras instaladas nas 18 aulas e PPTX reconstruídos. **Falta** montar o pacote e escrever o LEIAME do módulo. Duas gravuras são provisórias (A14 e A15). |
| **Módulos 03, 04, 05, 06, 13, 16** | Aulas construídas. **Aguardando as gravuras** que o Dr. José está gerando no Argon. |
| **Nivelamento (30 aulas)** | Aulas construídas. Aguardando gravuras. |
| **Hub de recursos** | Repositório publicado. Falta o Dr. José ligar o GitHub Pages. |

---

## 3. O hub no GitHub — hospedagem

**Repositório:** `jz3h/geriatria` · https://github.com/jz3h/geriatria
**Endereço público:** **https://jz3h.github.io/geriatria**

Esse endereço está **gravado em código QR no último slide de todas as 18 aulas do Módulo 01**. Ele nunca muda. O que muda é o conteúdo do `index.html` do repositório — é isso que torna o QR dinâmico.

**Pendência do Dr. José (uma vez só):** *Settings › Pages › Source: Deploy from a branch › Branch `main`, pasta `/ (root)` › Save*. Em um ou dois minutos o endereço responde.

**Quando as ferramentas estiverem prontas** (o Dr. José tem servidores Lenovo/Dell em casa): o `index.html` passa a redirecionar para onde elas estiverem. A recomendação técnica é servir o servidor doméstico por **Cloudflare Tunnel** — sem abrir porta, sem IP fixo — e deixar o GitHub Pages como camada de redirecionamento, porque ele não cai junto com a casa. Para redirecionar, basta trocar o corpo do `index.html` por:

```html
<meta http-equiv="refresh" content="0; url=https://ENDERECO-DAS-FERRAMENTAS">
```

Conteúdos previstos para o hub, já descritos na página: revisão de medicações, orientações ao paciente e ao cuidador, leitura de bula na pessoa idosa, direitos da pessoa idosa, escalas e instrumentos.

---

## 4. Decisões visuais fechadas — não revisitar sem pedido

**Paleta.** Magenta `#CE0058`, azul `#0057B7`, navy `#041E42`, papel claro. Tipografia **Hanken Grotesk** (variável; instâncias estáticas em `/home/claude/entrega_m01/fontes`).

**Acabamento das gravuras.** Cinco acabamentos aprovados, escolhidos automaticamente pelo tom medido da cena:

| Código | Acabamento | Quando entra |
|---|---|---|
| 2 | Óleo (Kuwahara anisotrópico orientado pelo tensor de estrutura) | luminância média < 88 |
| 6 | Cinema (curva S, sombra fria, pele protegida) | < 112 |
| 7 | Serigrafia (quantização em LAB, contorno fino) | detalhe alto + croma alto |
| 5 | Editorial impresso (curva S, split-tone, grão) | luz alta e quente |
| 9 | Luz dirigida (vinheta suave + foco quente) | demais casos |

**Regra de ouro: contraste e paleta preservados, pele sempre viva.** O Dr. José rejeitou explicitamente qualquer tratamento que deixasse a pessoa idosa com aparência cadavérica. Nada de dessaturar a cena, nada de azul pastel.

**Sinal de perigo.** O magenta é o único sinal. Halo de baixa dose sobre o objeto, mais realce do núcleo. Quando o campo magenta é grande (manta, parede), mantém-se só o maior componente conexo e a dose cai. A animação sobe em meio segundo e congela — **um disparo, sem repetição, nunca em laço**.

**Forma.** Imagem quadrada inteira no slide. **Sem legenda, sem borda, sem moldura.** A borda em pincelada foi testada e descartada: clareava demais a imagem. A legenda em Poppins foi testada e descartada: o Dr. José decidiu tirar as frases.

**Animação.** Onde o recurso tem movimento, o PPTX leva o GIF; onde é estático, leva o PNG. No deck o GIF é comprimido (950 px, 72 cores, 16 quadros) para o arquivo abrir rápido; **na pasta de Recursos Gráficos vai a versão em qualidade cheia** (1440×864, 58 quadros), e os LEIAMEs avisam que o docente pode puxá-la de lá.

**QR do último slide.** Nas aulas cujo tema se repete dentro do módulo, o cartão de ferramenta é genérico — *Recursos da aula · acesso rápido · acesse para ajudar sua prática e seu estudo* — com o QR do hub. Nas demais, permanece a ferramenta oficial específica (STOPP/START, CKD-EPI, MoCA, ABRAz...). **O Whitebook fica sempre abaixo, com QR fixo.** No M01 receberam o cartão genérico: A01, A02, A08, A15, A17 e A18.

**Bibliografia.** Toda afirmação com consequência clínica tem fonte localizável. Cada aula fecha com suas referências em Vancouver, com PMID ou DOI. Fontes verificadas em base indexada, nunca de memória. Casos clínicos de abertura são autorais e citados como `Linhares Junior JD. Caso clínico ilustrativo construído para esta aula, a partir da prática clínica geriátrica. In: Pós-graduação em Geriatria 2.0. Afya; 2026.`

---

## 5. Onde está cada coisa

**Acervo das aulas:** `/tmp/claude-0/-home-claude/ea6a24c2-30bf-5ae8-96a4-308e50583570/scratchpad/diamante/`
Uma pasta por aula (`M01-A01` … `M16-A18`, `N01` … `N60`), cada uma com `lesson.json` (todo o conteúdo), `visuais/` (recursos em HTML, PNG e GIF) e o `.pptx` construído.

**Ferramentas de construção:** `diamante/tools/`
- `build.py` — compõe o PPTX. Backup antes das alterações de hoje: `build.py.bak_qr`.
- `revisao_v4.py`, `qa.py`, `check.py` — revisão e conferência.
- `qr/hub.png`, `qr/whitebook.png` — os dois QR usados no slide final.

**Pipeline de gravuras:** `/home/claude/gravuras/`
- `final.py` — escolhe o acabamento pelo tom e aplica o sinal magenta. Função principal: `gravura_final(src, frase=None, acab=None, fundo=None)`.
- `acab10.py` — os dez acabamentos avaliados (cinco em uso: A2, A5, A6, A7, A9).
- `pictorico.py` — filtros pictóricos (Kuwahara, aquarela, guache, risografia, carvão, litografia).
- `v6.py` — cor viva (`viva`) e sinal de perigo (`brilho_perigo`).
- `matte.py` — segmentação ISNet em ONNX, inferência local (pesos em `/home/claude/models/`).
- `qrcode_puro.py` — gerador de QR próprio (modo byte, nível M, versões 1–10). Foi preciso escrevê-lo porque **o ambiente não alcança PyPI nem npm**. Cada código gerado é verificado por decodificação com `cv2.QRCodeDetector`.
- `aulas.py` — mapa cena → aula.
- `lote10.py` (M01), `m2.py` (M02) — produção em lote.
- `hub_card.py` — troca o cartão de ferramenta pelo cartão genérico do hub.

**Montagem do pacote:** `/home/claude/pacote/montar.py`
**LEIAMEs e PDF:** `/home/claude/entrega_m01/` (`LEIAME.md`, `LEIAME_M01.md`, `pdf.py`, `fontes/`)

---

## 6. Receita: quando chegarem gravuras novas do Argon

O Dr. José envia as imagens quadradas (1024×1024) pelo chat. Para cada lote:

**1. Identificar a aula de cada cena.** Ele costuma mandar sem nome de arquivo legível. Peça a lista por número, ou monte uma folha de contato numerada e devolva para ele confirmar:

```python
# monta a folha de contato numerada
from PIL import Image, ImageDraw, ImageFont
# ...ver /home/claude/gravuras/ para o exemplo usado no M02
```

**2. Tratar.** Para cada imagem, com o acabamento escolhido pelo tom:

```python
import sys; sys.path.insert(0,'/home/claude/gravuras')
from final import tom, ACAB
from v6 import quadrada
import v6, acab10
im = quadrada(caminho_da_imagem)
cod = tom(im)                                   # escolhe entre "2","5","6","7","9"
_bp = v6.brilho_perigo
v6.brilho_perigo = lambda x,*a,**k: x; acab10.brilho_perigo = lambda x,*a,**k: x
sem = ACAB[cod](im)                             # acabamento sem o sinal
v6.brilho_perigo = _bp; acab10.brilho_perigo = _bp
cheio = _bp(sem, 1.1 if cod=="6" else 1.0)      # com o sinal magenta
cheio.save("gravura.png")
```

O GIF de disparo único nasce interpolando `sem` → `cheio` em 12 quadros (curva `1-(1-t)³`), com o quadro final repetido na frente como pôster e um congelamento de 1,5 s no fim. Ver `lote10.py` para o laço completo.

**3. Instalar.** Copiar `gravura.png` e `gravura.gif` para `<AULA>/visuais/`, guardando o anterior como `gravura_anterior.*`.

**4. Reconstruir.** `cd diamante && python3 tools/build.py --no-render <AULA> ...`
Use `--no-render` sempre que só a gravura mudou. **Sem** `--no-render` o Chromium re-renderiza todos os recursos da aula, o que leva minutos por aula.

**5. Conferir.** Converta um PPTX para PDF e olhe o slide 1 e o slide final:
`soffice --headless --convert-to pdf --outdir /tmp/chk <arquivo>.pptx && pdftoppm -png -r 85 -f 1 -l 1 /tmp/chk/*.pdf /tmp/chk/s1`

---

## 7. Receita: montar o pacote de um módulo

A arquitetura de pastas foi definida pelo Dr. José:

```
ENTREGAS - JOSÉ
├── LEIAME - Entrega.pdf / .md
├── Hub de recursos (publicar)
└── Conteúdo - Módulos
    └── Aulas (Módulos Completos)
        └── Módulo NN - <nome do módulo>
            ├── LEIAME - Módulo NN.pdf / .md
            ├── Aulas (PPTX - COMPLETO - 18 AULAS)
            ├── Fonte de Letras
            └── Recursos Gráficos e suas Variações - MNN
```

Nomes dos recursos: `<AULA>_s<NN>_<titulo_do_slide_em_slug>.png` e `.gif`. O slide 1 com gravura vira `<AULA>_s01_gravura.png`. A pasta leva também um `DESCRICOES_RECURSOS.md` gerado automaticamente.

**Pesos.** Um módulo inteiro passa de 600 MB. O que resolve:
- PNG dos recursos chapados: quantizar para 256 cores (4× menor, erro médio 0,01 — invisível). **As gravuras, que são fotográficas, ficam em cor contínua.**
- GIF do deck: 950 px, 72 cores, 16 quadros. GIF da pasta de recursos: qualidade cheia.
- Entregar em três zips: aulas + recursos estáticos; animados A01–A09; animados A10–A18.

O script `/home/claude/pacote/montar.py` faz a montagem e os zips.

---

## 8. Conteúdo obrigatório dos LEIAMEs

**LEIAME geral** (raiz): assuntos abordados; autoria do conteudista com assistência e revisão por IA de ponta; fontes atualizadas e literatura consolidada; esteira de criação das gravuras; revisão por dois agentes treinados mais o próprio conteudista; número de versões, ajustes e melhorias; tecnologia empregada (linguagens, modelos distintos de IA — Claude Fable, Gemini Argon, IA do Whitebook, modelo local —, conectores, Skills, busca profunda, aprendizado de máquina e profundo); metodologias ativas, QR codes e AuraMed como ferramenta criada pelo conteudista; e a declaração de que recursos e textos são **base de trabalho**, que a Afya e os docentes usam como julgarem melhor.

**LEIAME de cada módulo:** assuntos abordados; o parágrafo padrão sobre cruzamento rigoroso de fontes e artigos dos últimos 48 meses; o cruzamento com a IA do Whitebook, com as bases do Dr. Leonardo, com a Avaliação Geriátrica Ampla e as ferramentas padrão do Grupo; quantas aulas; quantos slides; quantos recursos gráficos; e as particularidades do módulo.

**Tom:** terceira pessoa, técnico e formal, passando a ideia do trabalho mais tecnológico e mais bem entregue possível — **sem nunca mostrar fraqueza**. Nada de quebrar números por ano de publicação nem de expor limitações. Os números citados precisam ser reais e verificáveis.

Modelos prontos: `/home/claude/entrega_m01/LEIAME.md` e `LEIAME_M01.md`. O PDF sai com `python3 pdf.py` (paleta e tipografia do projeto; as instâncias de peso da Hanken Grotesk precisam existir em `fontes/`, geradas com fontTools — a fonte variável sozinha não produz negrito no reportlab).

---

## 9. Números do Módulo 01 (para referência de formato)

| Item | Quantidade |
|---|---|
| Aulas | 18 |
| Slides | 260 |
| Recursos gráficos distintos | 260 |
| Arquivos de recurso entregues (estático + animado) | 495 |
| Gravuras de abertura | 18 |
| Referências distintas verificadas | 162 |
| Publicadas nos últimos 48 meses | 57 |
| Códigos QR | 36 |

---

## 10. Pendências

**Imediatas**
1. Dr. José: ligar o GitHub Pages em `jz3h/geriatria`.
2. Montar o pacote do Módulo 02 e escrever o LEIAME do módulo.
3. Gerar as duas gravuras definitivas que faltam no M02 — incontinência de esforço (A14) e por transbordamento (A15). Prompts prontos em `PROMPTS_M02_FALTANTES.md`; as atuais são provisórias.

**Aguardando material**
4. Gravuras dos módulos 03, 04, 05, 06, 13, 16 e do Nivelamento — o Dr. José está gerando no Argon e enviará, incluindo animações.
5. Textos oficiais do Estatuto da Pessoa Idosa e do Estatuto dos Direitos do Paciente (Lei 15.378/2026). **O acesso ao Planalto está bloqueado neste ambiente** — precisam vir do Dr. José.

**Decisões dele em aberto**
6. M02: seis gravuras sobraram e estão em `Recursos_Graficos/Gravuras_alternativas` (números 08, 09, 10, 14, 15 e 20).
7. M01: três gravuras aguardam veredito como alternativas às instaladas em A12, A06 e A09, no artefato de avaliação.

---

## 11. Como o Dr. José trabalha

Vale saber, para não desperdiçar tempo dele:

- Ele decide rápido e corrige rápido. Quando rejeita, rejeita o conjunto — não pede ajuste fino.
- Prefere **ver opções numeradas** a ler descrições. Folhas de contato numeradas funcionam muito melhor que explicações.
- Não quer justificativa nem autoelogio. Quer o trabalho feito e o problema nomeado quando existe.
- Pede explicitamente: **em caso de dúvida, fazer a mais, nunca a menos.**
- Os LEIAMEs e qualquer material que a Afya vá ler são peça de propaganda do trabalho dele — devem ser impecáveis e nunca expor fragilidade.
- Ele agradece à Patrícia e ao Dr. Leonardo nos documentos. **Não citar a Liz.**

---

*Documento produzido em 5 de novembro de 2026 para retomada do projeto em conversa nova.*
