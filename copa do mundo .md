# Tabela da Copa 2026

## 1. Nome

Tabela da Copa 2026

## 2. Versão

1.0

---

## 3. Escopo

### Objetivo

Disponibilizar, organizar e apresentar os resultados dos jogos da Copa do Mundo de 2026 em formato aberto, acessível e estruturado, permitindo a consulta de partidas, classificação e avanço de fases.

### Público-alvo

Pessoas com interesse por futebol.

### Limitações

* Não realiza transmissão de jogos ao vivo
* Não realiza apostas ou previsões
* Não gerencia venda de ingressos
* Não integra dados oficiais em tempo real

---

## 4. Requisitos Funcionais (RF)

**RF01 - Gestão de Grupos**
Permitir o cadastro dos grupos de A a L.

**RF02 - Gestão de Seleções**
Permitir o cadastro das 48 seleções com nome, bandeira, abreviação e grupo.
Regra: o grupo deve ser previamente cadastrado.

**RF03 - Gestão de Sedes**
Permitir o cadastro de país, cidade, estádio e capacidade.

**RF04 - Gestão de Partidas**
Permitir o cadastro de partidas com data, horário, sede, seleção mandante e visitante.
Regras:

* A sede deve ser previamente cadastrada
* As seleções devem existir no sistema

**RF05 - Tabela de Partidas**
Permitir a visualização das partidas organizadas por grupo e ordem cronológica.

**RF06 - Resultado das Partidas**
Permitir o registro de gols das seleções.
Regra: valores devem ser maiores ou iguais a zero.

**RF07 - Classificação**
Permitir a visualização da classificação por grupo.
Critérios:

* Pontos
* Número de vitórias
* Saldo de gols

**RF08 - Avanço de Fase**
Calcular automaticamente os classificados.
Regras:

* 2 primeiros de cada grupo avançam (24 seleções)
* 8 melhores terceiros colocados completam 32 seleções
* Fases seguintes em formato eliminatório (mata-mata)

---

## 5. Requisitos Não Funcionais (RNF)

* Desempenho: tempo de resposta inferior a 2 segundos
* Disponibilidade: sistema disponível 99% do tempo
* Segurança: controle de acesso e validação de dados
* Usabilidade: interface simples e intuitiva
* Acessibilidade: compatível com dispositivos móveis

---

## 6. Diagramas UML

### 6.1 Diagrama de Classe

**Seleção**

* nome
* bandeira
* abreviação

- jogar()

**Grupo**

* nome

**Sede**

* país
* cidade
* estádio
* capacidade

**Partida**

* data
* horário
* sede

---

### 6.2 Diagrama de Caso de Uso

* Cadastrar grupos
* Cadastrar seleções
* Cadastrar sedes
* Cadastrar partidas
* Registrar resultados
* Visualizar tabela
* Consultar classificação
* Calcular classificados

---

## 7. Modelo de Dados (MER)

### Entidades

**Seleção**

* abreviacao (PK)
* nome
* bandeira

**Grupo**

* id (PK)
* nome
* fase

**Sede**

* id (PK)
* país
* cidade
* estádio
* capacidade

**Partida**

* id (PK)
* data
* horário
* sede (FK)
* mandante (FK)
* visitante (FK)

---

## 8. Arquitetura

* Padrão: MVC
* Estrutura: Monolito
* Comunicação: REST (JSON)
* Camadas:

  * Apresentação
  * Regra de negócio
  * Dados

---

## 9. Plano de Testes

* Testes unitários nas regras de negócio
* Testes de integração entre API e banco de dados
* Testes de interface
* Testes de validação das regras de classificação e avanço

---

## 10. Cronograma

| Etapa | Descrição                  | Prazo         |
| ----- | -------------------------- | ------------- |
| 1     | Levantamento de requisitos | Semana 1      |
| 2     | Modelagem                  | Semana 2      |
| 3     | Desenvolvimento            | Semanas 3 a 6 |
| 4     | Testes                     | Semana 7      |
| 5     | Implantação                | Semana 8      |

---

## 11. DevOps e Implantação

* Versionamento: Git
* Backup: diário automatizado
* Ambiente:

  * Desenvolvimento: local
  * Produção: cloud ou VPS
  * Containerização: Docker

---

## 12. Segurança e LGPD

### Política de Privacidade

* Informar quais dados são coletados
* Informar como os dados serão utilizados
* Garantir transparência ao usuário

### Proteção de Dados

* Criptografia de dados sensíveis
* Controle de acesso
* Monitoramento e logs

**Ameaça = Agente + Mecanismo + Ativo**

**LGPD:** tratamento de dados de pessoa física conforme legislação vigente

---

## 13. Investimento

Fórmula:
Investimento = horas trabalhadas × valor da hora

---

## Estrutura da Competição

* 48 seleções
* 12 grupos (A a L) com 4 seleções cada

### Classificação

* 2 primeiros de cada grupo avançam (24 seleções)
* 8 melhores terceiros colocados avançam (total de 32)

### Fases Eliminatórias

Sistema mata-mata até definição do campeão

### Critérios de Desempate

* Pontos
* Saldo de gols
* Número de vitórias

---

## Requisitos Técnicos

### Desktop

* Linguagem: C# (Visual Studio 2022)
* Banco de dados: PostgreSQL
* Infraestrutura: Windows 10+, 16GB RAM, i3, 240GB

### Web

* Front-end: HTML, CSS, JavaScript, React
* Back-end: Node.js / PHP
* Banco de dados: MySQL ou MariaDB
* Hospedagem: 1 vCPU, 2GB RAM, 50GB SSD
* Domínio: Registro.br
* Segurança: Cloudflare

### Mobile

* Tecnologia: React Native
* Consumo via API
* Ambiente: Expo

---

## Observações Técnicas

CRUD:

* Create: Incluir
* Read: Consultar
* Update: Alterar
* Delete: Excluir lógico

---
