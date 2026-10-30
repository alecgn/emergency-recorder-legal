# Emergency Recorder — documentos públicos

Este repositório existe por um motivo só: **hospedar os documentos públicos** do
aplicativo Emergency Recorder — página inicial, política de privacidade e termos de
serviço — em uma URL pública, via GitHub Pages.

O código do aplicativo é privado e fica em outro repositório. Aqui não há código —
apenas a página publicada.

## Por que um repositório separado

O GitHub Pages só funciona em repositórios públicos nas contas gratuitas. Tornar o
repositório do aplicativo público apenas para publicar uma página seria expor o código
inteiro por uma exigência de formulário.

## Como as páginas são geradas

São três páginas — início, política de privacidade e termos de serviço —, as exigidas
pela tela de consentimento OAuth do Google. O texto de cada uma é mantido em `docs/`,
**no repositório do aplicativo**, versionado junto com o código que ele descreve:

| Página | Origem |
|---|---|
| `index.html` | `docs/pagina-inicial.md` |
| `privacidade.html` | `docs/politica-de-privacidade.md` |
| `termos.html` | `docs/termos-de-servico.md` |

Para gerar, a partir da raiz do repositório do aplicativo:

```
pip install markdown pillow
python tool/build_site.py ../emergency-recorder-legal
```

Não edite os `.html` à mão. Duas cópias de um documento legal viram, com o tempo,
dois documentos diferentes — e o que está publicado é o que vale para quem lê.

## Não apague o arquivo de verificação

`googleb14c453426e6868e.html` prova ao Google que este site é nosso. É o que permite
a tela de consentimento OAuth exibir a marca do aplicativo. Ele não é gerado pelo
script e não tem conteúdo útil — apagá-lo derruba a verificação silenciosamente, e o
sintoma só aparece na próxima revisão do Google.

## Não apague os vídeos de demonstração

`videos/FOREGROUND_SERVICE_CAMERA.mp4` e `videos/FOREGROUND_SERVICE_MICROPHONE.mp4` são os
vídeos que a declaração de serviço em primeiro plano do Play Console aponta. Apagá-los ou
renomeá-los quebra o link dessa declaração, e o sintoma só aparece quando a Play reanalisar
o app. Para trocar um vídeo, substitua o arquivo **mantendo o nome**.

## Página publicada

<https://alecgn.github.io/emergency-recorder-legal/>
