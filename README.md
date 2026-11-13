# brute-force-medusa-kali
# ⚔️ Cybersecurity Lab: Ataques de Força Bruta com Medusa e Kali Linux

![Security](https://img.shields.io/badge/Focus-Offensive%20%26%20Defensive%20Security-red?style=for-the-badge)
![Environment](https://img.shields.io/badge/Lab-Kali%20Linux%20%7C%20Metasploitable%202-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

## 📖 Visão Geral do Projeto
Este repositório documenta um desafio prático de cibersegurança desenvolvido durante a formação da **DIO (Digital Innovation One)**. O objetivo foi simular e documentar cenários reais de ataques de força bruta (*Brute Force* e *Password Spraying*) utilizando a ferramenta **Medusa** no **Kali Linux** em um ambiente isolado de testes contendo alvos como o **Metasploitable 2** e a aplicação **DVWA**.

Além do aspecto ofensivo, o projeto enfatiza as **medidas de mitigação, auditoria e hardening** necessárias para proteger infraestruturas contra esse tipo de vetor de ataque.

---

## 🏗️ Arquitetura do Laboratório

* **Máquina Atacante:** Kali Linux 2026.x (IP: `192.168.56.10`)
* **Máquina Alvo:** Metasploitable 2 (IP: `192.168.56.101`)
* **Rede:** Host-Only / Exclusiva de Hospedeiro no Oracle VM VirtualBox (Garantindo o isolamento da rede física)

---

## 🚀 Cenários Práticos Testados

### 1. Força Bruta em Serviço FTP (Porta 21)
* **Objetivo:** Identificar credenciais válidas via autenticação contínua.
* **Ferramenta:** Medusa
* **Comando:**
  ```bash
  medusa -h 192.168.56.101 -U wordlists/usernames_custom.txt -P wordlists/passwords_custom.txt -M ftp -v 4
