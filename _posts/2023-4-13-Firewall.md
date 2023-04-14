---
layout: post
title: Firewall
---

Dado uma rede onde a regra é que apenas o tráfego legítimo deve ser aceito, foram instalados dois firewalls para fazer a proteção na camada de transporte. O firewall n° 1 protege a DMZ (zona desmilitarizada) e a LAN (rede local), o firewall n° 2 protege somente a LAN. Dessa forma, quando necessário os servidores e recursos na DMZ podem ser acessados ​​pela Internet, mas o restante da LAN interna permanece inacessível, com isso a LAN tem camada adicional de segurança.

![_config.yml]({{ site.baseurl }}/images\posts-images\firewall\rede.png)

Sabendo que apenas o tráfego legítimo deve ser autorizado e a regra default é bloquear tudo, foram definidas para o firewall n° 1 as seguintes regras: 
* Regras de entrada: DNS, HTTP, e-mail, chat, VoIP e banco de dados da WAN para seus respectivos servidores na rede DMZ.
    * Essas regras permitem que a internet acesse os servidores e recursos na DMZ.
* Regras de saída: DNS, HTTP, e-mail, chat, VoIP e banco de dados de seus respectivos servidores na DMZ para WAN. 
    * Essas regras permitem que os servidores DMZ se comuniquem com a internet.
* Regra de saída: HTTP para a internet vindo da LAN.
    * Essa regra permite que a LAN acesse a internet

Por meio dessas regras, a internet pode acessar o DMZ para tudo o que é necessário e vice-versa. Além disso, também é possível que os clientes da LAN usem a web.

O firewall n° 1 configurado com essas regras bloqueia boa parte do tráfego malicioso, porém alguns ataques ainda acontecem, isso porque o firewall usado é limitado à camada de transporte, então certos ataques disfarçados de tráfego legítimo conseguem passar e entrar na DMZ.

![_config.yml]({{ site.baseurl }}/images\posts-images\firewall\regras_firewall1.png)

No firewall n° 2 foram definidas as seguintes regras:
* Regras de saída: DNS, e-mail, chat, VOIP e banco de dados para os servidores da DMZ.
    * Essas regras permitem que a LAN acesse os servidores e recursos na DMZ.
* Regras de entrada: e-mail, chat e VoIP da DMZ para LAN.
    * Essas regras permitem que LAN receba mensagens e-mail, chat e VoIP, vindas da DMZ.
* Regra de saída: HTTP para qualquer servidor HTTP.
    * Essa regra permite que LAN acesse a internet.

Essas regras asseguram que a LAN esteja protegida contra uma grande quantidade de vírus e ameaças existentes, isso porque a LAN tem entradas somente da DMZ, um ambiente teoricamente mais seguro.

![_config.yml]({{ site.baseurl }}/images\posts-images\firewall\regras_firewall2.png)

Essa organização de regras nos dois firewalls proporciona uma boa proteção para a rede interna, mas não a deixa imune a ataques.

![_config.yml]({{ site.baseurl }}/images\posts-images\firewall\funcionando_sem_ataques_app.png)

Ataques disfarçados de tráfego legitimo conseguem passar pelo firewall.

![_config.yml]({{ site.baseurl }}/images\posts-images\firewall\funcionando_com_ataques_app.png)

[Arquivo do simulador(Firewall.dat)]({{ site.baseurl }}/files\firewall\Firewall.dat)