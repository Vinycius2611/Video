# Estúdio de Vídeo — Vinycius Moraes

Repositório dedicado à produção de vídeos imobiliários com **HyperFrames**, separado do portal imobiliário.

## Teste inicial

- `index.html`: composição demonstrativa de 6 segundos em 9:16 (540 × 960, 24 fps), com animação determinística e tipografia.
- `.github/workflows/render-hyperframes.yml`: tenta renderizar com a CLI oficial do HyperFrames em um executor do GitHub Actions e disponibilizar o MP4 como **artifact**.
- A demonstração não contém imagens reais da Casa Costa Verde. A intenção é **comprovar que o HyperFrames realmente executa na nuvem antes de carregar arquivos reais**.
- Valor exibido somente como exemplo da locação anunciada; não é um anúncio pronto para publicação.

### Renderização local (opcional, não necessária no PC do usuário)

```sh
npx --yes hyperframes@latest check --json
npx --yes hyperframes@latest render --quality draft --fps 24 --output renders/TESTE_HYPERFRAMES.mp4
```

### Baixar o teste no GitHub

Abra a aba **Actions** → **Teste HyperFrames / MP4** → execução mais recente → **Artifacts** → `teste-hyperframes-mp4`.

O trabalho inicial foi preparado pelo ChatGPT com autorização do proprietário do repositório em 1/11/2026. Sem mídia pessoal neste repositório público.
