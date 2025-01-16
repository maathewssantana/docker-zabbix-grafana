# Serviço de monitoramento ☁️🌍

## Objetivo

Criação de Containers no Docker com Serviços de Monitoramento
Implante serviços de monitoramento de forma eficiente utilizando containers Docker.

Monitoramento de um Windows Server 2016 com o Agent Zabbix
Configure o agente Zabbix para monitorar e gerenciar seu servidor Windows Server 2016 de maneira proativa.

Exibição do Monitoramento no Grafana
Visualize os dados coletados pelo Zabbix em um painel gráfico intuitivo e personalizado no Grafana, facilitando a análise e interpretação de métricas de desempenho.

## Created by :🙋🏾‍♂️

- Matheus Santana.

# Topologia

![proj-zabbix-grafana-docker drawio](https://github.com/user-attachments/assets/b7dce71e-181f-4f63-8dc2-fbc5eb922ab8)


# Execução 🚀


Certo, vamos continuar com o tutorial:

---

### Instalação dos Containers

1. **Criação dos Containers**
   Iniciamos a instalação dos containers utilizando o código YAML com a estrutura para a instalação de:

   - MySQL
   - Zabbix Server
   - Zabbix Frontend
   - Grafana

   Para iniciar os containers, utilize o comando:
   ```bash
   docker-compose up -d docker-compose.yml
   ```

2. **Configuração do Zabbix no Grafana**
   Após iniciar os containers, configuramos o plugin do Zabbix no Grafana para a integração dos dados. Assim, podemos consumir e visualizar os dados do Zabbix no Grafana.

3. **Acesso e Configuração**
   - Acesse o Zabbix através do endereço `http://localhost` na porta 80 para configurar o Zabbix Server.
   - Acesse o Grafana através do endereço `http://localhost:3000` na porta 3000 para configurar o Grafana e integrar os dados do Zabbix.

4. **Verificação e Configuração do Plugin no Grafana**
   - Verifique no Grafana se a instalação do plugin do Zabbix está configurada corretamente.
   - Após isso, configure o plugin para integrar o Grafana com o Zabbix.

     ![grafana](https://github.com/user-attachments/assets/f71f2f12-0439-4a6b-9c78-03e1b714cd33)


5. **Criação de Usuário no Zabbix**
   - Será necessário criar um usuário no Zabbix com permissões de superadministrador para garantir a integração adequada.
![zabbix](https://github.com/user-attachments/assets/eb042f3c-e93b-469d-8f8d-262ab3c7049a)


6. **Instalação do Agente no Servidor Monitorado**

  - Após configurar o Zabbix e o Grafana, instale o agente Zabbix no servidor que será monitorado, neste caso, um Windows Server 2016.
    ![windows](https://github.com/user-attachments/assets/bfa673e3-aafd-4fd3-b557-a5855c687447)


7. **Configuração do Monitoramento no Zabbix**

  - Insira o IP do host no monitoramento do Zabbix e aguarde a validação para verificar se a conexão foi bem-sucedida.
    ![windowsmoni](https://github.com/user-attachments/assets/c2b77528-4fda-4b15-9f87-cd343117ad90)

8. **Grafana Monitoramento**

   - Após a realização desses passos configuramos o Dashboard com a visualização no grafana.
     ![grafanamoni](https://github.com/user-attachments/assets/2cc655ec-cbf4-4fea-8c39-20ed28c3fce1)



