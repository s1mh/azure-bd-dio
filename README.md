# 🗄️ Laboratório - Configurando uma Instância de Banco de Dados na Azure

Este repositório documenta o processo de criação e configuração de uma instância de banco de dados SQL na plataforma Microsoft Azure, como parte do desafio **"Configurando uma instância de Banco de Dados na Azure"** da DIO.

---

## 🎯 Objetivos

- Praticar a configuração de uma instância de banco de dados no Azure.
- Documentar o processo técnico de forma clara e estruturada.
- Compartilhar anotações, dicas e prints úteis para estudos futuros.

---

## 📚 Tutorial Utilizado

Todo o processo foi baseado no guia oficial da Microsoft:  
🔗 [Início Rápido: criar Instância Gerenciada de SQL do Azure](https://learn.microsoft.com/pt-br/azure/azure-sql/database/single-database-create-quickstart)

---

## 📘 Etapas Realizadas

1. Acesso ao [Portal do Azure](https://portal.azure.com/)
2. Criação de grupo de recursos: `myVM_group`
3. Criação da instância SQL:
   - Servidor lógico: `desafio-bd.database.windows.net`
   - Tipo de serviço: **Uso Geral - Sem servidor (Gen5, 1 vCore)**
   - Armazenamento: 32 GB com pausa automática após 1 hora
4. Configuração de segurança e acesso:
   - Autenticação via Azure Active Directory (AAD)
   - Acesso público desabilitado
   - Nenhuma regra de firewall
5. Configuração de backups:
   - Frequência diferencial: 12 horas
   - Retenção PITR: 7 dias
   - Redundância: geográfica
6. Validação da instância no portal

---

## 🔧 Detalhes da Configuração do Banco de Dados

- **Grupo de Recursos:** myVM_group  
- **Status:** Online  
- **Localização:** Brazil South  
- **Nome do Servidor:** desafio-bd.database.windows.net  
- **Camada de Serviço:** Uso Geral (Sem servidor)  
- **vCores:** 1  
- **Armazenamento Máximo:** 32 GB  
- **Pausa Automática:** 1 hora  
- **Backups:**
  - Diferencial: a cada 12 horas  
  - PITR (Recuperação pontual): 7 dias  
  - Redundância de backup: Geográfica  
- **Acesso Público:** Desabilitado  
- **Regras de Firewall:** Nenhuma  
- **Autenticação:** Azure Active Directory (AAD)  
- **Defender para SQL:** Desabilitado  
- **Always Encrypted:** Desabilitado  
- **Replicações:** 0 réplicas

---

## 💡 Dicas Importantes

- A camada **sem servidor** é excelente para ambientes de aprendizado com custo otimizado.
- Sempre revise as políticas de backup e retenção para garantir recuperação de dados.
- O uso de autenticação AAD aumenta a segurança e integração com o ambiente corporativo.

---

## 🖼️ Capturas de Tela

As capturas das principais etapas estão disponíveis na pasta `/images`.

---

## 📎 Referências

- [Início rápido: Instância SQL do Azure](https://learn.microsoft.com/pt-br/azure/azure-sql/database/single-database-create-quickstart)  
- [Documentação do GitHub](https://docs.github.com)  
- [Guia de Markdown GitHub](https://www.markdownguide.org/basic-syntax/)

---

> *Desenvolvido como parte do desafio "Configurando uma instância de Banco de Dados na Azure" da [DIO](https://web.dio.me/).*
