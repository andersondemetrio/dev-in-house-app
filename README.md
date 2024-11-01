# Projeto de Navegação React Native com AsyncStorage

Este é um aplicativo mobile desenvolvido em React Native, que utiliza o AsyncStorage para gerenciar o estado de login e oferece navegação entre telas através do React Navigation.

## Índice

- [Visão Geral](#visão-geral)
- [Funcionalidades](#funcionalidades)
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Configuração](#configuração)
- [Uso](#uso)
- [Estrutura de Navegação](#estrutura-de-navegação)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Visão Geral

Este projeto é uma aplicação móvel simples para exibir listas de produtos, usuários e movimentações, com uma tela de login e armazenamento de dados de login usando o `AsyncStorage`.

## Funcionalidades

- **Tela de Login**: Verificação do status de login e armazenamento de dados com `AsyncStorage`.
- **Navegação entre Telas**: Implementação de navegação por pilha com o `React Navigation`.
- **Listagem e Gerenciamento**: Visualização de listas de produtos, usuários e movimentações.
- **Perfil e Registros**: Navegação adicional para funcionalidades de usuário.

## Pré-requisitos

- Node.js (versão 14 ou superior)
- npm ou yarn
- Expo CLI (caso utilize o Expo)
- React Native CLI (caso utilize CLI do React Native)

## Instalação

Clone este repositório:

```bash
git clone https://github.com/andersondemetrio/seu-repositorio.git

===> Bibliotecas necessárias
npm install @react-navigation/native
npx expo install react-native-screens react-native-safe-area-context
npm install @react-navigation/stack
npm install axios
npx expo install @react-native-async-storage/async-storage
npx expo install @react-native-picker/picker
npx expo install lottie-react-native
npx expo install expo-image-picker
npx expo install react-native-maps

# Usando Expo
npx expo start

# Ou usando React Native CLI
npx react-native run-android # ou run-ios


Estrutura de Navegação
A navegação do aplicativo é gerenciada por Stack Navigator do @react-navigation/stack. Abaixo estão as telas principais:

LoginScreen: Tela inicial para login de usuários. Se o usuário já estiver logado (verificado pelo AsyncStorage), ele será redirecionado para a tela principal.

HomeScreen: Tela inicial pós-login, onde o usuário pode navegar para:

ProductListScreen: Tela para listar produtos.
UserListScreen: Tela para listar e gerenciar usuários.
UserRegisterScreen: Tela para registrar novos usuários.
MovementListScreen: Tela para listar e gerenciar movimentações.
MovementsList: Tela específica para perfil de movimentações.

Estrutura do Código
O código é organizado em componentes e telas no diretório src/screens e src/components:

├── src
│   ├── components
│   │   └── Header.js          # Componente de cabeçalho usado em várias telas
│   ├── screens
│   │   ├── LoginScreen.js     # Tela de Login
│   │   ├── HomeScreen.js      # Tela Principal com navegação para as demais
│   │   ├── ProductListScreen.js # Tela de Produtos
│   │   ├── UserListScreen.js  # Tela de Listagem de Usuários
│   │   ├── UserRegisterScreen.js # Tela de Registro de Usuários
│   │   ├── MovementListScreen.js # Tela de Movimentações
│   │   └── MovementsList.js   # Tela de Perfil de Movimentações
└── App.tsx                    # Componente principal
