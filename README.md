# Vinycius Moraes — Estúdio HyperFrames

Repositório de **testes técnicos de vídeos imobiliários** com [HyperFrames](https://github.com/heygen-com/hyperframes) (renderizador oficial). Separado do portal de locações.

## Resultado confirmado (1/11/2026)

O GitHub Actions executou com sucesso o [benchmark oficial nº 41370565561](https://github.com/Vinycius2611/Video/actions/runs/41370565561) e publicou o [pacote com os três MP4s e laudos](https://github.com/Vinycius2611/Video/actions/runs/41370565561/artifacts/13108069878). Foram usados Node 22, Chromium Headless e FFmpeg; a CLI foi invocada como `npx hyperframes@latest`.

| Perfil | Resolução | Quadros/s | Duração | Codec de vídeo | Áudio | Tamanho real |
| --- | --- | --- | --- | --- | --- | --- |
| A `looks` | 1080×1920 | 30 | 5 s | H.264 | AAC 48 kHz, estéreo | 1.386.791 bytes |
| B `delivery` | 1080×1920 | 60 | 5 s | H.264 | AAC 48 kHz, estéreo | 1.880.048 bytes |
| C `looks` 4K | 2160×3840 | 30 | 5 s | H.264 | AAC 48 kHz, estéreo | 3.711.104 bytes |

O relatório `reports/relatorio.json` e os três quadros de revisão foram gerados no próprio runner, inspecionados depois. O teste 4K concluiu dentro do limite de quatro minutos. São cenas **fictícias de demonstração**, sem fotos ou vídeos reais do imóvel. O som é um **tom de teste**, não uma narração pronta.

## Próxima produção: Casa Costa Verde

- Recomenda-se **1080×1920**, **30 FPS** se a mídia original for de 30 FPS; usar 60 FPS somente quando a fonte ou a animação exigirem.
- Aumentar para 4K não revela detalhes inexistentes no vídeo original, embora a composição gráfica possa ser nativa em 4K.
- A composição de teste `tests/premium/index.html` contém geometria com faces no espaço 3D via CSS, câmera em perspectiva, luz móvel, piscina fictícia e tipografia animada. **Não é reconstrução 3D fiel da casa**.
- Para edição imobiliária final, incorporar imagens reais em cenário de composição, preservar plantas e características reais, revisar o texto em área segura, sincronizar cortes/voz/trilha, e conferir o MP4 renderizado.

## Arquivos

- `index.html`: primeira demonstração técnica, 540×960 / 24 FPS.
- `tests/premium/index.html`: demonstração premium 1080×1920 / 5 segundos.
- `.github/workflows/render-hyperframes.yml`: executa o benchmark automaticamente após mudanças relevantes e também por disparo manual.

## Obter vídeos

1. Abra a aba [Actions](https://github.com/Vinycius2611/Video/actions).
2. Abra a execução **Laboratório HyperFrames - perfis de qualidade**.
3. Na área **Artifacts**, clique em `hyperframes-benchmark-premium`.
4. Extraia o ZIP para receber `renders/*.mp4` e `reports/*`.

Este repositório é público. **Não envie vídeos brutos privados, fotos pessoais, áudios originais, credenciais ou material confidencial** sem avaliar privacidade e direitos de uso.
