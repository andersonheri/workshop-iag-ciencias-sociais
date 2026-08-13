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
│   └── workshop-iag-ciencias-sociais.pdf
├── handout/    Guia de bolso complementar às aulas
│   ├── kit_sobrevivencia.tex
│   ├── kit-sobrevivencia-cientista-social-ia.pdf
│   └── assets/           (logo e marca do CEM usados no guia)
└── .gitignore
```

### Slides — `slides/workshop-iag-ciencias-sociais.tex`

Apresentação em Beamer com a estrutura do curso:

- **Dia 1 — Entender e decidir** (8h00–12h30): vocabulário essencial de IA generativa, quando usar (e quando não usar), epistemologia e limites.
- **Dia 2 — Praticar e aplicar** (8h00–12h30): fluxos de trabalho práticos de pesquisa, ensino e escrita com IA, exercícios guiados e referências.

Compila com **pdflatex** (tema Madrid, cores institucionais do CEM, sem dependência de fontes externas).

### Guia de bolso — `handout/kit_sobrevivencia.tex`

Manual prático complementar às aulas — "Kit de Sobrevivência do Cientista Social com IA" — pensado para consulta rápida no momento de uso: glossário, quando usar cada ferramenta, modelos de prompt prontos e modelo de declaração de uso de IA para manuscritos.

Compila com **xelatex** e usa a fonte **Poppins** (Google Fonts, licença OFL) para os títulos.

> **Uso e licença do conteúdo:** material de uso educacional. Reprodução e compartilhamento livres para fins não comerciais, desde que citada a fonte.
>
> **Como citar:** HENRIQUE, Anderson. *Kit de sobrevivência do cientista social com IA*: manual prático. São Paulo: Centro de Estudos da Metrópole (CEM/USP), 2026.

## Como compilar

Pré-requisitos: uma distribuição LaTeX (ex. [MiKTeX](https://miktex.org/) ou TeX Live) com `xelatex` e `pdflatex` disponíveis no PATH.

O guia de bolso (`handout/kit_sobrevivencia.tex`) usa a fonte **Poppins**, que não vem pré-instalada no sistema. Baixe a família em [Google Fonts](https://fonts.google.com/specimen/Poppins) e instale-a antes de compilar (sem isso, o `fontspec` falha ao localizar a fonte).

```bash
# Slides (Dia 1 e Dia 2)
cd slides
pdflatex -interaction=nonstopmode workshop-iag-ciencias-sociais.tex
pdflatex -interaction=nonstopmode workshop-iag-ciencias-sociais.tex   # 2ª rodada, acerta sumário/links

# Guia de bolso
cd ../handout
xelatex -interaction=nonstopmode kit_sobrevivencia.tex
xelatex -interaction=nonstopmode kit_sobrevivencia.tex   # 2ª rodada, acerta sumário/links
```

Os PDFs compilados já estão versionados neste repositório para consulta direta, sem necessidade de compilar localmente.
