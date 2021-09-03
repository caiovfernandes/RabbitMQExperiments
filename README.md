## Pre-requisitos para rodar os projetos
1. Na raíz do projeto, criar um virtual environment python com o comando:
```
    python3 -m venv venv
```

2. Ative o ambiente virtual com o comando:
```
    source venv/bin/activate
```

3. Instale as dependências necessárias com o comando:
```
    pip install -r requirements.txt
```

# Executando seções:
## 1. `HelloWorld`:
- Nesta seção, escrevemos dois pequenos programas em Python; um produtor (producer) que envia uma única mensagem e um consumidor (consumer) que recebe as mensagens e as imprime. É um "Hello World" de mensagens.
1. Em um terminal, inicie o consumidor executando `python HelloWorld/receiving.py`
2. Em um segundo terminal, envie uma mensagem com o comando `python HelloWorld/sending.py`

## 2. `WorkQueues`
- Nesta seção, criamos uma fila de trabalho (work queue) que é usada para distribuir time-consuming tasks entre vários workers.
1. Em um terminal, inicie o consumidor executando `python WorkQueues/worker.py`
2. Em um segundo terminal, envie uma mensagem com o comando `python WorkQueues/new_task.py`

## 3. `Publish_Subscribe`
- Nesta seção, vamos entregar uma mensagem a vários consumidores. Esse padrão é conhecido como "publish / subscribe".
1. Em um terminal, inicie o consumidor executando `python PublishSubscribe/receive_log.py`
2. Em um segundo terminal, envie uma mensagem com o comando `python PublishSubscribe/emit_log.py`

## 4. `Routing`
- Nesta seção, vamos tornar possível assinar apenas um subconjunto das mensagens.
1. Em um terminal, inicie o consumidor executando `python Routing/receive_log_direct.py info warning error`
2. Em um segundo terminal, envie uma mensagem com o comando `python Routing/emit_log_direct.py`

## 5. `Topics`
- Nesta seção, iremos melhorar nosso sistema de assinatura.
1. Em um terminal, inicie o consumidor executando `python Topics/receive_topic_log.py "#"`
2. Em um segundo terminal, envie uma mensagem com o comando `python Topics/emit_topic_log.py`

## 6. `RPC`
- Nesta seção, vamos usar RabbitMQ para construir um sistema RPC: um cliente e um servidor RPC escalonável.
1. Em um terminal, inicie o server executando `python RPC/rpc_server.py`
2. Em um segundo terminal, envie uma mensagem com o comando `python RPC/rpc_client.py`

## 6. `PublisherConfirms`
- Nesta seção, vamos usar Publisher Confirms para garantir que as mensagens publicadas cheguem com segurança ao broker.
1. Em um terminal, inicie o server executando `python RPC/rpc_server.py`
2. Em um segundo terminal, envie uma mensagem com o comando `python RPC/rpc_client.py`