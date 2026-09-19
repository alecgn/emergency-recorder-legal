# Emergency Recorder — documentos públicos

Este repositório existe por um motivo só: **hospedar a política de privacidade** do
aplicativo Emergency Recorder em uma URL pública, via GitHub Pages.

O código do aplicativo é privado e fica em outro repositório. Aqui não há código —
apenas a página publicada.

## Por que um repositório separado

O GitHub Pages só funciona em repositórios públicos nas contas gratuitas. Tornar o
repositório do aplicativo público apenas para publicar uma página seria expor o código
inteiro por uma exigência de formulário.

## Como a página é gerada

O texto é mantido em `docs/politica-de-privacidade.md`, **no repositório do
aplicativo**, versionado junto com o código que ele descreve. O `index.html` deste
repositório é gerado a partir dele:

```
python tool/build_privacy_page.py ../emergency-recorder-legal
```

Não edite o `index.html` à mão. Duas cópias de um documento legal viram, com o tempo,
duas políticas diferentes — e a que está publicada é a que vale para quem lê.

## Não apague o arquivo de verificação

`googleb14c453426e6868e.html` prova ao Google que este site é nosso. É o que permite
a tela de consentimento OAuth exibir a marca do aplicativo. Ele não é gerado pelo
script e não tem conteúdo útil — apagá-lo derruba a verificação silenciosamente, e o
sintoma só aparece na próxima revisão do Google.

## Página publicada

<https://alecgn.github.io/emergency-recorder-legal/>
