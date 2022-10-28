# ⚛️ React Native: Criando testes para sua aplicação

Esse é o projeto do curso **Criando testes para sua aplicação** da formação em **React Native** estudado pelo Fábio Mori na [Alura](https://www.alura.com.br/).

## 📱 Projeto

O objetivo deste projeto é criar testes para verificar a funcionalidade de um aplicativo de leilões.

## 🧑‍💻 Palavras-chave

As tecnologias e ferramentas ensinadas pela [Alura](https://www.alura.com.br/) no projeto são:

- React Native
- Expo
- Jest
- React Testing Library
- React Hooks Testing Library
- Detox
- Expects
- Coverage

## 📲 O aprendizado do aluno Fábio Mori
### Deixa eu te contar uma história

Já pensou criar um aplicativo super interessante e depois descobrir que ele está cheio de bugs? E o pior, imagina descobrir isso quando já existem milhares de usuários utilizando a sua aplicação? Essa situação pode ser, além de muito chata, um verdadeiro desastre para o seu projeto e sua empresa. Portanto uma das coisas mais importantes para os desenvolvedores é testar a sua aplicação antes de colocar para rodar. E como podemos fazer isso? Bom, o React Native possui diversas ferramentas e APIs que nos auxiliam e facilitam a implementação de testes no código do projeto para que seja possível validar ao máximo sua usabilidade. Você ficaria mais tranquilo se pudesse testar todo seu programa antes de lançar, não é mesmo? Eu também, então vamos adotar sempre essa boa prática.

### O que eu aprendi?

- Porque testar um código?
  - Para garantir que ele está funcionando da maneira como gostaríamos e que ele continue desta forma quando for lançado.
  - Embora criar um código com as funções de teste demande mais esforço inicialmente, a longo prazo isso vai poupar muito esforço de manutenção e correção versus um código que não possui um bom projeto de testes.
  
- Tipos de teste:
  - Unidade: testa um comportamento isolado, uma função, por exemplo.
  - Integração: testa a comunicação da aplicação com outros módulos, uma busca de informação na API, por exemplo (garante que a nossa aplicação está funcionando em harmonia com serviços externos).
  - Interface: testa uma aplicação real, rodar o programa em um simulador, por exemplo.
  
 - Pirâmide de testes:
  - Base (primeira camada): testes de unidade, com menos fidelização, porém mais baratos e rápidos
  - Corpo (camada do meio): testes de integração, mais fidelizados que os teste de unidade, porém menos baratos e rápidos.
  - Topo (última camada): testes de interface do usuário, são os de maior fidelização, porém os mais caros e demorados.
  - Geralmente, o custo de criação e execução de um teste está diretamente ligado ao nível de fidelização, quanto maior a fidelização, maior o custo.
  
- Tipos e técnicas:
  - Teste de fluxo: testa um passo a passo dentro da aplicação.
  - Teste de componente: renderiza o componente em memória.
  - TDD (Test Driven Development): desenvolvimento guiado por testes, primeiro você testa, depois desenvolve suas funcionalidades.
  
 - Vantagens de utilizar testes:
  - Menos ocorrência de bugs.
  - Incentiva códigos coesos.
  - Ajuda na validação dos requisitos.
  - Diminui o custo da aplicação a longo prazo.
  
- Desvantagens de utilizar testes:
  - Custo maior a curto prazo
  - Métricas podem ser mal entendidas
  
- Bibliotecas de testes:
  - Jest: faz teste de unidade, interface e se conecta com outras bibliotecas também.
  - React Testing Library: biblioteca de testes mais interativa e otimizada.
  - React Hooks Testing Library: biblioteca para testar os hooks.
  - Detox: biblioteca que faz testes de interface, porém precisa ser um projeto React Native puro.

- Expects: função utilizada nos testes para checar se os valores nos testes são os esperados.
  - `toBe()`: compara inteiros ou textos.
  -`toBeCloseTo()`: compara pontos flutuantes obtidos através de operações matemáticas (devido a arredondamentos, podem haver erros com o `toBe()`).
  -`toBeFalsy()`/`toBeTruthy()`: compara valores falsos/verdadeiros em um contexto booleano. No caso de falsy, não apenas 'false' será validado, mas valores como 'null', '0', "", 'undefined' e 'NaN', também.
  -`toEqual()`: compara objetos, verificando se as propriedades internas são iguais.
  - Na documentação oficial do Expect no Jest, tem todas as opções.
  
- Funções globais: utilizadas no desenvolvimento dos testes.
  - `describe` e `it` não são as únicas.
  - Podemos usar algumas funções para controlar quais métodos de teste serão executados ou até executar funções antes/depois das funções de teste.
  - `describe('', () => {})`: cria um contexto com uma descrição para todos os testes dentro da função.
  - `test('', () => {})`: cria um teste com uma função que deve ser correspondida ao que o teste pretente testar.
  - `it('', () => {})`: funciona assim como o `test`.
  - `afterAll(() => {})`: executa a função após todos os testes do seu conteúdo terminarem a sua execução.
  - `beforeAll(() => {})`: executa a função antes que todos os testes do seu conteúdo comecem a sua execução.
  - `afterEachAll(() => {})`: executa a função sempre que um teste do seu contexto termine a sua execução.
  - `beforeEachAll(() => {})`: executa a função sempre antes que um teste do seu contexto começe a sua execução.
  - Na documentação oficial do Globais no Jest, tem todas as opções.
  
- Coverage: é a cobertura de teste da sua aplicação, o quantos porcento da sua aplicação está coberta em testes.
  - 100% de coverage não significa que seu código está 100% testado
  - Na pasta coverage do seu projeto possui um arquivo chamado `index.html` que é uma espécie de dashboard e relatório do percentual de coverage do seu código.
  
- Mocks com Jest: alguns métodos do Jest para trabalhar com os Mocks.
  - `mockClear()`: limpa todos os registros das chamadas das funções.
  - `mockReset()`: faz tudo o que o `mockClear()` faz, e também limpa as implementações e valores a serem retornados.
  - `mockRestore()`: faz tudo o que o `mockClear()` faz, e também volta a implementação do método original.
  - `mockImplementation(fn)`: seta uma nova implementação para a função mockada.
  - `mockReturnValue(value)`: seta um valor fixo a ser retornado.
  
- Snapshots:
  - Verifica se a estrutura do componente permanece a mesma, usando a referência JSON que a renderização retorna.
  - Ele não testa de fato a regra de negócio, ele testa as estruturas e até os estilos do componente.
  - Podemos usá-los em componentes simples, que não contém regras de negócio e que não mudam com frequência.
  
  
## ▶️ Rodando o Projeto

Você vai precisar ter:
```
Node: 16.8.0
NPM: 8.1.3
Expo: 5.2.0
```
Com a pasta do projeto no computador no terminal, digite:
```
npm install
```
Agora, digite para iniciar o projeto:
```
npm start
```
Para conectar a API:
No arquivo package.son -> onde está a API altere o valor do IP para o da sua máquina.
Na pasta src/servicos/apiLeiloes.js altere o valor do IP para o da sua máquina também.
```
npm run api
```
Instalando o jest:
```
expo install jest_expo jest
```
Instalando o Testing Library:
```
npm install --save-dev react-test-renderer @17.0.1 @testing-library/react-native @testing-library/react-hooks
```
Para rodar o teste:
```
npm test
```
IMPORTANTE: Existem mais configurações relacionadas as bibliotecas que estão sendo utilizadas que devem ser consultadas na documentação oficial de cada uma.

## 📚 Mais informações do curso da [Alura](https://www.alura.com.br/).

[Curso  React Native: Criando testes para sua aplicação](https://www.alura.com.br/curso-online-react-native-criando-testes-aplicacao).
