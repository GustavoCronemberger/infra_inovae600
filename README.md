# Projeto de Rede Local com VLANs, Roteamento e NAT

Este projeto descreve a implementação de uma rede capaz de comportar **mais de 600 dispositivos**, com conexão à internet e um **servidor de acesso restrito**.  
O objetivo foi aplicar conceitos práticos de redes de computadores, garantindo **eficiência, segurança e redundância**.

---

## Estrutura do Projeto

- **LAN (Rede Local):**  
  - Interligação entre Laboratório A e Laboratório B.  
  - Instalação de um switch em cada ambiente.

- **VLANs (Redes Locais Virtuais):**  
  - Segmentação em dois grupos: **Administrativo** e **Pesquisa**.  
  - Comunicação entre VLANs resolvida via **roteamento** em um roteador dedicado.

- **Endereçamento IP:**  
  - Necessidade de suportar mais de 600 dispositivos → abandono da Classe C.  
  - Classe B considerada, mas otimizada para evitar desperdício de endereços.  
  - Aplicação da lógica dos octetos para alocação eficiente.

- **Redundância e Resiliência:**  
  - Adição de um switch extra.  
  - Implementação do protocolo **STP (Spanning Tree Protocol)** para evitar falhas físicas e loops.

- **Segurança:**  
  - Acesso restrito ao servidor apenas para o setor **Administrativo (manager)**.  
  - Configuração de **ACL (Access Control List)** no roteador.

- **Conexão com a Internet:**  
  - Configuração de IP público.  
  - Utilização de **NAT (Network Address Translation)** para tradução entre IP público e privado.  
  - Testes realizados com sucesso.

---

## Tecnologias e Protocolos Utilizados

- **Switches** para interligação física.  
- **Roteador** para comunicação entre VLANs e acesso externo.  
- **VLANs** para segmentação lógica.  
- **STP (Spanning Tree Protocol)** para redundância.  
- **ACL (Access Control List)** para controle de acesso.  
- **NAT (Network Address Translation)** para conexão com a internet.  

---

## Resultados

- Rede funcional e escalável para **600+ dispositivos (apenas modificar a máscara de rede**.  
- Segmentação lógica eficiente entre setores.  
- Redundância implementada para maior confiabilidade.  
- Acesso seguro ao servidor administrativo.  
- Conexão estável com a internet após configuração de NAT.  

---

## Aprendizados

Este projeto demonstrou a aplicação prática de conceitos fundamentais de redes:  
- Planejamento de endereçamento IP.  
- Segmentação com VLANs.  
- Roteamento entre redes.  
- Redundância com STP.  
- Segurança com ACL.  
- Tradução de endereços com NAT.  
