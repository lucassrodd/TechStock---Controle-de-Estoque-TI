# 🖥️ TechStock-Controle-de-Estoque TI

## Descrição
Este é um sistema web simples para gerenciamento de estoque de equipamentos, desenvolvido em Python com Flask. Permite cadastrar, editar, remover e listar produtos, registrar vendas, controlar garantias e autenticar usuários.

**Autor:** Lucas Rodrigues Fernandes 

---

## Funcionalidades
- Cadastro completo de equipamentos com detalhes como nome, categoria, quantidade, preços, fornecedor, número de série, status, dados de aquisição e garantia.
- Edição e remoção de produtos existentes.
- Lista de produtos com dados formatados para fácil visualização.
- Registro de vendas com atualização automática do estoque.
- Monitoramento de garantias próximo ao vencimento com alertas.
- Sistema de login simples para autenticação e proteção das rotas.
- Interface web responsiva utilizando templates Jinja2.
- Histórico de movimentações de estoque para controle e análise.

---

## Tecnologias Utilizadas
- **Linguagem de Programação:** Python 3
- **Framework Web:** Flask
- **Template Engine:** Jinja2 (integrado ao Flask)
- **Gerenciamento de Dados:** Módulo `datetime` do Python
- **Controle de Sessão:** Flask sessões para autenticação simples

---

## Estrutura do Projeto
- `model.py`: Define as classes de domínio (Equipamento, Movimentação, EstoqueModel, Usuário) e gerenciamento dos dados em memória.
- `controller.py`: Contém a lógica de negócio, manipula os dados do modelo e prepara informações para as visualizações.
- `app.py`: Configura as rotas Flask, gerencia requisições HTTP, sessões e renderiza os templates.
- `templates/`: Contém os arquivos HTML para as páginas do sistema (login, cadastro, listagem, edição, alertas, vendas).

---

## Como Executar

**1. Instale as dependências (Flask):**
```bash
pip install flask
```

**2. Execute o arquivo principal:**
```bash
python app.py
```

**3. No navegador, acesse:**
```bash
http://127.0.0.1:5000/
```

**4. Faça login com o usuário padrão:**
---
|---------|------------|
| Usuário | admin      |
| Senha   | 1234       |
---

## Observações
- O sistema atualmente armazena os dados na memória, sem persistência em banco de dados.
- A autenticação é simples e fixa, recomendada apenas para uso em ambiente de desenvolvimento.
- Pode ser expandido para incluir banco de dados, autenticação avançada e outras funcionalidades conforme necessidade.
