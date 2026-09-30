# Descrição 

Este projeto está sendo desenvolvido como um aplicativo focado em logística para ajudar pequenos comércios, utilizando a biblioteca widget (Flutter) para construir interface com informações sobre o cliente, local, motorista, veículo e carga.

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
### Mapa e Rotas

*   **flutter_map**: Pacote do Flutter para renderizar mapas interativos e marcadores diretamente na interface do app.
*   **Servidor OSRM**: Motor de roteamento próprio integrado via requisições HTTP para cálculo de trajetos e distâncias.

## Pagamento
### Pagamento

*   **API do Mercado Pago** via SDK oficial (`mercadopago`).
*   **Checkout Pro** para redirecionamento seguro de pagamentos.
*   **Checkout Transparente** para geração e recebimento via **Pix**.

## Clima

Previsão do tempo via [Open-Meteo](https://open-meteo.com/)
A Open-Meteo é uma API gratuita de clima: você envia latitude e longitude e ela devolve a previsão (temperatura, chuva, vento) hora a hora, além de dados históricos.

No seu sistema, ela alimenta o PostgreSQL com previsões coletadas em segundo plano, e você usa esses dados para alertar motoristas e clientes sobre condições que possam atrasar entregas.

# Banco de Dados utilizado

## Postgresql
