# 🖥️ TechStock - Controle de Estoque TI

## Descrição

Este é um sistema web simples para gerenciamento de estoque de equipamentos, desenvolvido em Python com Flask. O sistema permite cadastrar, editar, remover e listar produtos, registrar vendas, controlar garantias e autenticar usuários.

**Autor:** Lucas Rodrigues Fernandes

---

## Funcionalidades

* Cadastro completo de equipamentos com detalhes como:

  * Nome
  * Categoria
  * Quantidade
  * Preços
  * Fornecedor
  * Número de série
  * Status
  * Dados de aquisição
  * Garantia
* Edição e remoção de produtos existentes
* Listagem de produtos com dados formatados para fácil visualização
* Registro de vendas com atualização automática do estoque
* Monitoramento de garantias próximas ao vencimento com alertas
* Sistema de login simples para autenticação e proteção das rotas
* Interface web responsiva utilizando templates Jinja2
* Histórico de movimentações de estoque para controle e análise

---

## Tecnologias Utilizadas

* **Linguagem de Programação:** Python 3
* **Framework Web:** Flask
* **Template Engine:** Jinja2 (integrado ao Flask)
* **Gerenciamento de Dados:** módulo `datetime` do Python
* **Controle de Sessão:** sessões do Flask para autenticação simples

---

## Estrutura do Projeto

* `model.py` → Define as classes de domínio (`Equipamento`, `Movimentação`, `EstoqueModel`, `Usuário`) e realiza o gerenciamento dos dados em memória.
* `controller.py` → Contém a lógica de negócio, manipula os dados do modelo e prepara informações para as visualizações.
* `app.py` → Configura as rotas Flask, gerencia requisições HTTP, sessões e renderiza os templates.
* `templates/` → Contém os arquivos HTML das páginas do sistema (login, cadastro, listagem, edição, alertas e vendas).

---

## Como Executar

### 1. Instale as dependências

```bash
pip install flask
```

### 2. Execute o arquivo principal

```bash
python app.py
```

### 3. Acesse no navegador

```bash
http://127.0.0.1:5000/
```

### 4. Faça login com o usuário padrão

| Usuário | Senha |
| ------- | ----- |
| admin   | 1234  |

---

## Observações

* Atualmente o sistema armazena os dados apenas em memória, sem persistência em banco de dados.
* A autenticação implementada é simples e fixa, sendo recomendada apenas para ambiente de desenvolvimento.
* O sistema pode ser expandido futuramente para incluir:

  * Banco de dados
  * Autenticação avançada
  * Novas funcionalidades
  * Melhorias de segurança
