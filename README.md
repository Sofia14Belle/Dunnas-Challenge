# Projeto Sistema de Controle de Entrada de Visitantes com Ruby on Rails

# Integrantes
- Keyllian7
- Sofia14Belle

# Sumário

- [📚 Antes de qualquer coisa, leia...](#antes-de-qualquer-coisa-leia)
- [💪 Desafio Proposto](#desafio-proposto)
  - [Objetivo do Projeto](#objetivo-do-projeto)
  - [Funcionalidades principais](#funcionalidades-principais)
  - [Estrutura da Instituição](#estrutura-da-instituição)
  - [Níveis de Permissão de Usuário](#níveis-de-permissão-de-usuário)
- [⚙️ Tecnologias Utilizadas](#tecnologias-utilizadas)
  - [Ruby on Rails](#ruby-on-rails)
  - [Tailwind CSS](#tailwind-css)
  - [Rubocop](#rubocop)
- [🛠️ Ferramentas Utilizadas](#ferramentas-utilizadas)
- [🔧 Principais Gems Utilizadas](#principais-gems-utilizadas)
- [📚 Materiais de Apoio Utilizados para o Desenvolvimento](#materiais-de-apoio-utilizados-para-o-desenvolvimento)
- [💼 Serviços](#serviços)
  - [Serviço de E-mail](#serviço-de-e-mail)
  - [Serviço AWS](#serviço-aws)
  - [Docker](#docker)
- [🔒 Permissões](#permissões)
- [🗃️ Banco de Dados](#banco-de-dados)
  - [Normalização do Banco de Dados](#normalização-do-banco-de-dados)
  - [Relacionamentos, Chaves Estrangeiras, Enums e Validações](#relacionamentos-chaves-estrangeiras-enums-e-validações)
- [🚀 Executando o Projeto](#executando-o-projeto)
  - [Passo 1: Instalar Dependências](#passo-1-instalar-dependências)
  - [Passo 2: Configuração do Banco de Dados](#passo-2-configuração-do-banco-de-dados)
  - [Passo 3: Executar o Projeto com Docker](#passo-3-executar-o-projeto-com-docker)
  - [Passo 4: Acessar o Projeto](#passo-4-acessar-o-projeto)
- [🧪 Testes](#testes)
- [📝 Documentação da API](#documentação-da-api)
- [🙌 Contribuições](#contribuições)
- [🖼️ Imagens da Web do Projeto](#imagens-da-web-do-projeto)
- [💻 Ainda sobre o Desenvolvimento](#ainda-sobre-o-desenvolvimento)
- [📄 Licença](#licença)


## 💪 Desafio Proposto

### Objetivo do Projeto  

O sistema tem como objetivo armazenar os registros de entradas de pessoas (visitantes) que frequentam uma determinada unidade de uma instituição.

### Funcionalidades principais:  

- **Cadastro de visitantes**: Solicita informações como CPF, nome, RG, telefone e foto (webcam).  
- **Consulta de visitantes**: Se o visitante já estiver cadastrado, ao preencher o CPF, o sistema preenche os dados automaticamente.  
- **Registro de visita**: Solicita o setor e o funcionário (opcional) ao qual a visita será realizada, e registra a data e hora da entrada.  

### Estrutura da Instituição:  
- A instituição possui **várias unidades**, sendo que cada unidade armazena apenas os dados das visitas realizadas nela, mas compartilha o cadastro dos visitantes para agilizar o processo.  
- **Setores e Funcionários**: Cada unidade possui vários setores e funcionários, que devem ser informados no momento do registro de uma visita.  

### Níveis de Permissão de Usuário:  
- **Administrador**: Pode cadastrar unidades, setores, funcionários e usuários.  
- **Atendente**: Responsável pelo cadastro de visitantes e registro de visitas apenas na sua unidade.  
- **Funcionário**: Pode visualizar a lista de visitantes aguardando e notificar o sistema sobre a realização da visita.  
- O sistema exibe as funcionalidades conforme a permissão de cada usuário.  

### Tecnologias e Ferramentas Utilizadas:  
- **Sistema Web**  
- **Arquitetura MVC** com Ruby on Rails  
- **Ruby** como linguagem de programação  
- **Devise** para autenticação de usuários  
- **Cancancan** para controle de permissões de usuários  

## ⚙️ Tecnologias Utilizadas  

### Ruby on Rails  
O projeto é desenvolvido utilizando **Ruby on Rails**, uma framework web popular para construção de aplicações web de forma rápida e eficiente.

### Tailwind CSS  
Este projeto utiliza o [**Tailwind CSS**](https://tailwindcss.com/) para a estilização. O Tailwind é um framework CSS utilitário que permite criar designs modernos e responsivos de maneira prática e ágil.

#### Configuração do Tailwind CSS  
O Tailwind CSS está configurado no arquivo **[Procfile.dev](Procfile.dev)** para ser observado e recompilado automaticamente durante o desenvolvimento. A configuração é a seguinte:

```dev
web: bin/rails server
css: bin/rails tailwindcss:watch
```

#### Arquivo de Estilos  
Os estilos globais do Tailwind CSS são importados no arquivo **application.css**:

```css
@import "tailwindcss";
```

Para mais informações sobre como utilizar o Tailwind CSS, consulte a [documentação oficial](https://tailwindcss.com/docs).

### Rubocop  
Por padrão, o **Rubocop** já vem configurado em projetos Rails, mas com configurações básicas. Para melhorar a qualidade do código, utilizei um repositório com configurações avançadas de linter recomendadas para projetos Rails.

Repositório: [Standard Ruby](https://github.com/standardrb/standard/blob/main/config/base.yml)

Se quiser as configurações avançadas, basta copiar o arquivo **base.yml** e colocá-lo no seu **.rubocop.yml** na raiz do projeto.

## 🛠️ Ferramentas Utilizadas  

### Docker & Portainer  
- **Docker** foi utilizado para criar contêineres no ambiente de desenvolvimento, garantindo um processo de configuração e execução mais eficiente.
- **Portainer** foi adotado como interface web para gerenciar os contêineres Docker de maneira visual e intuitiva.

### Git & GitHub  
- **Git** foi utilizado para o controle de versão do projeto.
- **GitHub** foi a plataforma escolhida para hospedar o repositório e possibilitar a colaboração.

### DBeaver  
- **DBeaver** foi utilizado para o gerenciamento e manipulação do banco de dados, oferecendo uma interface gráfica que facilita o gerenciamento das tabelas e dados.

### VSCode  
- **Visual Studio Code (VSCode)** foi a principal IDE utilizada no desenvolvimento do código, com suporte a diversas extensões que aumentam a produtividade e eficiência.

### Terminal (Linux)  
- O **terminal Linux** foi amplamente utilizado para realizar operações no sistema, além de interagir diretamente com o projeto.

### DBdiagram.io  
- Utilizei o **dbdiagram.io** para modelar o banco de dados, criando diagramas relacionais que ajudam a visualizar a estrutura e as interações entre as tabelas.

### Inteligência Artificial  
- A **Inteligência Artificial** foi utilizada para esclarecer dúvidas, analisar erros, buscar exemplos e outras finalidades de suporte. **NUNCA** foi utilizada para escrever código diretamente no projeto.
### Notion  
- O **Notion** foi utilizado para anotações, definição de metas, organização de ideias e planejamento geral do projeto.

### Draw.io  
- Utilizei o **Draw.io** para compreender melhor o projeto e criar modelos, como fluxos de dados e diagramas de arquitetura.

## 🔧 Principais Gems Utilizadas  

- **rails (~> 8.0.1)**: Framework principal para o desenvolvimento de aplicações web.
- **pg (~> 1.5, >= 1.5.6)**: Gem para integração com o banco de dados **PostgreSQL**.
- **dotenv-rails (~> 2.1, >= 2.1.1)**: Carrega variáveis de ambiente a partir de um arquivo **.env**.
- **devise**: Gem para autenticação de usuários.
- **cancancan**: Gem para controle de permissões e autorização de usuários.
- **carrierwave (~> 2.0)**: Responsável pelo **upload de arquivos**.
- **mini_magick**: Utilizada para o **processamento de imagens**.
- **fog-aws**: Gem para **armazenamento de arquivos na AWS S3**.
- **brazilian_documents (~> 0.1.4)**: Valida documentos brasileiros, como **CPF** e **RG**.
- **phonelib**: Realiza a **validação de números de telefone**.
- **puma (>= 5.0)**: Servidor web utilizado para rodar a aplicação.

## 📚 Materiais de Apoio Utilizados para o Desenvolvimento  

### YouTube  
Um canal que me ajudou bastante durante o processo foi o **RailsGO**. Recomendo a todos que estão aprendendo Ruby on Rails!  
[RailsGO no YouTube](https://www.youtube.com/@GorailsTV)

### Documentações  

- [**Cancancan**](https://github.com/CanCanCommunity/cancancan) - Gem para controle de permissões e autorização de usuários.  
- [**Carrierwave**](https://github.com/carrierwaveuploader/carrierwave) - Gem para upload de arquivos.  
- [**Phonelib**](https://github.com/daddyz/phonelib) - Gem para validação de números de telefone.  
- [**Devise**](https://github.com/heartcombo/devise) - Gem para autenticação de usuários.  
- [**dotenv**](https://github.com/bkeepers/dotenv) - Gem para carregar variáveis de ambiente.  
- [**Tailwind UI**](https://tailwindui.com/) - Recursos e componentes prontos para o Tailwind CSS.  
- [**Brazilian Documents**](https://github.com/fidelisrafael/brazilian_documents) - Validação de documentos brasileiros.  
- [**Getting Started with Rails**](https://guides.rubyonrails.org/getting_started.html#controllers-actions) - Guia oficial para começar com Rails.  
- [**Ruby Documentation**](https://www.ruby-lang.org/pt/documentation/) - Documentação oficial da linguagem Ruby.  
- [**Webcam API - MDN**](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia) - Documentação sobre o uso da webcam no navegador.  
- [**Standard Ruby**](https://github.com/standardrb/standard) - Repositório com configurações de linter para Ruby.

## 💼 Serviços

### Serviço de E-mail  

O projeto utiliza o **Action Mailer** para enviar e-mails pelos serviços da gem **Devise**. Para isso, escolhi o serviço do **Gmail**. A configuração do serviço de e-mail está no arquivo `development.rb`:

```rb
config.action_mailer.delivery_method = :smtp
config.action_mailer.smtp_settings = {
  address: "smtp.gmail.com",
  port: 587,
  domain: "gmail.com",
  user_name: ENV["EMAIL_GMAIL"],
  password: ENV["PASSWORD_GMAIL"],
  authentication: "plain",
  enable_starttls_auto: true
}
```

Aqui, as credenciais de e-mail são carregadas a partir das variáveis de ambiente, garantindo a segurança das informações sensíveis.

### Serviço AWS  

O projeto utiliza o **AWS S3** para armazenamento de fotos dos visitantes e usuários. A configuração do serviço está no arquivo `carrierwave.rb`, que utiliza a gem **CarrierWave** para integrar o armazenamento no S3:

```rb
CarrierWave.configure do |config|
  config.fog_credentials = {
    provider: "AWS",
    aws_access_key_id: ENV["AWS_ACCESS_KEY_ID"],
    aws_secret_access_key: ENV["AWS_SECRET_ACCESS_KEY"],
    region: ENV["AWS_REGION"],
    endpoint: "https://s3.sa-east-1.amazonaws.com"
  }

  config.fog_directory = ENV["AWS_BUCKET_NAME"]
  config.fog_public = false
  config.fog_attributes = {"Cache-Control" => "max-age=315576000"}
end
```

As credenciais de acesso à AWS também são carregadas a partir das variáveis de ambiente para garantir a segurança das informações sensíveis.

### Docker  

O projeto está configurado para ser executado em **containers Docker**. Abaixo está a configuração necessária para rodar a aplicação em um ambiente isolado.

#### Dockerfile  
O arquivo **Dockerfile** contém a configuração para a criação da imagem Docker:

```dockerfile
FROM ruby:3.2.0

RUN apt-get update -qq && apt-get install -y \
  build-essential \
  libpq-dev \
  nodejs \
  postgresql-client

WORKDIR /app

COPY Gemfile Gemfile.lock ./

RUN bundle install

COPY . .

EXPOSE 3000

CMD ["bash", "-c", "rm -f tmp/pids/server.pid && bundle exec rails server -b '0.0.0.0'"]
```

#### docker-compose.yml  
O arquivo **docker-compose.yml** é utilizado para organizar os containers, definindo as configurações de rede e volumes:

```yml
version: '3'

services:

  db:
    image: postgres
    restart: always
    ports:
      - "5432:5432"
    volumes:
      - ./pgdata:/data/postgres
    environment:
      POSTGRES_USER: ${POSTGRES_USER}
      POSTGRES_PASSWORD: ${POSTGRES_PASSWORD}
      POSTGRES_DB: ${POSTGRES_DB}
    networks:
      - app-network

  web:
    build:
      context: .
      dockerfile: Dockerfile
    command: bash -c "rm -f tmp/pids/server.pid && bundle exec rails server -b '0.0.0.0'"
    volumes:
      - ".:/app"
    ports:
      - "3000:3000"
    depends_on:
      - db
    networks:
      - app-network

volumes:
    pgdata:
      driver: local

networks:
  app-network:
```

#### Explicação:
- **Dockerfile**: Define a construção da imagem Docker, incluindo dependências necessárias e a execução do servidor Rails.
- **docker-compose.yml**: Configura os containers para o banco de dados (PostgreSQL) e o servidor web (Rails), garantindo que ambos compartilhem a mesma rede e volumes persistentes.

## 🔒 Permissões  

As permissões no sistema são baseadas em **roles** (funções) dos usuários, e os valores para cada role são os seguintes:
- **0** = **employee** (funcionário)
- **1** = **attendant** (atendente)
- **2** = **admin** (admin)

A gem **CanCanCan** é usada para configurar as permissões dos usuários. Você pode encontrar o arquivo de permissões completo em `app/models/ability.rb`.

### Exemplo de Configuração de Permissões:

```ruby
def initialize(user)
  case user.role
  when "admin"
    can :manage, :all
  when "attendant"
    can :read, Visit, unit_id: user.unit_id
    can :read, Visitor

    can :update, Visit, unit_id: user.unit_id
    can :update, Visitor

    can :create, Visit
    can :create, Visitor

    can :verify_by_cpf, Visitor
  when "employee"
    can :read, Visit, unit_id: user.unit_id
    can :update, Visit, unit_id: user.unit_id
  end
end
```

#### Explicação:
- **Admin** tem permissões completas e pode gerenciar todos os recursos do sistema.
- **Attendant** pode ler, criar e atualizar registros de visitas e visitantes dentro da sua unidade específica, além de realizar a verificação por **CPF** de visitantes.
- **Employee** pode ler e atualizar visitas dentro da sua unidade.

## 🗃️ Banco de Dados

### Normalização do Banco de Dados

O banco de dados foi projetado e estruturado de acordo com as três primeiras formas normais (1FN, 2FN e 3FN), garantindo um alto nível de integridade e eficiência na organização dos dados.

#### Explicação das Três Formas Normais:

- **Primeira Forma Normal (1FN)**: Todas as colunas nas tabelas contêm valores atômicos, sem campos que armazenem múltiplos valores ou listas. Cada valor é único e independente dentro de suas respectivas colunas.
  
- **Segunda Forma Normal (2FN)**: Todas as colunas não-chave dependem completamente da chave primária, eliminando dependências parciais.
  
- **Terceira Forma Normal (3FN)**: Não há dependências transitivas entre as colunas, ou seja, as colunas dependem apenas da chave primária e não umas das outras.

![Banco de dados - Imagem](https://drive.google.com/uc?export=view&id=1Aj0z4ckj0zLDjRgKxzx2OSrZ0qlupNOu)

### Relacionamentos, Chaves Estrangeiras, Enums e Validações

#### Tabelas e Relacionamentos:

![Diagrama ER](https://drive.google.com/uc?id=1KcNN1DS-6CjBhkOGVfSnuuTzJQuA_iHS)

#### Explicação das Notações na Imagem:
- **1..n**: Um para muitos
- **1..1**: Um para um
- **n..1**: Muitos para um
- **n..n**: Muitos para muitos

#### Tabelas e Relacionamentos:
1. **Tabela `sectors` (Setores)**:
   - `belongs_to :unit`: Cada setor pertence a uma unidade.
   - `has_many :visits`: Um setor pode ter várias visitas registradas.

2. **Tabela `units` (Unidades)**:
   - `has_many :sectors`: Uma unidade pode ter vários setores.
   - `has_many :users`: Uma unidade pode ter vários usuários.
   - `has_many :visits`: Uma unidade pode ter várias visitas.

3. **Tabela `users` (Usuários)**:
   - `belongs_to :unit, optional: true`: Um usuário pertence a uma unidade (opcional).
   - `belongs_to :sector, optional: true`: Um usuário pertence a um setor (opcional).
   - `has_many :visits`: Um usuário pode ter várias visitas.

4. **Tabela `visitors` (Visitantes)**:
   - `has_many :visits`: Um visitante pode ter várias visitas.

5. **Tabela `visits` (Visitas)**:
   - `belongs_to :visitor`: Cada visita pertence a um visitante.
   - `belongs_to :unit`: Cada visita pertence a uma unidade.
   - `belongs_to :sector`: Cada visita pertence a um setor.
   - `belongs_to :user, optional: true`: Cada visita pode ser associada a um usuário, mas isso é opcional.

### Relacionamentos de Chaves Estrangeiras:
- **`sectors`**: Tem uma chave estrangeira (`unit_id`) que se relaciona com a tabela `units`.
- **`users`**: Tem chaves estrangeiras (`unit_id`, `sector_id`) que se relacionam com `units` e `sectors`.
- **`visits`**: Tem chaves estrangeiras (`visitor_id`, `unit_id`, `sector_id`, `user_id`) que se relacionam com `visitors`, `units`, `sectors` e `users`.

### Enum:
- **Campo `status`** da tabela **`visits`**: Define o status da visita com os seguintes valores:
  - `pending` (pendente)
  - `completed` (completada)
  - `absent` (ausente)
  
- **Campo `role`** da tabela **`users`**: Define o papel do usuário com os seguintes valores:
  - `employee` (funcionário)
  - `attendant` (atendente)
  - `admin` (administrador)

### Validações:
- **Validações em várias tabelas** garantem que os dados inseridos sejam válidos, como CPF, RG, e-mail, entre outros.
- **`User`** e **`Visitor`** possuem validações específicas para Telefone, CPF e RG, garantindo que sigam os padrões brasileiros.

## 🚀 Executando o Projeto

### Passo 1: Instalar Dependências

1. **Clone o repositório do projeto:**

   Se você ainda não tem o projeto em sua máquina local, clone o repositório utilizando o comando:

   ```sh
   git clone <URL_DO_REPOSITORIO>
   ```

2. **Navegue até a pasta do projeto:**

   Entre na pasta do projeto com o comando:

   ```sh
   cd nome-do-projeto
   ```

3. **Crie o arquivo `.env`:**

   Na raiz do projeto, crie um arquivo `.env` com as variáveis de ambiente necessárias. Para isso, adicione os seguintes parâmetros (sem valores) conforme descrito:

   ```env
   POSTGRES_USER=seu_usuario_no_banco
   POSTGRES_PASSWORD=sua_senha_do_banco
   POSTGRES_DB=nome_do_banco
   DATABASE_HOST=localhost
   EMAIL_GMAIL=seu_email@gmail.com
   PASSWORD_GMAIL=sua_senha_de_aplicativo
   AWS_ACCESS_KEY_ID=sua_chave_de_acesso_aws
   AWS_SECRET_ACCESS_KEY=sua_chave_secreta_aws
   AWS_BUCKET_NAME=seu_nome_do_bucket_aws
   AWS_REGION=regiao_do_bucket_aws
   ```
#### Explicação das Variáveis:
  - **POSTGRES_USER**, **POSTGRES_PASSWORD**, **POSTGRES_DB**: Credenciais e informações de configuração para o banco de dados PostgreSQL.
  - **DATABASE_HOST**: O endereço onde o banco de dados está hospedado (geralmente `localhost` durante o desenvolvimento local).
  - **EMAIL_GMAIL** e **PASSWORD_GMAIL**: Credenciais de acesso ao serviço de e-mail via **Gmail** para enviar e-mails através do **Action Mailer**.
  - **AWS_ACCESS_KEY_ID**, **AWS_SECRET_ACCESS_KEY**, **AWS_BUCKET_NAME**, **AWS_REGION**: Credenciais e informações relacionadas ao uso do **AWS S3** para o armazenamento de arquivos.

4. **Instale as dependências com o `bundle`:**

   Para instalar as dependências do projeto, execute o seguinte comando:

   ```sh
   bundle install
   ```

   Isso irá baixar e instalar todas as gems necessárias para o projeto.

---

### Passo 2: Configuração do Banco de Dados

5. **Crie o banco de dados:**

   Execute o seguinte comando para criar o banco de dados:

   ```sh
   bin/rails db:create
   ```

6. **Execute as migrações:**

   Depois de criar o banco de dados, execute as migrações para criar as tabelas necessárias:

   ```sh
   bin/rails db:migrate
   ```

7. **Popule o banco com dados iniciais (seeds):**

   Se você desejar adicionar dados iniciais ao banco (como um usuário administrador), execute o comando:

   ```sh
   bin/rails db:seed
   ```

   **Nota:** O comando `seed` acima irá gerar um usuário admin com as seguintes informações, mas antes de executá-lo, vá até o model de `user` e desative a validação de foto. Execute o comando e depois reative a validação de foto, pois há um bug que impede a            execução correta sem essa alteração, uma possível solução seria utilizar outra gem para o upload de fotos, mas, por enquanto, mantive a atual para atender aos requisitos do projeto.

   O arquivo está em: `app/models/user.rb`

   **Altere a validação de foto temporariamente:**

   ```ruby
   validates :photo, presence: false  # Desative a validação temporariamente
   ```

   Após rodar o `db:seed`, reative a validação:

   ```ruby
   validates :photo, presence: true
   ```

   **Dados do Usuário Admin para o `seed`:**

   ```sh
   email: "keyllianazevedo2@gmail.com"
   password: "123456",
   password_confirmation: "123456",
   confirmed_at: Time.now,
   role: 2,
   cpf: "24327784052",  # CPF gerado pelo site https://www.4devs.com.br/gerador_de_cpf
   rg: "123456789",
   name: "Keyllian Azevedo",
   telephone: "55 92 36170584",  # Telefone gerado pelo site https://geradornv.com.br/gerador-telefone/
   ```

---

### Passo 3: Executar o Projeto com Docker

8. **Suba os containers com Docker Compose:**

   Caso você queira rodar o projeto em containers Docker, execute:

   ```sh
   docker-compose up
   ```

   Isso irá levantar os containers para o banco de dados e a aplicação, conforme descrito no `docker-compose.yml`.

---

### Passo 4: Acessar o Projeto

9. **Acesse a aplicação:**

  Se tudo ocorrer sem erros, a aplicação estará disponível em `http://localhost:3000`. Caso ocorra algum erro durante a execução, consulte os logs ou entre em contato para que eu possa te ajudar a resolver.

---

## ⚙️ Outros Comandos Úteis

- **Parar o Docker Compose:**

   Se você estiver usando Docker, para parar os containers, execute:

   ```sh
   docker-compose down
   ```

- **Rodar o servidor sem Docker:**

   Caso você não esteja utilizando Docker, pode rodar o servidor localmente com o comando:

   ```sh
   bin/rails server
   ```

---

## 🧪 Testes

Por conta do limitado tempo de desenvolvimento, não consegui criar testes unitários, mas caso você queira criar testes e executá-los, o comando é o seguinte:

```sh
bin/rails test
```

Este comando executará os testes do projeto (caso existam) e mostrará os resultados no terminal.

Se você for adicionar ou criar novos testes, pode usar as funcionalidades da framework de testes do Rails, como **Test::Unit** ou **RSpec**, dependendo de como preferir estruturar seus testes.

Aqui está a seção completa de **Documentação da API** para o seu guia de execução do projeto:

---

## 📝 Documentação da API

Neste período, o tempo foi corrido e, por isso, não consegui implementar o Swagger para a documentação das rotas. No entanto, aqui estão as principais rotas da API gerado por IA:

### Autenticação

- **POST /users/sign_in**
  - **Descrição**: Realiza o login do usuário.
  - **Parâmetros**:
    - `email`: string (obrigatório)
    - `password`: string (obrigatório)
  - **Respostas**:
    - `200 OK`: Login bem-sucedido.
    - `401 Unauthorized`: Credenciais inválidas.

- **DELETE /users/sign_out**
  - **Descrição**: Realiza o logout do usuário.
  - **Respostas**:
    - `204 No Content`: Logout bem-sucedido.

---

### Usuários

- **POST /users**
  - **Descrição**: Cria um novo usuário.
  - **Parâmetros**:
    - `email`: string (obrigatório)
    - `password`: string (obrigatório)
    - `name`: string (obrigatório)
    - `cpf`: string (obrigatório)
    - `rg`: string (obrigatório)
    - `telephone`: string (obrigatório)
    - `photo`: arquivo (obrigatório)
    - `role`: integer (obrigatório)
    - `unit_id`: uuid (opcional)
    - `sector_id`: uuid (opcional)
  - **Respostas**:
    - `201 Created`: Usuário criado com sucesso.
    - `422 Unprocessable Entity`: Erro de validação.

- **GET /users**
  - **Descrição**: Retorna a lista de usuários.
  - **Respostas**:
    - `200 OK`: Lista de usuários.

---

### Visitantes

- **GET /visitors**
  - **Descrição**: Retorna a lista de visitantes.
  - **Respostas**:
    - `200 OK`: Lista de visitantes.

- **POST /visitors**
  - **Descrição**: Cria um novo visitante.
  - **Parâmetros**:
    - `name`: string (obrigatório)
    - `cpf`: string (obrigatório)
    - `rg`: string (obrigatório)
    - `telephone`: string (obrigatório)
    - `photo`: arquivo (obrigatório)
  - **Respostas**:
    - `201 Created`: Visitante criado com sucesso.
    - `422 Unprocessable Entity`: Erro de validação.

- **GET /visitors/:id**
  - **Descrição**: Retorna os detalhes de um visitante específico.
  - **Parâmetros**:
    - `id`: uuid (obrigatório)
  - **Respostas**:
    - `200 OK`: Detalhes do visitante.
    - `404 Not Found`: Visitante não encontrado.

---

### Visitas

- **GET /visits**
  - **Descrição**: Retorna a lista de visitas.
  - **Respostas**:
    - `200 OK`: Lista de visitas.

- **POST /visits**
  - **Descrição**: Cria uma nova visita.
  - **Parâmetros**:
    - `visitor_id`: uuid (obrigatório)
    - `unit_id`: uuid (obrigatório)
    - `sector_id`: uuid (obrigatório)
    - `user_id`: uuid (opcional)
    - `date_time`: datetime (obrigatório)
    - `status`: integer (obrigatório)
  - **Respostas**:
    - `201 Created`: Visita criada com sucesso.
    - `422 Unprocessable Entity`: Erro de validação.

- **GET /visits/:id**
  - **Descrição**: Retorna os detalhes de uma visita específica.
  - **Parâmetros**:
    - `id`: uuid (obrigatório)
  - **Respostas**:
    - `200 OK`: Detalhes da visita.
    - `404 Not Found`: Visita não encontrada.

---

### Setores

- **GET /sectors**
  - **Descrição**: Retorna a lista de setores.
  - **Respostas**:
    - `200 OK`: Lista de setores.

- **POST /sectors**
  - **Descrição**: Cria um novo setor.
  - **Parâmetros**:
    - `name`: string (obrigatório)
    - `unit_id`: uuid (obrigatório)
  - **Respostas**:
    - `201 Created`: Setor criado com sucesso.
    - `422 Unprocessable Entity`: Erro de validação.

- **GET /sectors/:id**
  - **Descrição**: Retorna os detalhes de um setor específico.
  - **Parâmetros**:
    - `id`: uuid (obrigatório)
  - **Respostas**:
    - `200 OK`: Detalhes do setor.
    - `404 Not Found`: Setor não encontrado.

---

### Unidades

- **GET /units**
  - **Descrição**: Retorna a lista de unidades.
  - **Respostas**:
    - `200 OK`: Lista de unidades.

- **POST /units**
  - **Descrição**: Cria uma nova unidade.
  - **Parâmetros**:
    - `name`: string (obrigatório)
    - `email`: string (opcional)
  - **Respostas**:
    - `201 Created`: Unidade criada com sucesso.
    - `422 Unprocessable Entity`: Erro de validação.

- **GET /units/:id**
  - **Descrição**: Retorna os detalhes de uma unidade específica.
  - **Parâmetros**:
    - `id`: uuid (obrigatório)
  - **Respostas**:
    - `200 OK`: Detalhes da unidade.
    - `404 Not Found`: Unidade não encontrada.

---

Caso queira documentar mais rotas ou utilizar ferramentas como o Swagger no futuro, você pode facilmente adicionar essas rotas a partir dessa estrutura inicial.

## 🙌 Contribuições

Contribuições para este projeto são bem-vindas! Se você deseja melhorar ou adicionar algo ao projeto, fique à vontade para:

1. **Abrir Issues**: Caso encontre algum bug, tenha sugestões de melhorias ou queira discutir novas funcionalidades, abra uma *issue* para que possamos analisar e discutir a melhor forma de implementar.
   
2. **Criar Pull Requests (PRs)**: Se você desenvolveu alguma funcionalidade, corrigiu um bug ou fez melhorias, envie um *pull request* para a branch principal. As contribuições serão avaliadas e, se estiverem de acordo com os padrões do projeto, serão aceitas.

Se este projeto tiver continuidade, podemos seguir desenvolvendo e evoluindo juntos!

Agradeço qualquer contribuição!

## 🖼️ Imagens da Web do Projeto

Antes de ver a parte web do projeto, gostaria de pedir desculpas por não ter um designer dedicado e por não ser muito experiente na parte de front-end. Contudo, tentei fazer algo simples, prático e agradável. Os modelos de views foram baseados na documentação com *show*, *index*, *update*, *delete* e *new*, então todos os modelos seguem a mesma estrutura, claro que com variações nas informações de cada modelo.

Abaixo estão algumas imagens do projeto. Para ver o projeto completo, acesse o link do vídeo no YouTube, onde mostro o projeto em detalhes!

| Imagem | Link |
|--------|------|
| ![Imagem 1](https://drive.google.com/uc?id=14ICIj5ZtOtkDbvcueNPZ5XTqXJGoD4Nw) | [Visualizar](https://drive.google.com/file/d/14ICIj5ZtOtkDbvcueNPZ5XTqXJGoD4Nw/view?usp=sharing) |
| ![Imagem 2](https://drive.google.com/uc?id=17i-1K-f765ZyIaOIjhvdDahx3v6kGTh9) | [Visualizar](https://drive.google.com/file/d/17i-1K-f765ZyIaOIjhvdDahx3v6kGTh9/view?usp=sharing) |
| ![Imagem 3](https://drive.google.com/uc?id=1Bd2llu4iMPJl9683CTk_Schcm51rq4ki) | [Visualizar](https://drive.google.com/file/d/1Bd2llu4iMPJl9683CTk_Schcm51rq4ki/view?usp=sharing) |
| ![Imagem 4](https://drive.google.com/uc?id=1UF7UeOZEwE_ksMnNO3afY41CpBhJuJdS) | [Visualizar](https://drive.google.com/file/d/1UF7UeOZEwE_ksMnNO3afY41CpBhJuJdS/view?usp=sharing) |
| ![Imagem 5](https://drive.google.com/uc?id=1Yj9eiZcUUtKVifK09HmC5s1DOLhCSPlG) | [Visualizar](https://drive.google.com/file/d/1Yj9eiZcUUtKVifK09HmC5s1DOLhCSPlG/view?usp=sharing) |
| ![Imagem 6](https://drive.google.com/uc?id=1a6d5gbJCJXbBO-O7q1sRchiYv4PEg1Pe) | [Visualizar](https://drive.google.com/file/d/1a6d5gbJCJXbBO-O7q1sRchiYv4PEg1Pe/view?usp=sharing) |
| ![Imagem 7](https://drive.google.com/uc?id=1a_trbil75wTzCvC1xuPCne29Oyc6B45P) | [Visualizar](https://drive.google.com/file/d/1a_trbil75wTzCvC1xuPCne29Oyc6B45P/view?usp=sharing) |
| ![Imagem 8](https://drive.google.com/uc?id=1bkPfpqzHJP8_qT9ayBml5VDjcLMCnEnN) | [Visualizar](https://drive.google.com/file/d/1bkPfpqzHJP8_qT9ayBml5VDjcLMCnEnN/view?usp=sharing) |
| ![Imagem 9](https://drive.google.com/uc?id=1dw1PGjswhR5IJBLKlbirC0bjzu-wQIAN) | [Visualizar](https://drive.google.com/file/d/1dw1PGjswhR5IJBLKlbirC0bjzu-wQIAN/view?usp=sharing) |
| ![Imagem 10](https://drive.google.com/uc?id=1qYqtKCpCSX5dXaicO8JCNKQJQWBScxr7) | [Visualizar](https://drive.google.com/file/d/1qYqtKCpCSX5dXaicO8JCNKQJQWBScxr7/view?usp=sharing) |
| ![Imagem 11](https://drive.google.com/uc?id=1zK6jR4d2xAOKPUgu8PUCCbR7rPHcU89G) | [Visualizar](https://drive.google.com/file/d/1zK6jR4d2xAOKPUgu8PUCCbR7rPHcU89G/view?usp=sharing) |

### Como baixar as imagens

1. Clique no link de "Visualizar" correspondente à imagem desejada.
2. Você será redirecionado para o Google Drive, onde poderá visualizar e baixar a imagem.

---

## 💻 Ainda sobre o Desenvolvimento

Aqui estão algumas imagens das anotações que fiz durante o desenvolvimento. Não considere a bagunça hahaha!

![Anotação 1](https://drive.google.com/uc?id=1QPIVChj53cs7izm-cYklBcrH-VpZuSig)
![Anotação 2](https://drive.google.com/uc?id=1ueWf7o7s2QLQ5ESViJU8oUnumVK0-37g)
![Anotação 3](https://drive.google.com/uc?id=14_BNf_yNBqaACm4LAurvjGOEVXjfgzL5)

---

## 📄 Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

---
