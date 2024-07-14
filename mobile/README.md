## Configuração para Rodar o Build

- Sem Android Studio (Software) - apenas CommandLine.
- Neste `README.md` contém as instruções para preparar o ambiente Windows e celular Android para rodar o APK no aparelho.

### Instalações:

1. [Node.js via NVM](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating)
    - 1.1. `nvm list`
    - 1.2. `nvm install 20.11.0`
    - 1.3. `nvm use 20.11.0`
2. Python2
    - 2.1. `npm install --python=python2.7`
    - 2.2. `npm config set python python2.7`
3. Yarn
    - 3.1. `npm install --global yarn`
    - 3.2. `yarn global add react-native-cli`
4. [Java JDK](https://www.oracle.com/br/java/technologies/downloads/)
    - 4.1. Configurar a variável de ambiente:
        Nome: `JAVA_HOME`
        Caminho: `C:\Program Files\Java\jdk-21`
5. [Android SDK Manager CLI](https://developer.android.com/studio/index.html)
    - 5.1. Extrair para a pasta `C:/dev`
    - 5.2. Adicionar na variável de ambiente `path` do usuário:
        Caminho: `C:\dev\commandlinetools-win-11076708_latest\bin`
    - 5.3. Configurar a variável de ambiente:
        Nome: `ANDROID_HOME`
        Caminho: `C:\Users\SEU_USUARIO\AppData\Local\Android\Sdk`
    - 5.4. Para verificar se funcionou, rodar `sdkmanager` no PowerShell.
6. [ADB](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)
    - 5.1. Extrair para a pasta `C:/dev`
    - 5.2. Adicionar na variável de ambiente `path` do usuário:
        Caminho: `C:\dev\platform-tools-latest-windows`
    - 5.3. Para verificar se funcionou, rodar `adb` no PowerShell.

### Feito as configurações, será possível rodar o projeto via Development Build:

- Lembrar de Habilitar "USB Debugging" no Celular. 
- `npx expo prebuild`
- `npx expo run:android`

- Obs: orientações seguidas de [kingsukhoi/installreactnative.md](https://gist.github.com/kingsukhoi/338b0ca3aa98f0a3d05d1c3a0ebe2d20)