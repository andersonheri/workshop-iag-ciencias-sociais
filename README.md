# Introdução à Inteligência Artificial Generativa nas Ciências Sociais

Material didático do mini curso do **CEM/USP** (Centro de Estudos da Metrópole) sobre uso responsável de IA generativa em pesquisa, ensino e escrita acadêmica em Ciências Sociais. Formato: 2 dias, 8h00–12h30, nível introdutório, independente de plataforma.

- **Autor:** Anderson Henrique
- **Vínculo:** CEM/USP • INCT QualiGov • Pesquisador Convidado IPEA • Doutor em Ciência Política pela UFPE
- **Contato:** andersonheri@gmail.com
- **Financiamento:** Fundação de Amparo à Pesquisa do Estado de São Paulo (FAPESP), processo 2025/15250-0
- **Edição:** 1ª edição, 2026

## Conteúdo do repositório

```
├── slides/     Slides do mini curso (Beamer, 2 dias)
│   ├── workshop-iag-ciencias-sociais.tex
│   ├── workshop-iag-ciencias-sociais.pdf
│   └── assets/           (logo do CEM usada na capa)
└── .gitignore
```

> O guia de bolso ("Kit de Sobrevivência do Cientista Social com IA") foi retirado temporariamente do repositório para ajustes e volta assim que a revisão for concluída.

### Slides — `slides/workshop-iag-ciencias-sociais.tex`

Apresentação em Beamer com a estrutura do curso:

- **Dia 1 — Entender e decidir** (8h00–12h30): vocabulário essencial de IA generativa, quando usar (e quando não usar), epistemologia e limites.
- **Dia 2 — Praticar e aplicar** (8h00–12h30): fluxos de trabalho práticos de pesquisa, ensino e escrita com IA, exercícios guiados e referências.

Compila com **pdflatex** (tema Madrid, cores institucionais do CEM, sem dependência de fontes externas).

## Material complementar

- **Vídeo:** ["A curiosa linha do tempo da evolução da Inteligência Artificial"](https://youtu.be/SkX6MKU9gAQ), BBC Brasil (YouTube). Linkado aqui, e não hospedado no repositório, por ser conteúdo de terceiros protegido por direitos autorais.

## Como compilar

Pré-requisitos: uma distribuição LaTeX (ex. [MiKTeX](https://miktex.org/) ou TeX Live) com `pdflatex` disponível no PATH.

```bash
# Slides (Dia 1 e Dia 2)
cd slides
pdflatex -interaction=nonstopmode workshop-iag-ciencias-sociais.tex
pdflatex -interaction=nonstopmode workshop-iag-ciencias-sociais.tex   # 2ª rodada, acerta sumário/links
```

O PDF compilado já está versionado neste repositório para consulta direta, sem necessidade de compilar localmente.

## Declaração de uso de IA

Registramos aqui o uso de IA na preparação *deste repositório* (não do conteúdo pedagógico em si, de autoria integral do autor):

> Este repositório foi organizado com apoio do Claude (Anthropic), via Claude Code, em agosto de 2026, sob supervisão direta do autor. Uso que apoiou tarefas operacionais: instalação e configuração do ambiente de compilação LaTeX (MiKTeX, fonte Poppins) e do GitHub CLI; compilação e verificação de que os documentos `.tex` geram PDF sem erros; reestruturação dos arquivos em `slides/` e `handout/`; redação deste README; criação do repositório e push inicial no GitHub. O conteúdo intelectual dos slides e do guia de bolso não foi gerado por IA. Todas as saídas foram revisadas e aprovadas pelo autor, que se responsabiliza integralmente pelo conteúdo final.
