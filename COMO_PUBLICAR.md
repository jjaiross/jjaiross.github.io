# Como publicar este site no GitHub Pages

Este guia é o caminho mais direto.

## 1. Descompacte o arquivo

Descompacte o `.zip` em uma pasta, por exemplo:

```bash
cd ~/Documentos
unzip site_jose_jairo_quarto.zip
cd site_jose_jairo_quarto
```

## 2. Crie o repositório no GitHub

No GitHub, crie um repositório chamado:

```text
jjaiross.github.io
```

Deixe como público.

## 3. Envie os arquivos

Dentro da pasta do projeto, rode:

```bash
git init
git add .
git commit -m "Create personal website"
git branch -M main
git remote add origin https://github.com/jjaiross/jjaiross.github.io.git
git push -u origin main
```

## 4. Configure o GitHub Pages

No GitHub:

```text
Settings > Pages > Build and deployment > Source > GitHub Actions
```

Depois salve.

## 5. Aguarde o GitHub Actions

Vá na aba:

```text
Actions
```

Se estiver tudo certo, aparecerá um processo chamado:

```text
Publish Quarto Website
```

Quando ele terminar, o site ficará disponível em:

```text
https://jjaiross.github.io
```

## 6. Para alterar depois

Edite qualquer arquivo `.qmd`, por exemplo `index.qmd`.

Depois rode:

```bash
git add .
git commit -m "Update website"
git push
```

O GitHub vai atualizar o site automaticamente.
