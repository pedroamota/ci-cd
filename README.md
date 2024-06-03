# 📱🔢 Seminário

Bem-vindo ao repositório do nosso seminário sobre desenvolvimento de uma calculadora em Flutter!

## Tecnologias utilizadas
- [Flutter](https://flutter.dev/) - Linguagem de programação que permite que os desenvolvedores criem aplicações nativas para dispositivos móveis (iOS e Android), web e desktop a partir de uma única base de código.

## Conteúdo do Seminário

- Introdução ao Flutter e Dart
- Configuração do ambiente de desenvolvimento
- Estrutura de um projeto Flutter
- Criação da interface de usuário (UI) da calculadora
- Implementação das funcionalidades básicas da calculadora
- Testes e depuração

### Requisitos

 - Flutter SDK
- Conhecimentos básicos de programação em Dart
- Um editor de código como Visual Studio Code ou Android Studio

### Instruções de Uso

1. **Clone o Repositório:**
   ```bash
   git clone https://github.com/wilicarol/Seminario_C214_2024.git
   cd Seminario_C214_2024
   ```

2. **Instale as dependências:**
   ```bash
   flutter pub get
   ```
   O comando `flutter pub get` é utilizado no Flutter para gerenciar as dependências do projeto.


3. **Execute o projeto:**
   ```bash
   flutter run
   ```

1. **Montar imagem:**

    ```
    docker build -t dockerfile .  
    ```

2. **Iniciar:**
   
    Subir container
    ```
    docker run --name jenkins_flutter -p 8080:8080 -p 50000:50000 dockerfile
    ```
    Subir com docker-compose
    ```
    docker-compose -f docker-compose.yaml up.

## Testes:

 **Execute os Testes:**
    ```bash
    flutter test
    ```
    Os testes serão executados e você verá os resultados no terminal.
    Obs.: Verifique que você está no diretório raiz do projeto.

## Equipe

<div style="display: flex; justify-content: space-between;">
  <a href="https://github.com/pedroamota" style="margin-right: 10px;">
    <p> Pedro Augusto da Luz Mota </p>
  </a>
  <a href="https://github.com/wilicarol" style="margin-right: 10px;">
    <p> Wiliane Carolina Silva </p>
  </a>
</div>