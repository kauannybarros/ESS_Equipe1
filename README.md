# Sistema de Reserva de Salas e Equipamentos - Equipe 1

Este repositório contém o monorepo do projeto desenvolvido para a disciplina de **Engenharia de Software e Sistemas (ESS)**, lecionada pelo professor **Breno Miranda** no período **2026.1** no **CIn - UFPE**.

## 📌 O Projeto
A aplicação tem como objetivo principal gerenciar a reserva de salas e computadores de laboratório, além de permitir solicitações de manutenção. [cite_start]O sistema atende a diferentes perfis de usuários (Discentes, Docentes e Administradores) com fluxos de aprovação integrados[cite: 1, 14, 22].

---

## 🛠 Stack Tecnológica

O projeto foi construído utilizando tecnologias modernas para garantir escalabilidade e simplicidade:

* **Frontend:** React, JavaScript e CSS puro.
* **Backend:** FastAPI (Python).
* **Banco de Dados:** (Definir conforme implementação, ex: PostgreSQL/SQLite).

---

## 👥 Perfis de Usuário e Funcionalidades

### 🎓 Usuários (Discentes e Docentes)
* [cite_start]**Cadastro e Perfil:** Registro obrigatório com CPF, nome, senha e vínculo[cite: 41, 55].
    * [cite_start]**Discentes:** Devem informar Curso e Matrícula[cite: 51].
    * [cite_start]**Docentes:** Devem informar o SIAPE[cite: 51].
* [cite_start]**Reservas:** Efetuar, editar, cancelar e visualizar o histórico de reservas de salas ou computadores[cite: 15, 124, 159].
* [cite_start]**Solicitações (Docentes):** Criar solicitações de manutenção para salas específicas[cite: 63, 66].
* [cite_start]**Avaliações:** Realizar reviews de salas e equipamentos[cite: 29, 32].

### 🔑 Administradores
* [cite_start]**Gestão de Salas:** Cadastro (Nome, Capacidade, Descrição e total de Computadores), edição e remoção de salas[cite: 17, 96, 245].
* [cite_start]**Moderação:** Confirmar ou negar reservas e solicitações de manutenção[cite: 187, 212].
* [cite_start]**Controle de Manutenção:** Definir períodos de manutenção, o que bloqueia automaticamente novas reservas e nega pendências existentes[cite: 235, 241, 243].

---

## 📋 Regras de Negócio Importantes

* [cite_start]**Prioridade:** Reservas feitas por professores têm prioridade visual na fila de aprovação do administrador[cite: 154, 193].
* [cite_start]**Restrição de Horário:** Um usuário só pode possuir **uma única reserva** por data/horário[cite: 74, 95].
* [cite_start]**Edição/Cancelamento:** Só é permitido editar ou cancelar reservas e solicitações que ainda estejam com o status **Pendente**[cite: 71, 91, 145].
* **Estados da Reserva:**
    1.  [cite_start]**Pendente:** Aguardando admin[cite: 84].
    2.  [cite_start]**Confirmada:** Aprovada pelo admin[cite: 85].
    3.  [cite_start]**Negada:** Rejeitada pelo admin[cite: 86].
    4.  [cite_start]**Concluída:** Quando o horário da reserva confirmada já passou[cite: 87].
* [cite_start]**Segurança:** O login é realizado via CPF e Senha (máximo 128 caracteres)[cite: 55, 57]. [cite_start]Não há recuperação de senha ou foto de perfil[cite: 53, 55].

---

## 🗂️ Estrutura de Dados (Principais Objetos)

| Objeto | Atributos Principais |
| :--- | :--- |
| **Sala** | [cite_start]Nome, Capacidade, Descrição, Qtd Computadores, Status Manutenção [cite: 245] |
| **Usuário** | [cite_start]Nome, CPF, Senha, Tipo (Docente/Discente), SIAPE/Matrícula, Curso [cite: 252] |
| **Reserva de Sala** | [cite_start]Usuário, Sala, Horário Início, Horário Fim, Status [cite: 262] |
| **Reserva de Computador** | [cite_start]Usuário, Sala, Qtd Computadores, Horário Início/Fim, Status [cite: 267] |
| **Solicitação Manutenção**| [cite_start]Usuário, Sala, Descrição, Data Início/Fim [cite: 272] |

---

## 🚀 Como Executar (Em breve)

*(Espaço reservado para instruções de `npm install`, `pip install -r requirements.txt`, etc)*

---
**Equipe 1 - ESS 2026.1**
