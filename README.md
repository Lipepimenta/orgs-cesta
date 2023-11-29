# ReactNative

## Instalação do Node.JS
O primeiro passo é instalar o Node.JS. Recomendo a versão LTS, que é a versão mais estável do Node.
- Detalhes da instalação na última etapa: "autorize instalar todas as ferramentas necessárias e next".
- Após a instalação, abra o terminal e digite "node --version" para verificar se a instalação ocorreu corretamente.

## Configuração do Ambiente para Projeto Expo React Native

Antes de começar, certifique-se de ter o Node.js instalado e o ambiente Android Studio/emulador configurado.

1. Abra o terminal como administrador e execute o seguinte comando para criar um novo projeto Expo React Native:

    ```bash
    npx create-expo-app nome_da_pasta
    ```

2. Após criar a pasta, abra o emulador do Android Studio e, em seguida, abra o projeto no Visual Studio Code.

3. No terminal do Visual Studio Code, verifique se o ambiente Expo está funcionando. Execute o comando que foi exibido no terminal ao criar o projeto, por exemplo:

    ```bash
    npm run android
    ```

    Isso iniciará o código no emulador Android aberto.

4. Certifique-se de que tudo está funcionando corretamente antes de prosseguir.

5. Instale a biblioteca de navegação para facilitar a transição entre páginas. Encerre o emulador e execute os seguintes comandos um de cada vez no terminal do Visual Studio Code:

    ```bash
    npm install @react-navigation/native
    ```
     ```bash
    npx expo install react-native-screens react-native-safe-area-context
    ```
      ```bash
    npm install @react-navigation/native-stack
    ```

6. Agora seu projeto está configurado para suportar navegação entre páginas.

7. Reinicie o emulador e continue desenvolvendo seu projeto!

Lembre-se, o comando `npm run android` pode ser substituído por `npm run ios` se estiver desenvolvendo para iOS.


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
```
Após salvar o arquivo, abra o terminal no VSCode, digite "npm start" e pressione Enter. Responda "y" (yes) para utilizar a porta de acesso informada e instalar o package, se necessário.

*Observação:* Se o PC estiver na mesma rede Wi-Fi do celular, essa configuração não é necessária.

## Vídeos Úteis

Aqui estão alguns vídeos que podem ajudá-lo na configuração do ambiente:

- [Configurando o Ambiente Expo React Native](https://www.youtube.com/watch?v=1Bwp1BzYLx0)
- [Guia Detalhado para Iniciar com React Navigation](https://www.youtube.com/watch?v=1IpmTcN4JvY)
