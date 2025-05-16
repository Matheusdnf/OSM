# Engenharia de Requisitos

## 📌 Definição Geral

Engenharia de Requisitos é o conjunto de atividades voltadas para **descobrir, analisar, especificar e manter os requisitos** de um sistema. O termo "engenharia" é usado para destacar que essas atividades devem ser feitas de forma **organizada**, **sistemática** e com o uso de **técnicas bem definidas**, durante todo o ciclo de vida do sistema.

---

## 🧩 Tipos de Requisitos

### ✅ Requisitos de Usuário

- Escritos em **linguagem natural**, sem muitos detalhes técnicos.
- Voltados para usuários e clientes.
- Devem ser fáceis de entender.

**Exemplo:**

> O sistema deve permitir que os clientes reservem filmes pela internet.

### ⚙️ Requisitos de Sistema

- Técnicos e mais detalhados.
- Especificados pelos desenvolvedores.
- Usados como base para o desenvolvimento do sistema.

**Exemplo:**

> O sistema deve registrar as reservas em um banco de dados MySQL e garantir tempo de resposta inferior a 1 segundo para cada consulta.

---

## 🧭 Classificação dos Requisitos

### 🔹 Requisitos Funcionais

Definem as **funcionalidades** do sistema – ou seja, o que o sistema deve fazer.

**Exemplo (Sistema de Locadora):**

- Cadastrar clientes, filmes e funcionários.
- Realizar reservas e devoluções.
- Calcular multas por atraso.
- Controlar pagamentos.

### 🔸 Requisitos Não Funcionais

Definem **restrições de qualidade** e requisitos relacionados ao **desempenho**, **segurança**, **usabilidade** e outros aspectos.

**Exemplo (Sistema de Locadora):**

- Privacidade dos dados dos clientes.
- Sistema deve estar disponível 99,99% do tempo.
- Interface deve funcionar em computadores, tablets e celulares.
- Tempo de carregamento de páginas inferior a 2 segundos.

---

## 🛠️ Características dos Requisitos de Qualidade

| Categoria          | Descrição                                                    |
| ------------------ | ------------------------------------------------------------ |
| **Desempenho**     | Tempo de resposta, transações por segundo, latência          |
| **Espaço**         | Uso de disco, memória RAM, cache                             |
| **Confiabilidade** | Tempo médio entre falhas (MTBF), disponibilidade (%)         |
| **Robustez**       | Capacidade de recuperação após falhas (MTTR), perda de dados |
| **Usabilidade**    | Facilidade de uso, tempo de aprendizado para novos usuários  |
| **Portabilidade**  | Facilidade de rodar em diferentes sistemas e dispositivos    |

> ⚠️ Use **métricas objetivas** sempre que possível.  
> Exemplo incorreto: "O sistema deve ser rápido."  
> Exemplo correto: "99% das transações devem ter tempo de resposta menor que 1 segundo em qualquer intervalo de 5 minutos."

---

## 🔍 Elicitação de Requisitos

A **Elicitação de Requisitos** é a etapa inicial do projeto em que se busca entender o que o sistema precisa fazer. Envolve coleta de informações através de:

- Entrevistas com usuários e clientes.
- Observação de processos existentes.
- Questionários.
- Análise de documentos.
- Workshops ou reuniões.

![imagem_requisito](/image/requisito.png)

**Exemplo (Sistema de Locadora):**

> Atualmente tudo é feito de forma manual. Não há controle preciso de clientes nem do estoque de filmes.  
> Requisitos identificados: cadastro de clientes, controle de filmes disponíveis, geração de relatórios, sistema de reservas etc.

---

## ✅ Boas Práticas na Especificação de Requisitos

- **Precisos:** Evitar ambiguidade.
- **Completos:** Não deixar lacunas.
- **Consistentes:** Sem contradições.
- **Verificáveis:** Devem ser testáveis para garantir que foram atendidos.

---
