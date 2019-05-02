# Serviços Cognitivos: Laboratório 3 - ChatBot Pedido de Pizzas SampaMais

[![bit-azure.png](https://i.postimg.cc/ZKwS8SHj/bit-azure.png)](https://postimg.cc/vcxkyCp6)

Nesse laboratório estaremos integrando um **[Azure Bot Service](https://aka.ms/AA4qm7p)** de pedido de Pizzas ao **[Serviço Cognitivo](https://aka.ms/AA4qm7k)** de Processamento de Linguagem Natural chamado **[LUIS](https://aka.ms/AA4qm7q)**

## Agenda - Lab 03

- **[1. Criando Conta no LUIS](#1-criando-conta-no-luis)**

- **[2. Criando uma App no LUIS](#2-criando-uma-app-no-luis)**

- **[3. Criando as Intenções no LUIS](#3-criando-as-intenções-no-luis)**

- **[4. Criando as Entidades no LUIS](#4-criando-as-entidades-no-luis)**

- **[5. Criando os Enunciados no LUIS](#5-criando-os-enunciados-no-luis)**

- **[6. Conectando o LUIS com ChatBot](#6-conectando-o-luis-com-chatbot)**

- **[7. Palavras Finais](#7-palavras-finais)**


## 1. Criando Conta no LUIS.ai

1. Abram o site do [LUIS.ai](https://aka.ms/AA4q8w1)

A aparência do site do LUIS é como demonstra na figura abaixo:

[![Screen-Shot-04-08-19-at-08-07-PM.png](https://i.postimg.cc/qv5JF0XM/Screen-Shot-04-08-19-at-08-07-PM.png)](https://postimg.cc/JsjCyf29)

2. Vão até o botão **Sign in** conforme a imagem abaixo:

[![imagem-02.png](https://i.postimg.cc/Bb67RWC4/imagem-02.png)](https://postimg.cc/phwBn676)

3. Ao clicar em **Sign in** aparecerá uma outra janela onde você colocará a sua conta de e-mail que você usou ao criar a conta do **[Portal Azure](https://aka.ms/AA4qm7a)**. Após isso você será direcionado ao portal principal do LUIS. 

4. Depois que você entra no Portal do LUIS, aparecerá algumas perguntas que deverão ser respondidas. Bastam seguir conforme a imagem abaixo e depois clique no botão **Continue**:

[![Screen-Shot-04-08-19-at-08-16-PM.jpg](https://i.postimg.cc/MKdwNxbf/Screen-Shot-04-08-19-at-08-16-PM.jpg)](https://postimg.cc/rK07RBHq)

5. Aparecerá uma outra janela. Dessa vez, basta clicar em **Create a LUIS app now**

[![image-1.jpg](https://i.postimg.cc/2y9HdHhy/image-1.jpg)](https://postimg.cc/CnDHSsvp)

6. Feito isso, abrirá um Dashboard do Portal do site do LUIS:

[![Screen-Shot-04-08-19-at-08-30-PM.png](https://i.postimg.cc/MpVDXZPv/Screen-Shot-04-08-19-at-08-30-PM.png)](https://postimg.cc/87kW0GVS)

## 2. Criando uma App no LUIS:

1. Clique em **Create new App**

[![image-1.png](https://i.postimg.cc/4xPrn1FK/image-1.png)](https://postimg.cc/dh7WxGFv)

2. Depois de clicar em **Create New App**, abrirá uma janela popup como segue a imagem abaixo. Preencha conforme a imagem abaixo e depois clique no botão em **Done**

[![Screen-Shot-04-08-19-at-08-47-PM.png](https://i.postimg.cc/bvNd23y4/Screen-Shot-04-08-19-at-08-47-PM.png)](https://postimg.cc/cv2dp78c)

3. Seguindo esses passos, o site direcionará para a página da aplicação criada

[![Screen-Shot-04-08-19-at-08-49-PM.png](https://i.postimg.cc/QdDvmzWY/Screen-Shot-04-08-19-at-08-49-PM.png)](https://postimg.cc/hfCCPpsV)

## 3. Criando as Intenções no LUIS

Nesta parte, vamos criar as Intents (Intenções) da nossa aplicação. Nesse caso criaremos 4 inteções, são elas:

* Cancelar
* Pedir
* Saudar
* Verificar
* None (default)

1. Vamos agora adicionar essas inteções. Cliquem em **Create new Intent**

[![image-1.png](https://i.postimg.cc/DzvkvNv4/image-1.png)](https://postimg.cc/v4NSX36G)

2. Abrirá uma janela popup pedindo para criar uma nova inteção. Vamos cadastrar as 4 intenções acima e depois clique no botão **Done**

[![Screen-Shot-04-08-19-at-08-57-PM.png](https://i.postimg.cc/pLZVJzy8/Screen-Shot-04-08-19-at-08-57-PM.png)](https://postimg.cc/mPPGbcY2)

3. No final teremos cadastradas as 4 intenções no LUIS, conforme a imagem abaixo:

[![Screen-Shot-04-08-19-at-08-59-PM.png](https://i.postimg.cc/XYQ3CWDk/Screen-Shot-04-08-19-at-08-59-PM.png)](https://postimg.cc/DSJR99hS)

Perfeito! Agora vamos dar prosseguimento e vamos cadastrar as Entidades!

## 4. Criando as Entidades no LUIS

Para a nossa aplicação, como estamos lidando com uma Pizzaria, nossa entidade principale será: **Pizza**. 

1. Para criar uma Entidade, clique no botão **Entities**

[![imagem.png](https://i.postimg.cc/V6wRPym2/imagem.png)](https://postimg.cc/mcdM75cS)

2. Depois clique em **Create new Entity**.

[![imagem-1.jpg](https://i.postimg.cc/HsrbKWbV/imagem-1.jpg)](https://postimg.cc/Mv8cfSPS)

3. Ao clicar em **Create new Entity**, abrirá uma janela popup para registrar uma Entidade. Nesse caso, vamos cadastrar: **Pizza**, conforme a imagem abaixo:

[![Screen-Shot-04-08-19-at-09-07-PM.png](https://i.postimg.cc/s2sQV3GP/Screen-Shot-04-08-19-at-09-07-PM.png)](https://postimg.cc/87XP4QHs)

4. Clique no botão **Done**

5. Feito isso, vamos agora incluir uma Entidade pré-definida. No site do LUIS, podemos ver uma lista de Entidades pré-definidas que podemos usar em nossa aplicação. No nosso caso, usaremos a **DateTime**. Para isso, clique no botão **Add prebuilt entity**:

[![imagem-1.jpg](https://i.postimg.cc/d1zydpV4/imagem-1.jpg)](https://postimg.cc/CBs5pvDq)

6. Abrirá uma janela popup. Vamos adicionar **DateTime** e depois clique no botão **Done**

[![imagem-1.jpg](https://i.postimg.cc/NFkjMz9y/imagem-1.jpg)](https://postimg.cc/Zv0SsjLZ)

Agora estamos prontos para melhorar os nossos modelos criados no Intents. Vamos prosseguir!!!

## 5. Criando os Enunciados no LUIS

Agora vamos clicar em cada **Entidade** criada e vamos cadastrar algumas prováveis frases que os usuários poderão digitar no nosso ChatBot.

1. Clique, por exemplo, na Entidade: Cancelar. Depois digite uma frase que remete de acordo a Entidade e depois aperte a tecla **Enter** e vejam como deve ficar(como exemplo), a Entidade **Cancelar**:

[![Screen-Shot-04-08-19-at-09-21-PM.png](https://i.postimg.cc/QxcyBrdY/Screen-Shot-04-08-19-at-09-21-PM.png)](https://postimg.cc/QHxbPw5c)

2. Feito os Enunciados da Intenção **Cancelar**, agora vamos fazer para os demais.

3. Agora vamos 'treinar as nossas Entidades criadas com seus respectivos Enunciados. Para isso, clique no botão **Train**, conforme a imagem abaixo:

[![imagem-1.jpg](https://i.postimg.cc/52hysLV2/imagem-1.jpg)](https://postimg.cc/LJVmXq5c)

4. Quando o botão **Train** ficar verde, daí poderemos apertar o botão **Publish**

[![imagem-1.jpg](https://i.postimg.cc/N08sbnDd/imagem-1.jpg)](https://postimg.cc/sBXCgwtW)

5. Abrirá uma janela popup. Basta escolher a opção: **Production** e depois clicar no botão **Publish**

[![Screen-Shot-04-08-19-at-09-30-PM.png](https://i.postimg.cc/xjp0sMGV/Screen-Shot-04-08-19-at-09-30-PM.png)](https://postimg.cc/23vRyqX0)

6. Aparecerá a seguinte mensagem: `Publishing complete. Refer to the list of endpoints to access your endpoint URL`. Clique justamente nessa frase, pois é aí que iremos pegar o nosso endpoint para conectar com o nosso ChatBot

[![Screen-Shot-04-08-19-at-09-32-PM.png](https://i.postimg.cc/zv4YqwpL/Screen-Shot-04-08-19-at-09-32-PM.png)](https://postimg.cc/QKgybT2s)

7. Abrirá uma nova janela chamada: **Keys and Endpoints Settings**. Vamos até a coluna **Enpoint** e copiar:

[![Screen-Shot-04-08-19-at-09-34-PM.png](https://i.postimg.cc/hPFSWgY2/Screen-Shot-04-08-19-at-09-34-PM.png)](https://postimg.cc/V5RyXymt)

Completamos a criação das: Entidades, Enunciados e Intenções. Agora vamos, conectar o que fizemos no LUIS ao nosso ChatBot

## 6. Conectando o LUIS com ChatBot

1. Abre a aplicação no **[VS Code](http://bit.ly/2IhTeUb)** 

2. Crie um arquivo chamado: `.env`

3. Dentro do arquivo `env`, digite:

```
LUIS_MODEL_URL=<cole-aqui-o-endpoint-criado-no-luis>
```

[![Screen-Shot-04-08-19-at-09-46-PM.png](https://i.postimg.cc/52dj381N/Screen-Shot-04-08-19-at-09-46-PM.png)](https://postimg.cc/6yc962yD)

4. Vá até a pasta `lab3\worshop-3` e execute o comando no prompt comando da sua distro (Sistema operacional) o comando: 

```
> node pizzariaSampaMais.js
```

5. Agora abre o **[Microsoft Bot Framework Emulator v.3](http://bit.ly/2G578HB)** conforme segue a execução da aplicação no gif abaixo:

[![bot-builder-3.gif](https://s2.gifyu.com/images/bot-builder-3.gif)](https://gifyu.com/image/3oZe)

## 7. Palavras Finais

Nesse laboratório, você pôde ser capaz em aprender sobre/como:

* Introdução a ChatBots
* Introdução a Serviços Cognitivos
* Manipular o site do LUIS
* Criar Intenções
* Criar Entidades
* Criar os Enunciados de suas respectivas Entidades
* Conectar o Serviço Cognitivo NLP (LUIS) ao Chatbot




































