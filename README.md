# Introdução à Inteligência Artificial Generativa nas Ciências Sociais

Material didático do minicurso do **CEM/USP** (Centro de Estudos da Metrópole) sobre uso responsável de IA generativa em pesquisa, ensino e escrita acadêmica em Ciências Sociais. Formato: 2 dias, 8h00–12h30, nível introdutório, independente de plataforma.

- **Autor:** Anderson Henrique
- **Vínculo:** CEM/USP • INCT QualiGov • Pesquisador Convidado IPEA • Doutor em Ciência Política pela UFPE
- **Site:** [ahenriquecp.com](https://www.ahenriquecp.com)
- **Contato:** andersonheri@gmail.com
- **Financiamento:** Fundação de Amparo à Pesquisa do Estado de São Paulo (FAPESP), processo 2025/15250-0
- **Edição:** 1ª edição, 2026

## Conteúdo do repositório

```
├── slides/     Slides do minicurso (Beamer, 2 dias)
│   ├── workshop-iag-ciencias-sociais.tex
│   ├── workshop-iag-ciencias-sociais.pdf
│   └── assets/           (logo do CEM usada na capa)
├── handout/    Manual de Sobrevivência, guia de bolso complementar às aulas
│   ├── manual_sobrevivencia.tex
│   ├── manual-sobrevivencia-cientista-social-ia.pdf
│   └── assets/           (logo e marca do CEM usados no manual)
└── .gitignore
```

### Slides — `slides/workshop-iag-ciencias-sociais.tex`

Apresentação em Beamer com a estrutura do curso:

- **Dia 1 — Entender e decidir** (8h00–12h30): vocabulário essencial de IA generativa, quando usar (e quando não usar), epistemologia e limites.
- **Dia 2 — Praticar e aplicar** (8h00–12h30): fluxos de trabalho práticos de pesquisa, ensino e escrita com IA, exercícios guiados e referências.

Compila com **pdflatex** (tema Madrid, cores institucionais do CEM, sem dependência de fontes externas). Ao todo, **7 exercícios práticos (hands-on)** distribuídos pelos dois dias — 1 no Dia 1 e 6 no Dia 2, um por módulo de M5 a M9 —, além de slides revisados para privilegiar tópicos curtos em vez de parágrafos corridos.

### Manual de Sobrevivência — `handout/manual_sobrevivencia.tex`

"Manual de Sobrevivência do Cientista Social com IA": guia de bolso complementar às aulas, pensado para consulta rápida no momento de uso — glossário, quando usar cada ferramenta, ~29 modelos de prompt prontos e modelo de declaração de uso de IA para manuscritos.

Compila com **xelatex** e usa a fonte **Poppins** (Google Fonts, licença OFL) para os títulos.

> **Uso e licença do conteúdo:** material de uso educacional. Reprodução e compartilhamento livres para fins não comerciais, desde que citada a fonte.
>
> **Como citar:** HENRIQUE, Anderson. *Manual de sobrevivência do cientista social com IA*: manual prático. São Paulo: Centro de Estudos da Metrópole (CEM/USP), 2026. DOI: [10.5281/zenodo.21982080](https://doi.org/10.5281/zenodo.21982080).

## Material complementar

- **Vídeo:** ["A curiosa linha do tempo da evolução da Inteligência Artificial"](https://youtu.be/SkX6MKU9gAQ), BBC Brasil (YouTube). Linkado aqui, e não hospedado no repositório, por ser conteúdo de terceiros protegido por direitos autorais.

## Como compilar

Pré-requisitos: uma distribuição LaTeX (ex. [MiKTeX](https://miktex.org/) ou TeX Live) com `xelatex` e `pdflatex` disponíveis no PATH.

O manual (`handout/manual_sobrevivencia.tex`) usa a fonte **Poppins**, que não vem pré-instalada no sistema. Baixe a família em [Google Fonts](https://fonts.google.com/specimen/Poppins) e instale-a antes de compilar (sem isso, o `fontspec` falha ao localizar a fonte).

```bash
# Slides (Dia 1 e Dia 2)
cd slides
pdflatex -interaction=nonstopmode workshop-iag-ciencias-sociais.tex
pdflatex -interaction=nonstopmode workshop-iag-ciencias-sociais.tex   # 2ª rodada, acerta sumário/links

# Manual de Sobrevivência
cd ../handout
xelatex -interaction=nonstopmode manual_sobrevivencia.tex
xelatex -interaction=nonstopmode manual_sobrevivencia.tex   # 2ª rodada, acerta sumário/links
```

Os PDFs compilados já estão versionados neste repositório para consulta direta, sem necessidade de compilar localmente.

## Declaração de uso de IA

Registramos aqui o uso de IA na preparação *deste repositório* (não do conteúdo pedagógico em si, de autoria integral do autor — o manual traz sua própria declaração de uso de IA na ficha técnica):

> Este repositório foi organizado com apoio do Claude (Anthropic), via Claude Code, entre agosto de 2026, sob supervisão direta do autor. Uso que apoiou tarefas operacionais: instalação e configuração do ambiente de compilação LaTeX (MiKTeX, fonte Poppins) e do GitHub CLI; compilação e verificação de que os documentos `.tex` geram PDF sem erros; reestruturação e limpeza dos arquivos em `slides/` e `handout/`; revisão de conteúdo dos slides do Dia 2 (densidade de texto e cobertura de exercícios práticos), com os ajustes aplicados sob orientação e aprovação do autor; redação deste README; criação do repositório e dos commits no GitHub. O conteúdo intelectual dos slides e do manual não foi gerado por IA. Todas as saídas foram revisadas e aprovadas pelo autor, que se responsabiliza integralmente pelo conteúdo final.
