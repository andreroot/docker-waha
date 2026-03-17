# 📡 Waha



### Plataforma

- configuração no docker:
message, message.any


- **fluxo | N8N integração com waha**

    *Waha*

    criar pacote 
    @devlikeapro/n8n-nodes-waha

    fluxo recebe via whatsapp comandos e são criados fluxos para as msgs com palavras chave



### Administração | Dockers 

- **comandos docker** a estrutura dos docker esta baseada em docker compose

[baixar]

    docker-compose down

[subir]

    docker-compose up -d 

[update]

    docker-compose up --build -d

    docker-compose up -d --force-recreate waha
    
    docker-compose down --volumes --remove-orphans

    docker-compose build --no-cache

    docker-compose up -d

- **migrar arquivos para maq local**

    ```sudo chmod 777 /home/administrador/projetos/n8n/dados-integracao-docker-n8n/n8n_data/```

    ```sudo chown -R administrador:administrador /home/administrador/projetos/n8n/dados-integracao-docker-n8n/n8n_data/```
    
    ```sudo chgrp administrador /home/administrador/projetos/n8n/dados-integracao-docker-n8n/n8n_data/```

    **copiar de arquivos** scp n8n_data/_data/* administrador@host:/home/administrador/projetos/n8n/dados-integracao-docker-n8n/n8n_data/_data
    
    **permissões para docker ler/escrever na pasta volume** sudo chown -R 1000:1000 ./n8n_data