# Laboratorio: Criando um ataque de brute force de senhas com medusa e kali linux (DIO)
Este repositório documenta a execução de um desafio prático de segurança da informação, focado em ataques de força bruta. O projeto foi desenvolvido como parte do bootcamp de Cyber Segurança da Santander - Cibersegurança 2025 - DIO.

**Autor:** Marcelo Leal
**LinkedIn:** https://www.linkedin.com/in/slmarcelo/

---

## 1. Descrição do Desafio

O objetivo deste projeto é implementar e documentar um cenário prático de ataque de força bruta utilizando **Kali Linux** e a ferramenta **Medusa**. O ambiente de teste controlado é composto por máquinas virtuais vulneráveis (como **Metasploitable 2** e **DVWA**) para simular ataques a diferentes serviços (FTP, Web e SMB) e, em seguida, propor as devidas medidas de mitigação.

## 2. Configuração do Ambiente (Laboratório)

Para a realização dos testes, foi configurado um laboratório virtual isolado, garantindo que todas as atividades de pentest ficassem contidas e seguras.

* **Software de Virtualização:** VirtualBox
* **Configuração de Rede:** "Rede Interna" (VirtualBox) para isolar as VMs do restante da rede.

### Máquinas Virtuais

| Propósito | Sistema Operacional | Endereço IP (Exemplo) |
| :--- | :--- | :--- |
| 📍 **Atacante** | Kali Linux | `192.168.56.100` |
| 🎯 **Vítima** | Metasploitable 2 | `192.168.56.103` |

### Ferramentas Utilizadas

* **Nmap:** Para reconhecimento e escaneamento de portas e serviços.
* **Medusa:** Ferramenta principal para a execução dos ataques de força bruta.
* **Enum4Linux:** Para enumeração de usuários no serviço SMB.
* **Wordlists:** Listas de senhas e usuários


## 3. Descobrir IPs e verificar a conectividade entre as maquinas

Para descobrir o ip do Kali 

ip addr

Com os seguintes comando é possivel descobrir os ips da rede para encontrar a VM Metasploitable

arp  -a

sudo nmap -sn 192.168.56.0/24
 
sudo netdiscover -r 192.168.56.0/24



