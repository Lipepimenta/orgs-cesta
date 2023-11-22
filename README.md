# ReactNative

## Instalação do Node.JS
O primeiro passo é instalar o Node.JS. Recomendo a versão LTS, que é a versão mais estável do Node.
- Detalhes da instalação na última etapa: "autorize instalar todas as ferramentas necessárias e next".
- Após a instalação, abra o terminal e digite "node --version" para verificar se a instalação ocorreu corretamente.

## Instalação do Expo
Assim que o Node estiver instalado, acesse o [site do Expo](https://docs.expo.dev/get-started/installation/). Para as últimas versões, o Expo mudou, siga as informações disponíveis no [blog](https://blog.expo.dev/the-new-expo-cli-f4250d8e3421) para instalar o Expo. Após a instalação, vamos criar um projeto.

Para criar um projeto, abra o PowerShell, acesse a pasta desejada e digite:

Escolha o tipo de arquivo (por exemplo, *blank*), pressione Enter e aguarde a criação do projeto. Em seguida, abra a pasta no VSCode.

## Como rodar o emulador no celular fora da rede

Para executar o código no emulador do celular fora da mesma rede, ajuste as configurações no `package.json` para tunnel.

Ao usar o comando `npm start` no terminal do VSCode, a página da web não abre devido a mudanças recentes. Para contornar esse problema, adicione as seguintes linhas dentro de "scripts" no `package.json`:
```json
"scripts": {
  "start": "expo start --tunnel",
  "android": "expo start --android",
  "ios": "expo start --ios",
  "web": "expo start --web",
  "eject": "expo eject"
}

Após salvar o arquivo, abra o terminal no VSCode, digite "npm start" e pressione Enter. Responda "y" (yes) para utilizar a porta de acesso informada e instalar o package, se necessário.

Observação: Se o PC estiver na mesma rede Wi-Fi do celular, essa configuração não é necessária.
