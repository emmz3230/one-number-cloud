---
sidebar_position: 1
slug: /
---

# Planejamento de Instâncias de Computação na

Os fatores abaixo precisam ser considerados quando estiver sendo feito o planejamento de
implantação de instâncias de cloud computing:

- A criação de uma rede privada (VPC).
  Veja: Tutorial de Redes.
- A criação de um roteador da rede pública para a rede privada.
  Veja: Tutorial Roteadores.
- Se for necessário manter o IP público (e.g. para uso em registro DNS,
  balanceamento de carga, escalonamento horizontal, failover, switchover), é
  necessário que seja reservado IP(s) flutuante(s).
  Veja: Tutorial IPs Flutuantes.
- Para criar uma conexão entre redes de uma rede dentro de um projeto com a rede
  interna da empresa ou outra rede externa ao projeto, e para melhor segurança de
  gerenciamento interno das instâncias sem expor serviços (e.g. ssh) direto nas redes
  públicas, é possível criar uma rede privada virtual através do serviço de VPN.
  Veja: Tutorial VPN Site-to-Site.
- Para expor os serviços necessários para as redes desejadas é necessário criar
  grupos de segurança com as regras de acordo com o tipo de serviço (e.g. ingress
  TCP porta 22 [SSH] CIDR1 0.0.0.0/32 = acesso ao serviço de ssh vindo de qualquer
  rede).
  Veja: Tutorial Grupos de Segurança.
- Para criar um balanceamento de carga com mais garantia de disponibilidade é
  necessário criar grupos de servidores. A criação de grupos de servidores define
  regras de afinidade e anti-afinidade.
  Veja: Tutorial Load Balancers (Balanceamento de Carga).
- Para balanceamento de carga e melhor aproveitamento de IPs públicos reservados,
  existe o serviço de balanceamento de carga (Load Balancer) que permite realizar
  balanceamento de carga para as instâncias desejadas.
  Veja: Tutorial Load Balancers (Balanceamento de Carga).
- Veja: Tutorial Load Balancers (Balanceamento de Carga).
  ● Opcionalmente, algumas modificações podem ser realizadas na inicialização da
  imagem padrão através do uso do cloud-init. Através do cloud-init é possível fazer
  alterações no nome padrão do usuário, atualização e instalação de pacotes na
  inicialização da instância, etc.

Para acesso a instância(s) de computação Linux na nuvem One Cloud é necessário:

Notação CIDR (Classless Inter-Domain Routing): Notação onde o IP de rede é seguido
por um número decimal que representa a quantidade de bits 1 contínuos da esquerda para
a direita na máscara de roteamento de subrede.

---

- A criação de um par de chaves para acesso SSH ou importação de uma chave
  existente. A(s) chave(s) criada(s) ou importada(s) ser(á)(ão) utilizadas no momento
  da criação da(s) instância(s).
- Ou através da criação de um usuário e senha no momento da criação da instância
  computacional através do uso de um script (formato YAML) [cloud-init](https://cloudinit.readthedocs.io/en/latest/).

Licenças de instâncias de computação Windows na nuvem One Cloud:
`<TODO>`
