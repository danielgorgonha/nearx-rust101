# Rust 101 - Server Rust

Este repositório faz parte do módulo de Rust do curso **Rust 101**. Aqui, desenvolvemos um servidor simples em Rust, praticando desde a criação de bibliotecas até o trabalho em equipe e o deploy do software.

---

## Conteúdo do Módulo

### 1. Introdução
- Apresentação do módulo e dos objetivos do curso.
- Visão geral sobre a linguagem Rust e suas aplicações.

### 2. Desenvolvendo Software do Zero
- Aprendemos a criar um novo projeto Rust do zero.
- Criamos e publicamos uma biblioteca simples em Rust.

### 3. Desenvolvendo Software do Zero - Parte 2
- Simulamos o trabalho em equipe:
  - Clonando o projeto do repositório.
  - Criando novas branches.
  - Realizando commits e pull requests.
- Como parte dessa etapa, foi solicitado criar este servidor em Rust.

### 4. Submetendo Atividades
- Orientações sobre como submeter as atividades desenvolvidas durante o módulo.

### 5. Deploy do Software
- Aprendemos a criar um `Dockerfile` para o projeto.
- Praticamos o build e deploy do servidor Rust em um container Docker.

### 6. Encerramento
- Revisão dos principais aprendizados do módulo.
- Próximos passos sugeridos para aprofundamento em Rust.

---

## Sobre o Projeto

Este projeto é um servidor simples escrito em Rust, criado para fins didáticos. Ele inclui:

- Estrutura básica de um projeto Rust (`Cargo.toml`, `src/`, etc).
- Suporte a containerização via Docker.
- Práticas de versionamento com Git.

### Estrutura do Projeto

```
.
├── src/            # Código-f
```

### Estrutura do Projeto

---

## Funcionamento do Servidor

O servidor foi implementado usando o framework [Tide](https://github.com/http-rs/tide) e expõe três endpoints HTTP:

### Endpoints

#### 1. `GET /`
- **Descrição:** Endpoint de teste para verificar se o servidor está online.
- **Resposta:**  
  ```
  🖐️ Hello Tide!
  ```

#### 2. `GET /sum/:x/:y`
- **Descrição:** Soma dois números inteiros, incrementando o resultado em 1 (utiliza a função `sum_plus_one` da biblioteca `calc_near_x`).
- **Exemplo:**  
  ```
  GET http://127.0.0.1:3003/sum/2/3
  ```
  **Resposta:**  
  ```
  Resultado: 6
  ```
  *(2 + 3 = 5, mais 1 = 6)*

#### 3. `GET /sub/:x/:y`
- **Descrição:** Subtrai dois números inteiros, decrementando o resultado em 1 (utiliza a função `sub_less_one` da biblioteca `calc_near_x`).
- **Exemplo:**  
  ```
  GET http://127.0.0.1:3003/sub/5/2
  ```
  **Resposta:**  
  ```
  Resultado: 2
  ```
  *(5 - 2 = 3, menos 1 = 2)*

---

## Como rodar o projeto

### Pré-requisitos

- [Rust](https://www.rust-lang.org/tools/install)
- [Docker](https://docs.docker.com/get-docker/) (opcional, para rodar em container)

### Rodando localmente

```bash
cargo run
```

O servidor estará disponível em [http://127.0.0.1:3003](http://127.0.0.1:3003).

### Rodando com Docker

```bash
docker build -t server-rust .
docker run -p 3003:3003 server-rust
```

---

## Exemplos de uso

```bash
# Testando endpoint raiz
curl http://127.0.0.1:3003/

# Somando 10 + 5 (+1)
curl http://127.0.0.1:3003/sum/10/5

# Subtraindo 10 - 5 (-1)
curl http://127.0.0.1:3003/sub/10/5
```

---

## Licença

Este projeto é licenciado sob a licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.
