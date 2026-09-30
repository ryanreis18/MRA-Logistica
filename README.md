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
 Biblioteca Open Source no seu servidor

## Mapa e Rotas
 Leaflet + Servidor próprio OSRM

## Pagamento
### Pagamento

*   **API do Mercado Pago** via SDK oficial (`mercadopago`).
*   **Checkout Pro** para redirecionamento seguro de pagamentos.
*   **Checkout Transparente** para geração e recebimento via **Pix**.

## Clima

 API Open-Meteo

# Banco de Dados utilizado

## Postgresql
