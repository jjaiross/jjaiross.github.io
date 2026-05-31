# Site pessoal de José Jairo de Santana e Silva

Site acadêmico e profissional construído com **Quarto** e publicado em **GitHub Pages** no endereço [jjaiross.github.io](https://jjaiross.github.io).

## Estrutura

```text
site_jose_jairo_quarto/
├── _quarto.yml                  # configuração global do site
├── styles.css                   # estilos personalizados
├── index.qmd                    # página inicial
├── about.qmd                    # sobre
├── research.qmd                 # pesquisa
├── projects.qmd                 # projetos
├── publications.qmd             # publicações
├── teaching.qmd                 # ensino (lista de disciplinas)
├── software.qmd                 # código
├── posts.qmd                    # notas (índice)
├── cv.qmd                       # currículo
├── contact.qmd                  # contato
├── disciplinas/                 # páginas individuais de cada disciplina
│   ├── visao-computacional.qmd
│   ├── modelagem-computacional.qmd
│   └── programacao-computadores.qmd
├── posts/                       # arquivos das notas (um por post)
├── images/                      # imagens do site
├── files/                       # PDFs (CV e materiais de disciplinas)
│   ├── cv_jose_jairo.pdf
│   └── disciplinas/             # PDFs organizados por disciplina
├── docs/                        # saída do Quarto (gerada por quarto render)
├── COMO_PUBLICAR.md             # instruções de publicação
└── .github/workflows/publish.yml
```

## Visualização local

Requer o **Quarto 1.9+** instalado.

```bash
# servidor local com recarregamento automático
quarto preview

# renderização do site completo na pasta docs/
quarto render

# renderização de uma página específica
quarto render publications.qmd
```

## Publicação no GitHub Pages

O site é publicado automaticamente pelo **GitHub Actions** (`.github/workflows/publish.yml`) a cada `git push` na branch `main`.

Fluxo padrão de atualização:

```bash
# 1. edite o(s) .qmd desejado(s)
# 2. teste localmente com quarto preview
# 3. commit e push
git add <arquivos>
git commit -m "mensagem descritiva"
git push
```

O workflow renderiza o Quarto e publica em `https://jjaiross.github.io` em alguns minutos.

## Como adicionar conteúdo

### Nova publicação

Edite `publications.qmd` adicionando uma entrada com título, autores, periódico, DOI e descrição. Use o padrão das entradas existentes.

### Nova disciplina

1. Crie `disciplinas/<nome-da-disciplina>.qmd` com front matter `title`, `description` e listas de slides e conteúdos.
2. Coloque os PDFs em `files/disciplinas/<nome-da-disciplina>/`.
3. Adicione um `.card` em `teaching.qmd` apontando para a página criada.

Use **nomes sem acentos e sem espaços** nas pastas e arquivos (ex.: `programacao-computadores`) para evitar problemas de URL.

### Nova nota (post)

Crie `posts/<ano-mes-dia-slug>.qmd` com front matter `title`, `date`, `description` e `categories`. O índice em `posts.qmd` lista automaticamente em ordem decrescente.

### Trocar CV em PDF

Substitua o arquivo `files/cv_jose_jairo.pdf` pelo novo. O link em `cv.qmd` não precisa ser alterado.

### Trocar imagem de perfil

Substitua `images/foto-jose-jairo.jpeg` pelo novo arquivo com o mesmo nome (ou edite a referência em `index.qmd`).

## Observações

- A pasta `docs/` é gerada automaticamente pelo Quarto e contém o site renderizado servido pelo GitHub Pages.
- O front matter YAML no topo de cada `.qmd` controla título, descrição (usada em meta tags e Open Graph) e outras opções.
- Para detalhes adicionais de publicação, consulte `COMO_PUBLICAR.md`.
