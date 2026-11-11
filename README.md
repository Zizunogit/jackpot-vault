# Jackpot Vault

Acervo visual da Criação: grade infinita de personagens com zoom pela rolagem, busca, filtro por provedora e uma página por personagem com todas as imagens, organizadas por estilo e empresa.

Esta é a versão **v28** do protótipo, preparada para o GitHub Pages:

- Abre direto no acervo, **sem a tela de entrada simulada** (não pede nem valida e-mail).
- É um site estático: um `index.html` e a pasta `img/`. Não tem servidor nem instalação.
- Os dados do Drive são uma **leitura feita em 10/11/2026**. O site não lê o Drive sozinho.

## Publicar no GitHub Pages

1. Crie um repositório e envie **todo o conteúdo desta pasta** para a raiz da branch `main` (`index.html`, `img/`, `.nojekyll` e este `README.md`).
2. No repositório, abra **Settings › Pages**.
3. Em **Build and deployment**, escolha **Source: Deploy from a branch**, **Branch: `main`** e a pasta **`/ (root)`**. Clique em **Save**.
4. Em alguns minutos o endereço aparece no topo da mesma tela (`https://<usuário>.github.io/<repositório>/`).

> **Atenção:** um site do GitHub Pages é **público na internet**, mesmo quando o repositório é privado (só o GitHub Enterprise Cloud permite restringir o acesso). A página tem `noindex` para não aparecer em buscadores, mas qualquer pessoa com o link consegue abrir.

## Ver no computador antes de publicar

Os logos das provedoras não aparecem se você abrir o `index.html` com dois cliques (`file://`). Use um servidor local:

```bash
python3 -m http.server 8000
# abra http://localhost:8000
```

## O que é real e o que é simulado

| Real | Simulado |
|---|---|
| As 13 capas dos personagens V2 | Ícones, Realista, 3D e Thumb dos 13 exemplos (são marcações de volume) |
| Os 4 personagens lidos do Drive (Barba Rosa, Lucky Jaguar, Yo Dragon, Lucky Sheep) e as 26 imagens deles | Provedora dos 13 exemplos |
| "Abrir a pasta no Drive ↗" das imagens lidas do Drive e "Abrir a planilha ↗" (só abrem para quem tem acesso no Google) | Baixar, .zip, "Ler a planilha de novo" e "Abrir a pasta" dos exemplos |
| Logos das provedoras (17) | |

## Estrutura

```
index.html      página inteira: estilo, código e os dados (const ACERVO)
img/v2/f|g/     capas dos personagens (grande e pequena)
img/drive/      imagens lidas do Drive
img/prov/       logos das provedoras (silhueta branca)
.nojekyll       faz o GitHub Pages servir os arquivos como estão
```

Fontes: Schibsted Grotesk e Geist Mono, carregadas do Google Fonts.
