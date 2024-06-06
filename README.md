# Nanochat

NanoChat é um aplicativo de mensagens instantâneas desenvolvido utilizando o Flutter e integrado com o Firebase para fornecer funcionalidades robustas e escaláveis de backend. Este documento fornece uma visão geral das funcionalidades do NanoChat e instruções básicas sobre como configurar e executar o aplicativo.
Aplicativo remodelado com o intuito de integrar o banco de dados Firebase com o serviço de autenticação.

# Funcionalidades
1. Autenticação de Usuário
Cadastro e Login: Os usuários podem se cadastrar usando seu e-mail e senha. Após o cadastro, eles podem fazer login utilizando suas credenciais.

2. Armazenamento de Dados
Firestore: Utiliza o Firestore do Firebase para armazenar as mensagens de chat.
Segurança de Dados: Regras de segurança do Firestore configuradas para garantir que somente usuários autenticados possam acessar suas próprias mensagens.

3. Interface do Usuário
Interface Intuitiva: Design simples e intuitivo para facilitar a navegação e a utilização do aplicativo.

# Configuração e Execução
# Pré-requisitos
Flutter SDK instalado
Conta no Firebase
Editor de código (VSCode, Android Studio, etc.)

# Passo a Passo para Configuração
1. Clone o Repositório: 

2. Configurar Firebase:

  Acesse o Console do Firebase
  Crie um novo projeto ou utilize um projeto existente
  Adicione um novo aplicativo no projeto Firebase (Android e/ou iOS)
  Siga as instruções para configurar o Firebase no seu projeto Flutter
  *Para Android*: adicione o google-services.json ao diretório android/app
  *Para iOS*: adicione o GoogleService-Info.plist ao diretório ios/Runner

3. Adicionar Dependências do Firebase:

Abra o arquivo pubspec.yaml e adicione as dependências necessárias do Firebase:
yaml

dependencies:
  flutter:
    sdk: flutter
  firebase_core: ^1.10.6
  firebase_auth: ^3.3.11
  cloud_firestore: ^3.1.9
  firebase_messaging: ^11.2.6
Execute o comando para obter os pacotes:
sh
flutter pub get
4. Configurar Firestore:

No Console do Firebase, navegue até Firestore Database
Configure o banco de dados em modo de teste para desenvolvimento
Defina regras de segurança apropriadas para produção
5. Executar o Aplicativo:

Conecte um dispositivo ou inicie um emulador
Execute o comando:
sh
  flutter run
