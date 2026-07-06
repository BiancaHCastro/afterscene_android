# AfterScene

Aluno(a): Maria Bianca Holanda de Castro

Entrega: 05/07/2026

Tive essa ideia ao pensar em aplicações como o Skoob (registrar leituras de livros e publicar suas próprias resenhas), IMDB, entre outros, gosto muito de ler livros (principalmente fantasia) e séries, filmes, animes. A ideia é registrar as emoçoes que VOCÊ sentiu ao consumir aquela obra, partindo do ponto que consumimos muito entretenimento e tudo ocorre muito rápido em nossa sociedade liquida, é importante registrar aquilo que sentimos, que nos faz humanos.

## Sobre o Projeto

O **AfterScene** é um aplicativo Android desenvolvido em **Kotlin** com o objetivo de permitir ao usuário criar um catálogo pessoal de filmes, séries, animes e doramas, registrando não apenas informações da obra, mas também a emoção que ela despertou durante a experiência. 

O aplicativo foi desenvolvido como projeto para o curso de Android do Capacita, priorizando uma implementação simples, organizada e seguindo os principais conceitos de desenvolvimento Android moderno.

Todo o funcionamento ocorre **offline**, sem necessidade de conexão com a internet.

---

# Funcionalidades

O aplicativo permite:

- Visualizar uma biblioteca de obras cadastradas;
- Pesquisar obras pelo título;
- Adicionar novas obras;
- Editar obras existentes;
- Excluir registros;
- Selecionar uma imagem da galeria para representar a capa da obra;
- Armazenar permanentemente todas as informações utilizando **Room Database**.

Executar o projeto cadastrando suas obras consumidas (sejam livros, séries, filmes, doramas. etc)

---

# Tecnologias Utilizadas

O projeto foi desenvolvido utilizando as principais bibliotecas recomendadas para aplicações Android modernas:

- Kotlin
- Jetpack Compose
- Material 3
- Navigation Compose
- Room Database
- MVVM (Model-View-ViewModel)
- Repository Pattern
- StateFlow
- Kotlin Coroutines
- Coil (carregamento de imagens)
- Activity Result API (seleção de imagens da galeria)

---

# Arquitetura

O projeto utiliza a arquitetura **MVVM (Model-View-ViewModel)**, promovendo a separação entre interface, lógica de negócio e acesso aos dados.

O fluxo da aplicação ocorre da seguinte forma:

```
Interface (Jetpack Compose)
        ↓
ViewModel
        ↓
Repository
        ↓
Room Database
```

Dessa forma, a interface não acessa diretamente o banco de dados, tornando o código mais organizado e facilitando futuras manutenções.

---

# Persistência de Dados

Para o armazenamento das informações foi utilizado exclusivamente o **Room Database**, banco de dados local recomendado oficialmente pelo Android.

Não foram utilizados bancos de dados externos ou serviços em nuvem, como:

- Firebase;
- MongoDB;
- APIs externas.

Toda a persistência ocorre localmente no dispositivo, permitindo que o aplicativo funcione integralmente **offline**.

---

# Organização do Código

Durante o desenvolvimento buscou-se aplicar conceitos básicos de boas práticas de programação, dentre eles:

- Separação de responsabilidades entre as camadas da aplicação;
- Componentização da interface utilizando Jetpack Compose;
- Utilização de funções pequenas e objetivas;
- Uso de `StateFlow` para gerenciamento de estado;
- Utilização de expressões lambda para callbacks quando apropriado;
- Separação entre interface, lógica de negócio e persistência de dados;
- Nomenclatura clara para classes, funções e variáveis.

Embora seja um projeto de pequeno porte, sua estrutura foi organizada de forma semelhante à utilizada em aplicações Android reais.

---

# Desenvolvimento

Um dos principais desafios encontrados durante o desenvolvimento não esteve relacionado à implementação das funcionalidades do aplicativo, mas sim à configuração do ambiente de desenvolvimento.

A integração entre as bibliotecas do Jetpack Compose, Room, Navigation Compose, Coil e suas respectivas versões exigiu atenção para garantir compatibilidade entre o **Android Studio**, o **Gradle**, o **Android Gradle Plugin (AGP)** e o **Kotlin**.

Também foi necessário utilizar um template padrão para os arquivos de configuração do Gradle (`build.gradle` e `libs.versions.toml`). Por esse motivo, algumas dependências presentes no projeto não são necessariamente utilizadas diretamente na implementação do aplicativo, mas permanecem por fazerem parte da configuração padrão gerada para garantir estabilidade e compatibilidade entre as bibliotecas.

Outro desafio recorrente foi a execução do projeto no Android Studio, principalmente durante os testes em emuladores, envolvendo sincronização do Gradle, configuração do SDK, reconstrução do projeto e resolução de erros relacionados ao ambiente de desenvolvimento, situações comuns para desenvolvedores iniciantes em aplicações Android.

---

# Uso de Inteligência Artificial

Foi utilizado:

- **Uso da IA Gemini do Google como auxiliar de correção de código Kotlin e ChatGPT para escrita deste arquivo README.**

---

# Considerações Finais

O projeto permitiu aplicar, de forma prática, conceitos fundamentais do desenvolvimento Android moderno, como a construção de interfaces declarativas com Jetpack Compose, navegação entre telas, persistência local utilizando Room Database e organização da aplicação por meio da arquitetura MVVM.

Mesmo sendo um aplicativo simples, o desenvolvimento proporcionou experiência com boas práticas de organização do código, gerenciamento de estado e separação de responsabilidades, formando uma base importante para projetos Android de maior complexidade no futuro.