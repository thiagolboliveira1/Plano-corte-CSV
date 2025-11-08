# Plano de Corte • CSV — Instalação no iPhone (como app)

Você tem duas formas de usar no iPhone:

## A) Rápida (local, sem publicar)
1. Baixe o ZIP e extraia no app **Arquivos** (iCloud Drive ou No Meu iPhone).
2. Abra a pasta e toque em **index.html**.
3. Toque no botão de **compartilhar** e escolha **Abrir no Safari** (se aparecer).
4. No Safari, toque em **Compartilhar → Adicionar à Tela de Início**.
5. Abra o atalho criado — vai funcionar como um app (web app).

> Observação: em alguns iPhones, abrir o `index.html` direto do Arquivos exibe “Pré-visualização”. Procure a opção **Abrir no Safari**. Se não aparecer, use a opção B abaixo.

## B) Publicando (recomendado — funciona offline e instala como app)
1. Crie uma conta no **GitHub** (se ainda não tiver).
2. No GitHub, crie um repositório novo: `plano-corte-csv`.
3. Envie **todos os arquivos** desta pasta (index.html, index_pwa.html, manifest.json, service-worker.js, pasta icons).
4. Vá em **Settings → Pages → Source: Deploy from a branch**, selecione **main** e a pasta **/(root)**. Salve.
5. Abra a URL do GitHub Pages que aparecer (algo como `https://seuusuario.github.io/plano-corte-csv/`).
6. No iPhone, abra essa URL no **Safari**, toque em **Compartilhar → Adicionar à Tela de Início**.
7. Abra o atalho instalado. O service worker vai manter os arquivos em cache (funciona offline).

## Sobre exportar no Safari
- O botão **Exportar CSV** usa um caminho compatível com Safari: tenta download direto; se bloquear, usa `data:` na mesma aba; se precisar, abre o conteúdo em texto para você **Salvar em Arquivos**.
- Se o Safari bloquear pop-ups, o método já tenta **não abrir nova aba**. Se ainda assim bloquear, desative temporariamente em **Ajustes → Safari → Bloquear Pop-ups** e exporte novamente.

## Dicas
- O app salva seu histórico e preferências no **localStorage** (no próprio iPhone, por navegador).
- Os números são exportados **exatamente como digitados** (não converto vírgula/ponto).
- Para rodar os testes, no Safari (em um Mac) abra o console e rode: `tests.runAll()`.

Bom uso!
