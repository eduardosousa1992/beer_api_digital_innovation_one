# 🍺 BeerStock API Tests

Projeto de testes automatizados para a API de gerenciamento de estoque de cervejas (Spring Boot).

## 📌 Objetivo
Validar as principais funcionalidades da API, garantindo a integridade dos dados e o fluxo de negócio (End-to-End).

## 🚀 Como executar os testes

### ▶️ Via Postman (Collection Runner)

1. **Importar os arquivos:**
   - `BeerStock_Collection.json`
   - `BeerStock_Environment.json`

2. **Abrir o Runner:**
   - Selecione a Collection: `BeerStock API`
   - Selecione o Environment: `BeerStock_Env`

3. **Configurar Massa de Dados:**
   - Clique em **Select File** e anexe o arquivo `cervejas.json`.
   - Clique em **Preview** para garantir que os dados estão sendo lidos corretamente.

4. **Configuração de Execução:**
   - Defina o **Delay** para **500ms** (essencial para garantir a persistência no banco de dados entre as iterações).

5. **Clicar em Run.**

---

## 🛠️ Tecnologias Utilizadas
- **Postman**: Automação de requisições.
- **JavaScript**: Scripts de validação e persistência dinâmica.
- **JSON**: Estrutura da massa de dados.

## ✅ Boas Práticas Implementadas
- **Data Driven Testing**: Testes baseados em massa de dados externa.
- **Request Chaining**: O ID gerado na criação é passado automaticamente para consulta e exclusão.
- **Validação de Contrato**: Verificação de status codes e estrutura de resposta.

---

## 🛠️ Solução de Problemas
- **Erro 400/415:** Certifique-se de que o arquivo JSON não contém aspas extras embutidas nos valores de texto.
- **Erro 404 no DELETE:** Se o teste de exclusão falhar, aumente o `Delay` no Runner.
