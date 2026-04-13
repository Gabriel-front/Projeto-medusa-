🔐 Relatório de Laboratório de Cibersegurança – Ataques de Força Bruta
📌 Visão Geral

Este projeto teve como objetivo a criação de um ambiente controlado para simulação de ataques de força bruta, com foco na exploração de autenticações fracas em serviços de rede e aplicações web.

O laboratório foi estruturado utilizando máquinas virtuais isoladas, permitindo a execução segura de testes ofensivos sem impacto em ambientes reais.

🖥️ Ambiente Utilizado
Virtualização: VirtualBox
Máquina atacante: Kali Linux
Máquina alvo: Metasploitable2
Rede: Host-Only (isolada)

⚙️ Configuração do Ambiente
Foram configuradas duas máquinas virtuais:

Kali Linux: utilizada para execução de ferramentas de ataque
Metasploitable2: ambiente vulnerável para testes

Ambas foram conectadas em rede Host-Only, garantindo comunicação interna sem acesso externo.

A máquina Metasploitable2 exigiu ativação manual da interface de rede para obtenção de IP válido e comunicação com o atacante.

🔄 Snapshots

Foram criados snapshots após a configuração inicial das máquinas.

Essa prática permitiu restaurar rapidamente o ambiente em caso de falhas ou após execuções de ataques, garantindo repetibilidade e segurança nos testes.

🎯 Objetivo do Projeto
Simular ataques de força bruta em diferentes serviços
Explorar falhas de autenticação
Testar combinações de usuários e senhas
Compreender técnicas reais utilizadas em pentests
🔐 Metodologia de Ataque

O projeto foi dividido em etapas práticas:

📍 1. Acesso à Máquina Vulnerável
Identificação do IP da Metasploitable2
Testes de conectividade entre as máquinas
📍 2. Criação de Wordlists
Desenvolvimento de listas personalizadas de usuários e senhas
Uso de padrões comuns (ex: admin, user, password, 123456)
📍 3. Simulação de Ataques de Força Bruta

Foram realizados ataques em diferentes cenários:

🔹 Formulários Web
Testes de autenticação em páginas web vulneráveis
Validação de credenciais fracas
🔹 Serviços de Rede (SMB)
Enumeração de usuários via SMB
Testes de acesso com credenciais comuns
📍 4. Uso da Ferramenta Medusa

A ferramenta Medusa foi utilizada como principal recurso para execução de ataques de força bruta.

Principais características exploradas:

Ataques paralelos (alta performance)
Testes automatizados de múltiplas combinações
Suporte a diversos serviços (SSH, FTP, SMB, HTTP, etc.)

Exemplo de uso:

medusa -h <IP_ALVO> -u <usuario> -P <wordlist> -M smbnt

Ou com múltiplos usuários:

medusa -h <IP_ALVO> -U usuarios.txt -P senhas.txt -M smbnt
📍 5. Ataque em Cadeia

Foi realizado um cenário mais avançado envolvendo:

Enumeração de usuários via SMB
Aplicação de password spraying
Tentativas de login com credenciais coletadas
📍 6. Teste de Acesso

Após encontrar credenciais válidas:

Acesso via smbclient
Validação do comprometimento do serviço
🛠️ Ferramentas Utilizadas
Medusa
Nmap
smbclient
Metasploit Framework
Netcat
⚠️ Considerações de Segurança

Todos os testes foram realizados em ambiente isolado e controlado.

As vulnerabilidades exploradas pertencem ao sistema Metasploitable2, desenvolvido especificamente para fins educacionais.

📚 Conclusão

O projeto demonstrou, na prática, como ataques de força bruta podem comprometer sistemas com autenticação fraca.

O uso do Medusa evidenciou a eficiência de ferramentas automatizadas na exploração de credenciais, especialmente quando combinadas com boas estratégias de wordlists e enumeração.

Além disso, o laboratório reforçou a importância de:

Políticas fortes de senha
Bloqueio após tentativas de login
Monitoramento de acessos


projeto desenvolvido pela DIO.
meus sinceros agradecimentos!!
Este relatorio foi ultilizado com o auxilio do chat gpt.
