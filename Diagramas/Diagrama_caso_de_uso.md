# 📘 Documentos Textuais de Especificação de Requisitos

## 📌 O que são?

Casos de uso são documentos textuais que descrevem, de forma detalhada, **como um ator interage com o sistema** para atingir um determinado objetivo. O **ator** é sempre uma entidade **externa ao sistema**, como um usuário, outro sistema ou dispositivo.

Cada caso de uso descreve:

- **Um objetivo específico** do ator.
- **Passos realizados** para alcançar esse objetivo.
- **Situações alternativas ou de erro** (extensões).

---

## 🧩 Estrutura de um Caso de Uso

Todo caso de uso deve conter:

### 🔹 Nome

- Deve iniciar com **um verbo no infinitivo**, indicando claramente a ação principal.
  - Exemplo: `Transferir Valores entre Contas`

### 🔹 Ator Principal

- Quem inicia a interação com o sistema.
  - Exemplo: `Cliente do Banco`

### 🔹 Fluxo Normal (ou “Fluxo Principal” ou “Fluxo Feliz”)

- Lista numerada com os **passos principais**, que ocorrem **sem erros** até a conclusão da operação.

### 🔹 Extensões (ou Fluxos Alternativos)

- Descrevem **variações** do fluxo normal, como:
  - Tratamento de erros.
  - Regras de negócio.
  - Alternativas de execução.

---

## ✅ Exemplo de Caso de Uso

### 📄 Nome: Transferir Valores entre Contas

**Ator:** Cliente do Banco

#### ✔️ Fluxo Normal:

1. Cliente autentica-se no sistema
2. Cliente informa agência e conta de destino
3. Cliente informa valor que deseja transferir
4. Cliente informa a data da transferência
5. Sistema efetua a transferência
6. Sistema pergunta se o cliente deseja fazer uma nova transferência

#### 🔄 Extensões:

- **2a** – Se agência ou conta forem inválidas, solicitar novos dados
- **3a** – Se valor for maior que o saldo, solicitar novo valor
- **4a** – Data deve ser a atual ou até um ano à frente
- **5a** – Se a data for a atual, transferir imediatamente
- **5b** – Se a data for futura, agendar a transferência

---

## ✍️ Boas Práticas para Escrever Casos de Uso

- Use **linguagem simples e direta**, como se explicasse para uma criança.
- Escreva ações com o **ator como sujeito** seguido de um **verbo de ação**.

  ✅ Exemplo:  
  `Cliente insere o cartão no caixa eletrônico.`  
  `Sistema valida o cartão inserido.`

- Se a ação for do sistema, inicie com:  
  `O sistema [verbo]...`

- Evite comandos técnicos como `se`, `enquanto`, `repita`.

  ✅ Em vez de:  
  `Enquanto cliente não encontra o produto, continue pesquisando.`  
  ✅ Use:  
  `O cliente pesquisa o catálogo até encontrar o produto desejado.`

- Não descreva **interface, botões, cores ou tecnologias**.

  🚫 Errado:  
  `Cliente pressiona o botão verde para confirmar a transferência.`  
  ✅ Correto:  
  `Cliente confirma a transferência.`

- Mantenha o **fluxo principal com no máximo 9 passos**.  
  Se necessário, **divida ou agrupe ações semelhantes**.

  ✅ Exemplo de agrupamento:  
  `Usuário informa login e senha` (em vez de dois passos separados).

- Evite criar casos de uso puramente com operações **CRUD** separadas.

  🚫 Errado:  
  `Cadastrar Professor`, `Atualizar Professor`, `Excluir Professor`  
  ✅ Correto:  
  `Gerenciar Professor` (incluindo as quatro operações)

- **Padronize o vocabulário** entre todos os casos de uso.  
  Use sempre os mesmos termos (ex: escolha entre "Cliente" ou "Usuário").

- Crie e mantenha um **glossário de termos** do projeto para garantir clareza entre a equipe e os usuários.

  💡 **Recomendação (The Pragmatic Programmer):**

  > "É muito difícil ter sucesso em um projeto onde usuários e desenvolvedores usam nomes diferentes para as mesmas coisas — ou pior, o mesmo nome para coisas diferentes."

---

## ✅ Resumo Final

| Elemento         | Deve conter                             |
| ---------------- | --------------------------------------- |
| **Nome**         | Verbo no infinitivo                     |
| **Ator**         | Quem inicia a ação (externo ao sistema) |
| **Fluxo Normal** | Lista de passos bem-sucedidos           |
| **Extensões**    | Variações, erros, exceções              |
| **Linguagem**    | Clara, simples, sem termos técnicos     |
| **Estilo**       | Foco no "o quê", não no "como"          |
| **Consistência** | Vocabulário padronizado                 |
| **Agrupamento**  | Evite excesso de casos de uso simples   |

# Diagrama de Caso De Uso

Ele representa os atores de um sistema (como pequenos bonecos) e os casos de uso (como elipses). Mostram-se também dois tipos de relacionamento: (1) ligando ator com caso de uso, que indicam que um ator participa de um determinado caso de uso; (2) ligando dois casos de uso, que indicam que um caso de uso inclui ou estende outro caso de uso.

✅ **---Include--->**
O relacionamento _include_ indica que um caso de uso sempre inclui outro caso de uso como parte de sua execução.

- O caso de uso incluído é chamado automaticamente sempre que o principal é executado.

- Funcionalidade obrigatória que é sempre executada como parte de outro caso de uso.

**Exemplo**: No sistema de compras online, o caso de uso "Finalizar Pedido" pode incluir o caso de uso "Calcular Frete", pois esse cálculo sempre ocorre durante a finalização.

✅ **---Extend--->**
O relacionamento _extend_ indica que um caso de uso pode estender outro, ou seja, adicionar comportamento opcional, que ocorre apenas em certas condições.

- Representa uma funcionalidade opcional, que só é executada sob certas condições.

- Caso de uso estendido só é ativado se a condição for atendida.

**Exemplo**: O caso de uso "Finalizar Pedido" pode estender o caso de uso "Aplicar Cupom de Desconto", pois essa ação só acontece se o usuário inserir um cupom.

![imagem_diagrama](/image/diagrama.png)

Dois atores: Cliente e Gerente.

Cliente participa dos seguintes casos de uso: Sacar Dinheiro e Transferir Valores.

Gerente é o ator principal do caso de uso Abrir Conta
O diagrama também deixa explícito que Transferir Valores inclui o caso de uso Autenticar Cliente.
