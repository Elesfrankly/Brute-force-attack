# Brute-force-attack
Desafio: Simulando um Ataque de Brute Force de Senhas com Medusa e Kali Linux

# Comando Medusa:
medusa -h 0.0.0.0 -U users.txt -P passwords.txt -M ftp -f -v 4
# smbnt
medusa -h 0.0.0.0 -U users.txt -P passwords.txt -M smbnt -f
#ou
hydra -L users.txt -P passwords.txt smb://0.0.0.0

# Simulando Ataque de Brute Force com Medusa e Kali Linux

## 1. Ambiente
- Diagrama da rede Host-Only no VirtualBox (texto ou ASCII)
- IPs: Kali 192.168.56.101 / Metasploitable 192.168.56.102
- Screenshot da verificação de isolamento

## 2. Wordlists
users.txt
passwords.txt

## 3. FTP
- Comando + saída (/results/medusa_ftp.txt)
- Screenshot de validação (/images/ftp_success.png)
- Reflexão: risco de credenciais padrão

## 4. SMB Password Spraying
- Processo de enumeração de usuários
- Comando e saída do Medusa/Hydra
- Screenshot de validação

## 5. DVWA (formulário web)
- Processo de tentativa
- Fenômeno de falso positivo e análise de causa
- Sugestão de ferramenta alternativa

## 6. Medidas de Mitigação
- MFA
- Bloqueio de conta / rate limiting
- Fail2Ban
- Alteração de credenciais padrão
- Monitoramento de múltiplas falhas de login nos logs
