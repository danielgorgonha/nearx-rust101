# Modulo01 - Introdução ao ambiente Rust

Este módulo apresenta o ambiente de desenvolvimento Rust, ideal para quem está começando e quer entender o básico da linguagem e do ecossistema Rust.

## O que é Rust?
Rust é uma linguagem de programação moderna, focada em segurança, desempenho e concorrência. Ela é utilizada para construir desde sistemas embarcados até aplicações web de alta performance.

## Como montar o ambiente Rust

### 1. Instalação do Rust
A maneira recomendada de instalar o Rust é usando o gerenciador de versões `rustup`.

No terminal, execute:
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
Siga as instruções na tela para concluir a instalação.

### 2. Verificando a instalação
Após instalar, feche e reabra o terminal, então execute:
```bash
rustc --version
```
Você deve ver a versão instalada do Rust.

### 3. Instalando o Visual Studio Code (VSCode) e extensões
- Baixe o VSCode em: https://code.visualstudio.com/
- Instale a extensão "rust-analyzer" para suporte avançado ao Rust.

### 4. Criando seu primeiro projeto
No terminal, execute:
```bash
cargo new hello_rust
cd hello_rust
cargo run
```
Você verá a mensagem `Hello, world!` no terminal.

Pronto! Seu ambiente Rust está configurado para começar a programar.
