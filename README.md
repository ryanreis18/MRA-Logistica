# Descrição 

Este projeto está sendo desenvolvido como um aplicativo focado em logística para ajudar pequenos comércios, utilizando o framework **Flutter** para construir interfaces com informações sobre o cliente, local, motorista, veículo e carga.

# Funcionalidades

* Página inicial com motoristas cadastrados e mapa
* Página de negociação, acessível ao clicar no perfil de um motorista para negociar
* Chat entre motorista e cliente
* Suporte 24h
* Roteirização
* Rastreamento em tempo real
* Gestão de Inventário e Armazenagem
* Logística de Transporte e Frota
* Arquitetura Técnica
* Segurança aplicada

# API utilizada

## Rastreamento

### 📡 Infraestrutura de Rastreamento (Servidor Open Source)

O sistema utiliza uma biblioteca e infraestrutura de código aberto auto-hospedada no back-end para gerenciar a telemetria da frota em tempo real:

* **Processamento de Coordenadas:** Recebe continuamente os pacotes de dados de localização (latitude e longitude) transmitidos pelo aplicativo do motorista ou por rastreadores dedicados.
* **Comunicação em Tempo Real:** Mantém conexões persistentes para atualizar a posição dos veículos na interface do usuário, sem a necessidade de recarregar a página.
* **Histórico e Telemetria:** Registra o rastro do percurso percorrido e monitora eventos importantes do trajeto (como velocidade, paradas e status de ignição).

## Mapa e Rotas

*   **flutter_map**: Pacote do Flutter para renderizar mapas interativos e marcadores diretamente na interface do app.
*   **Servidor OSRM**: Motor de roteamento próprio integrado via requisições HTTP para cálculo de trajetos e distâncias.

## Pagamento

*   **API do Mercado Pago**: Integração direta via requisições HTTP (`Dio` / `Http`) no ecossistema Dart/Flutter.
*   **Checkout Pro**: Redirecionamento seguro para a interface do Mercado Pago.
*   **Checkout Transparente**: Geração e exibição de **Pix** (Copia e Cola / QR Code) direto no app.

## Clima

*   **Open-Meteo API**: API gratuita de clima que fornece previsões (temperatura, chuva, vento) com base em coordenadas geográficas.
*   **Integração**: Coleta dados em segundo plano para alimentar o PostgreSQL, gerando alertas de possíveis atrasos nas entregas devido ao clima.

# Banco de Dados utilizado

*   **PostgreSQL**: Banco de dados relacional para persistência de dados de usuários, rotas, histórico e logs de telemetria.
