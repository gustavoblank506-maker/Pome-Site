# Pome — site

A página oficial do [Pome](https://gustavoblank506-maker.github.io/Pome-Site/) e o
lugar de onde o instalador é baixado.

O **código do aplicativo não está aqui** — este repositório é público porque um
site e um binário precisam ser públicos, e o app é produto comercial.

## Não edite estes arquivos à mão

`termos.html`, `privacidade.html`, `assets/tokens.css` e `assets/versao.js` são
**gerados** a partir do repositório do aplicativo, por `npm run site`:

| Arquivo | De onde vem |
|---|---|
| `termos.html`, `privacidade.html` | `src/data/legal.ts` — a mesma fonte que o app mostra na tela |
| `assets/tokens.css` | `src/theme/tokens.ts` — a paleta da marca |
| `assets/versao.js` | Medido do próprio instalador: versão, tamanho e SHA-256 |

Editar aqui cria uma segunda versão da mesma promessa, e a próxima geração
apaga a edição. Para mudar qualquer um deles, muda-se o aplicativo.

## Publicar uma versão nova

No repositório do app: `npm run dist`, depois `npm run site` — nessa ordem, porque
o segundo mede o arquivo que o primeiro gera. Copiar `site/` para cá, commitar, e
criar a release com a tag `v<versão>` anexando `Pome-<versão>-instalador.exe` com
o nome exato.

---

© 2026 Gustavo. Todos os direitos reservados.
