## Explicação do Workflow

1. Input type:
    - Define o tipo de atualização da versão:
        - patch: Incrementa apenas o número de patch.
        - minor: Incrementa o número secundário e zera o patch.
        - major: Incrementa o número principal e zera os outros.

2. Atualização da Versão:
    - Lê a versão atual no package.json usando Node.js.
    - Divide a versão em major, minor e patch para atualização conforme o tipo especificado.

3. Manipulação do package.json:
    - Atualiza a versão no package.json usando o comando jq.

4. Criação e Push da Branch:
    - Nomeia a branch no formato release/v{nova_versão}.
    - Faz commit das mudanças e envia a branch para o repositório remoto.



## Como Executar

1. Vá até a aba Actions no GitHub e escolha o workflow.
2. Clique em Run workflow.
3. Escolha o tipo de atualização: patch, minor, ou major.



## Resultado

1. A versão no package.json será incrementada automaticamente.
2. Um commit será feito com a mensagem: chore: bump version to x.y.z.
3. Uma nova branch chamada release/vx.y.z será criada e enviada ao repositório remoto.