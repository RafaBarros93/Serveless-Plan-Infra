# Passo a passo para a utilização do Serveless

## Ambiente de Desenvolvimento

## Para nossa nova infraestrutura iremos utilizar o framework Servless juntamente com o Cloud Functions da Ibm

**Alguns links para estudo repositorios e informações complementares com exemplos da utilização da ferramenta**

```

    Repósitorio do Serveless:
    (https://github.com/serverless)


    Documentação Serveless
    (https://serverless.com/framework/docs/providers/openwhisk/guide/quick-start/)


    Documentação CloudFunctions
    (https://console.bluemix.net/openwhisk/)

    Explicação do Serveless pelo LevelUpTuts

    (https://www.youtube.com/channel/UCyU5wkjgQYGRB0hIHMwm2Sg)

    Pequeno tutorial da Pagar.me Talks

    (https://www.youtube.com/watch?v=2oNovfw3V08&t=43s)


```

##Pré requisitos

```
1.Node.js v6.5.0 or later.
2.Serverless CLI v1.9.0 or later. You can run npm install -g serverless to install it.
3.An IBM Bluemix account. If you don't already have one, you can sign up for an account and then follow the instructions for getting access to OpenWhisk on Bluemix.
4.Set-up your Provider Credentials.
5. Install Framework & Dependencies Due to an outstanding issue with provider plugins, the OpenWhisk provider must be installed as a global module.
```

# Passo a passo para a utilização do Serveless

**1 - Instalar o serveless via npm**

```
# Installing the serverless cli
npm install -g serverless
# Updating serverless from a previous version of serverless
npm install -g serverless
# Login to the serverless platform (optional)
serverless login

```

**2- Criar um novo serviço**

```
# Create a new Serverless Service/Project
$ serverless create --template openwhisk-nodejs --path my-service
# Change into the newly created directory
$ cd my-service
# Install npm dependencies
$ npm install

```

**3- Fazer o deploy do serviço**

```
serverless deploy -v

```

**4- Fazer o deploy da função apenas**

```
 serverless logs -f hello -t

```

**5- Invocar a função**

```
    serverless invoke --function teste

    # results
{
  "payload": "Teste ok!!"
}

serverless invoke --function teste --data '{"name": "Rafael"}'
#results
{
  "payload": "Teste, Rafael!"
}

```

# Authors

-   **Rafael Lopes** \- Backend Developer \- [RafaBarros93](https://github.com/RafaBarros93)

# Thanks for

-   **Team NuHackers**
