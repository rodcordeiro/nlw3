# Atualização (versões diferentes)

Nessa seção iremos ensinar a atualizar utilizando os mesmos métodos vistos na seção **Instalação**.

## Node e npm

Se você já possui Node na versão 12, não é preciso instalar nem atualizar

### Linux (Ubuntu)

Para atualizar o seu Node e npm utilizando o **NodeSource**, siga os passos:

- Existem dois casos que você pode se deparar:
    - **Caso 1**: você já tem o Node 12 (LTS mais recente), mas desatualizado.

    Basta atualizar utilizando os clássicos comandos:

    ```json
    sudo apt-get update && sudo apt-get upgrade
    ```

    - Em seguida, rode os comandos:

    ```bash
    node -v
    npm -v
    ```

    Caso estejam nas versões 12.18.3 e 6.14.6, respectivamente, a atualização ocorreu com sucesso.

    ---

    - Caso 2: você tem um Node em outra versão que não seja a LTS mais recente (12).

    Primeiramente é preciso desinstalar o Node:

    ```json
    sudo apt-get remove nodejs
    ```

    Em seguida, é preciso remover o Node do pacote de dependências. Aperte a tecla `Windows` e busque pela opção **Software & Updates**. Clique na aba **Other Software** e procure na lista pelas dependências do Node referente a versão que você quer remover. Abaixo segue um exemplo de como apareceria no caso da versão 10 do Node:

    ![Atualizac%CC%A7a%CC%83o%20(verso%CC%83es%20diferentes)%20808149db41194693ab72e142bd63bf4e/Untitled.png](Atualizac%CC%A7a%CC%83o%20(verso%CC%83es%20diferentes)%20808149db41194693ab72e142bd63bf4e/Untitled.png)

    Selecione ambas e clique no botão **Remove**. Feche a janela e aceita a opção de atualizar as informações clicando no botão **Reload**.

    ![Atualizac%CC%A7a%CC%83o%20(verso%CC%83es%20diferentes)%20808149db41194693ab72e142bd63bf4e/Untitled%201.png](Atualizac%CC%A7a%CC%83o%20(verso%CC%83es%20diferentes)%20808149db41194693ab72e142bd63bf4e/Untitled%201.png)

    Após remover ambas as dependências, abra o terminal e execute os comandos:

    ```bash
    curl -sL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
    sudo apt-get install -y nodejs
    ```

    Por fim, rode os comandos:

    ```bash
    node -v
    npm -v
    ```

    Caso estejam nas versões 12.18.3 e 6.14.6, respectivamente, a atualização ocorreu com sucesso.

### macOS

Para atualizar o seu Node e npm utilizando o **Homebrew**, siga os passos:

- Remova o Node da sua máquina:

```bash
brew uninstall node
```

- Atualize o brew e instale a versão LTS mais recente (12)

```bash
brew update
brew install node@12
```

- Como instalamos uma versão do Node diferente da default do Homebrew (o padrão é a current, nesse caso v14), é preciso adicionar manualmente o `path` do Node na nossa variável ambiente. Adicione a seguinte linha ao final do arquivo `~/.bashrc` (ou do arquivo `~/.zshrc` caso você utilize o shell ZSH):

```bash
export PATH="/usr/local/opt/node@12/bin:$PATH"
```

- Reinicie o terminal e rode os comandos:

```bash
node -v
npm -v
```

Caso estejam nas versões 12.18.3 e 6.14.6, respectivamente, a atualização ocorreu com sucesso.

### Windows

Para atualizar o seu Node e npm utilizando o **Chocolatey**, siga os passos:

- Execute o seguinte comando:

```bash
choco upgrade nodejs-lts
```

- Em seguida, rode os comandos:

```bash
node -v
npm -v
```

Caso estejam nas versões 12.18.3 e 6.14.6, respectivamente, a atualização ocorreu com sucesso.

## Yarn 1

Se você já possui Yarn na versão 1.22, não é preciso instalar nem atualizar

### Linux (Ubuntu/Debian)

Para atualizar o seu Yarn 1 utilizando o , siga os passos:

- Execute os seguintes comandos:

```bash
sudo apt-get update
sudo apt-get --only-upgrade install yarn
```

- Em seguida, rode o comando:

```bash
yarn --version
```

Caso esteja na versão 1.22.4, a atualização ocorreu com sucesso.

### macOS

Para atualizar o seu Yarn 1 utilizando o **Homebrew**, siga os passos:

- Execute o seguinte comando:

```bash
brew upgrade yarn
```

- Em seguida, rode o comando:

```bash
yarn --version
```

Caso esteja na versão 1.22.4, a atualização ocorreu com sucesso.

### Windows

Para atualizar o seu Yarn 1 utilizando o **Chocolatey**, siga os passos:

- Execute o seguinte comando:

```bash
choco upgrade yarn
```

- Em seguida, rode o comando:

```bash
yarn --version
```

Caso esteja na versão 1.22.4, a atualização ocorreu com sucesso.