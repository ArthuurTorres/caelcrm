Este é um projeto simples de CRM (Customer Relationship Management) desenvolvido para corretoras de planos de saúde, utilizando Android com Kotlin e integração com o Firebase. O aplicativo permite gerenciar leads, contatos e tarefas de forma simples e eficiente.

Funcionalidades
Cadastro de Leads: Adiciona novos leads com informações básicas como nome e e-mail.

Exibição de Leads: Visualiza a lista de leads cadastrados.

Gerenciamento de Contatos: Contatos de leads podem ser gerenciados e acessados facilmente.

Gerenciamento de Tarefas: Criação e visualização de tarefas associadas aos leads e contatos.

Tecnologias Utilizadas
Kotlin: Linguagem de programação utilizada para o desenvolvimento Android.

Firebase: Plataforma do Google para gerenciamento de banco de dados (Realtime Database) e autenticação de usuários.

Android Studio: IDE utilizada para o desenvolvimento do aplicativo Android.

RecyclerView: Componente para exibir a lista de leads de maneira eficiente.

Configuração do Projeto
1. Criar um novo projeto no Android Studio
Crie um novo projeto no Android Studio utilizando Kotlin como linguagem de programação.

2. Adicionar dependências no build.gradle
No arquivo build.gradle (do módulo app), adicione as seguintes dependências:

gradle
Copiar
dependencies {
    implementation 'com.google.firebase:firebase-auth:21.0.1'
    implementation 'com.google.firebase:firebase-database:20.0.3'
    implementation 'com.google.android.material:material:1.4.0'
    implementation 'androidx.recyclerview:recyclerview:1.2.1'
    implementation 'androidx.lifecycle:lifecycle-extensions:2.2.0'
    implementation 'androidx.constraintlayout:constraintlayout:2.1.1'
}
3. Configuração do Firebase
Crie um novo projeto no Firebase Console e adicione seu aplicativo Android.

Habilite Firebase Realtime Database e Firebase Authentication.

Baixe o arquivo google-services.json e adicione ao seu projeto no Android Studio.

4. Configuração do Firebase no build.gradle
Adicione a seguinte linha no build.gradle (nível do projeto):

gradle
Copiar
classpath 'com.google.gms:google-services:4.3.10'
E no build.gradle (nível do app):

gradle
Copiar
apply plugin: 'com.google.gms.google-services'
5. Firebase Authentication (opcional)
Se você decidir adicionar login de usuário, configure a autenticação no Firebase Console e use a API de autenticação para gerenciar os usuários que podem acessar o CRM.

Como Rodar o Projeto
Clone o repositório:

bash
Copiar
git clone https://github.com/seu_usuario/seu_repositorio.git
Abra o projeto no Android Studio.

Sincronize o projeto com o Gradle para garantir que as dependências sejam baixadas.

Execute o projeto em um dispositivo Android ou no emulador.

Adicione novos leads através da interface de usuário e visualize-os na lista de leads.

Estrutura do Projeto
MainActivity.kt: Tela principal do aplicativo, que exibe a lista de leads e permite adicionar novos leads.

Lead.kt: Classe de dados que representa um lead (contém id, nome e e-mail).

LeadAdapter.kt: Adaptador utilizado para exibir os leads em uma RecyclerView.

Layouts:

activity_main.xml: Layout para a tela principal, onde os leads são exibidos.

lead_item.xml: Layout para cada item de lead na lista.
