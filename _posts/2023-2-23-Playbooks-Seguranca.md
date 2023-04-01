---
layout: post
title: Playbooks de segurança
---

Um playbook é um manual usado para responder a eventos de segurança e ameaças.
Um manual de segurança cibernética adequado assume que haverá perda de dados e garante que a empresa sobreviverá, independentemente de como os dados são perdidos. 

## Playbooks para alguns ataques

### Playbook malware

**Identificação**

Após observar a presença de malware no sistema deve-se:
1. Isolar o ambiente infectado, preservando seu estado atual para investigar o tipo de ataque.
2. Buscar identificar o tipo de malware que está atacando para determinar como se defender.
3. Determinar os ativos afetados pelo ataque.
4. Utilizar os logs para determinar como ocorreu a invasão do sistema.

**Contenção**

Com as informações coletadas na identificação:
1. Fechar as lacunas abertas pelo ataque cibernético. Exemplos: alterações no firewall, regras de bloqueio de email, etc.
2. Implementar regra, procedimento e segmentação de rede temporários para conter o malware.

**Erradicação**

Preservar todos os dados, equipamentos e/ou sistemas relevantes e substituir ou reconstruir os sistemas de acordo.

**Recuperação**

1. Restaurar os sistemas a partir de backup limpo.
2. Corrigir as vulnerabilidades detectadas na investigação.
3. Redefinir senhas ou outras informações sensíveis
4. Monitorar atividades maliciosas relacionadas a esse ataque por um período.

### Playbook ataque DDos

**Identificação**

Para identificar um ataque DDos verificar:
1. O aumento do volume de tráfego criptografado. 
2. O aumento consistente na utilização da largura de banda acima de 80%.
3. O aumento anormal nas falhas de pesquisa de DNS. 
4. A origem do aumento da utilização da largura de banda.
5. Verifique os logs do servidor alvo do DDoS.

**Contenção**

Com as informações coletadas na identificação:
1. Bloquear os endereços IP identificados como enviando tráfego de aceleração.
2. Permitir ou priorizar apenas IPs na lista de permissões.
3. Alternar para link alternativo. 
4. Se o gargalo for um recurso específico de um aplicativo, desative o recurso temporariamente. 

**Erradicação**

1. Se possível, encaminhar o tráfego por meio de um serviço ou produto de depuração de tráfego via DNS ou alterações de roteamento.
2. Configurar filtros de saída para bloquear o tráfego que seus sistemas podem enviar em resposta ao tráfego DDoS, para evitar a adição de pacotes desnecessários à rede.

**Recuperação**

1. Avaliar o fim da situação DDoS.
2. Certifique-se de que os serviços afetados estejam acessíveis novamente.
3. Certifique-se de que o desempenho da infraestrutura esteja de volta ao seu desempenho normal.
4. Reverter as medidas de mitigação.
5. Volte o tráfego para a rede original.
6. Reinicie os serviços interrompidos.

### Playbook phishing

**Identificação**

Ao ser detectado o incidente: 
1. Deve-se obter todos os e-mails ou URLs de phishing.
2. Deve-se investigar se essas informações coletadas são:
    1. E-mails sinalizados por vários filtros.
    2. E-mails não retornáveis e não entregáveis.
    3. Notificação por terceiros de e-mails suspeitos.
    4. E-mails vinculados a URLs internos e externos.
    5. Notificação do provedor e agências especializadas sobre e-mails.
    6. Atividade suspeita no site da organização.
3. Use os meios disponíveis para coletar informações e analisar para:
    1. Identifique os dados que foram comprometidos.
    2. Usuários, clientes, público susceptível de ficar exposto.
    3. Quem pode ter lançado o ataque.
    4. Quem têm conhecimento desse ataque.
    5. Pior caso de impacto no sistema.

**Contenção**

1. Isolar o sistema, incluindo usuário ou servidores afetados pelo ataque.
2. Informar todos os usuários sobre os problemas e ações imediatas que precisam ser tomadas por eles para conter o ataque.

**Erradicação**

1. Usar técnicas de remoção de malwares para livrar o sistema do malware instalado durante o ataque.
2. Instalar o patch, atualizar as regras e modificar o filtro de conteúdo para evitar novos problemas.

**Recuperação**

1. Limpe e volte o sistema ao seu estado normal.
2. Prepare um comunicado detalhado e divulgue-o amplamente para evitar futuros ataques desse tipo.
3. Documente o problema e as ações tomadas, incluindo alterações de política, modificações de processo e alterações de configuração.
