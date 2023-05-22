
# Lições cryptozombies 
![CryptoZombies](https://user-images.githubusercontent.com/13703497/69648502-c8f3db80-10ae-11ea-9d52-ce4d4bbc426a.jpeg)

Aprendendo a escrever smart contracts em Solidity através da construção do um jogo .


 ## Payable modifier
> um tipo especial de função que pode receber Ether.
## modificador de estado
visualizar

> nenhum dado é salvo/alterado. sem custo de gás se chamado externamente de fora do contrato (mas faça o gás de costa se chamado internamente por outra função)
puro

> não lê nenhum dado do blockchain. sem custo de gás se chamado externamente de fora do contrato (mas faça o gás de costa se chamado internamente por outra função)


## Custom modifier

> definir a lógica personalizada para determinar como eles afetam uma função, por exemplo, validações em `onlyOwner`, `aboveLevel`.
## Visibility modifier
private

> só pode ser chamado de outras funções dentro do contrato
interno

> é como private, mas também pode ser chamado por contratos que herdam deste
externo

> só pode ser chamado fora do contrato
público

> pode ser chamado em qualquer lugar, tanto interna quanto externamente. No Solidity, quando você declara uma variável pública, ela cria automaticamente uma função pública "getter" com o mesmo nome.
indexado

> para filtrar os eventos e apenas escutar as mudanças relacionadas ao usuário atual, o contrato Solidity teria que usar a palavra-chave indexada

## Types

uint

> equivalent to uint256
string

struct
## Terms
tokens
um contrato inteligente que segue algumas regras comuns. todos os tokens ERC20 compartilham o mesmo conjunto de funções com os mesmos nomes

  ## ERC-20

 tokens fungíveis (negociáveis, divisíveis)

 ## ERC-721
> tokens não fungíveis (NFT).
> não intercambiáveis, pois cada um é considerado único e não divisível. Você só pode negociá-los em unidades inteiras e cada um tem um ID exclusivo. por exemplo, peça de arte, personagem do jogo,

 ## msg.sender
> é uma variável global disponível para todas as funções - refere-se ao endereço do remetente

 ## Wei
> a menor subunidade do éter — há 10^18 wei em um éter

 ## Web3.js
> uma biblioteca JavaScript da Ethereum Foundation. Os nós Ethereum falam apenas uma linguagem chamada JSON-RPC, que não é muito legível por humanos. Uma consulta para informar ao nó que você deseja chamar uma função em um contrato é mais ou menos assim:
> `{"jsonrpc":"2.0","method":"eth_sendTransaction","params":[{"from":"0xb60e8dd61c5d32be8058bb8eb970870f07233155","to":"0xd46e8dd67c5d32be8058bb8eb970870f07244567","gas":"0x76c0","gasPrice":"0x9184e72a000","value":"0x9184e72a","data":"0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675"}],"id":1}`
 ## call
> usado para as funções `view` e `pure`. Ele é executado apenas no nó local e não cria uma transação no blockchain. As funções `view` e `pure` são somente leitura e não mudam de estado no blockchain. Eles também não custam combustível e o usuário não será solicitado a assinar uma transação com o MetaMask.
 ## send
> cria uma transação e altera dados no blockchain. Você precisará usar send para qualquer função que não seja `view` ou `pure`.
assert vs require
> assert é semelhante a require, onde lançará um erro se for falso. require reembolsará o usuário pelo restante de seu gás quando uma função falhar, enquanto assert não o fará. assert é normalmente usado quando algo deu terrivelmente errado com o código (como um estouro de uint).
 ## Web3 Provider

> assert é semelhante a require, onde lançará um erro se for falso. require reembolsará o usuário pelo restante de seu gás quando uma função falhar, enquanto assert não o fará. assert é normalmente usado quando algo deu terrivelmente errado com o código (como um estouro de uint).
 ## Infura
> Infura é um serviço que mantém um conjunto de nós Ethereum com uma camada de cache para leituras rápidas, que você pode acessar gratuitamente por meio de sua API. Usando o Infura como provedor, você pode enviar e receber mensagens com segurança de/para o blockchain Ethereum sem precisar configurar e manter seu próprio nó.
## Metamask
> extensão de navegador para Chrome e Firefox que permite aos usuários gerenciar com segurança suas contas Ethereum e chaves privadas e usar essas contas para interagir com sites que usam Web3.js.
> Metamask usa os servidores da Infura sob o capô como um provedor web3, assim como fizemos acima — mas também dá ao usuário a opção de escolher seu próprio provedor web3. Então, usando o provedor web3 da Metamask, você está dando uma escolha ao usuário, e é uma coisa a menos com que você precisa se preocupar em seu aplicativo.
> Metamask usa os servidores da Infura sob o capô como um provedor web3, assim como fizemos acima — mas também dá ao usuário a opção de escolher seu próprio provedor web3. Então, usando o provedor web3 da Metamask, você está dando uma escolha ao usuário, e é uma coisa a menos com que você precisa se preocupar em seu aplicativo.
## ABI
> ABI significa Application Binary Interface. Basicamente, é uma representação dos métodos de seus contratos no formato JSON que informa ao Web3.js como formatar chamadas de função de uma maneira que seu contrato entenda.
> Quando você compilar seu contrato para implantar no Ethereum (que abordaremos na Lição 7), o compilador Solidity fornecerá a ABI,





## Referência

 - [jogo cryptozombies](https://cryptozombies.io/en/course/)
 

