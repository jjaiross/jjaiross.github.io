# Site pessoal — José Jairo de Santana e Silva

Este repositório contém um site pessoal/acadêmico feito com **Quarto** e preparado para ser publicado no **GitHub Pages**.

## Estrutura

```text
site_jose_jairo_quarto/
├── _quarto.yml
├── index.qmd
├── about.qmd
├── research.qmd
├── projects.qmd
├── publications.qmd
├── teaching.qmd
├── software.qmd
├── posts.qmd
├── cv.qmd
├── contact.qmd
├── styles.css
├── images/
├── files/
├── posts/
└── .github/workflows/publish.yml
```

## O que editar primeiro

Edite nesta ordem:

1. `index.qmd` — página inicial.
2. `about.qmd` — sobre você.
3. `projects.qmd` — seus projetos.
4. `publications.qmd` — suas publicações.
5. `teaching.qmd` — disciplinas e materiais.
6. `cv.qmd` — currículo.
7. `contact.qmd` — contato.

## Como publicar no GitHub

### 1. Crie um repositório no GitHub

Crie um repositório com o nome:

```text
josejairo.github.io
```

Se seu usuário do GitHub for outro, use:

```text
SEU_USUARIO.github.io
```

### 2. Envie os arquivos para o GitHub

Dentro da pasta deste projeto, rode:

```bash
git init
git add .
git commit -m "Create personal website"
git branch -M main
git remote add origin https://github.com/jjaiross/josejairo.github.io.git
git push -u origin main
```

Troque `jjaiross` pelo seu usuário do GitHub, se for diferente.

### 3. Configure o GitHub Pages

No GitHub:

1. Entre no repositório.
2. Vá em **Settings**.
3. Vá em **Pages**.
4. Em **Build and deployment**, escolha **GitHub Actions**.
5. Salve.

O arquivo `.github/workflows/publish.yml` vai renderizar o site automaticamente.

### 4. Acesse o site

Depois de alguns minutos, o site deve aparecer em:

```text
https://jjaiross.github.io/josejairo.github.io/
```

## Como testar localmente com Quarto

Se tiver o Quarto instalado, rode:

```bash
quarto preview
```

Para gerar os arquivos HTML:

```bash
quarto render
```

## Observações

- A pasta `docs/` será criada automaticamente quando o site for renderizado.
- A publicação pelo GitHub Actions não exige que você rode `quarto render` no seu computador.
- Para trocar a imagem de perfil, coloque sua foto em `images/` e edite o arquivo `index.qmd`.
- Para colocar seu CV em PDF, salve o arquivo dentro de `files/` e edite `cv.qmd`.
