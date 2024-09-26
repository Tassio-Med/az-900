#  📘 Manual para Construção e Gestão de Infraestrutura no Azure

Este guia passo a passo te auxiliará a desenvolver e gerenciar sua infraestrutura no Azure, com foco em organização, segurança e eficiência. Aqui serão exploradas a criação de grupos de recursos, regras de segurança e monitoramento dos serviços.



## Iniciando sua Jornada no Azure

Primeiramente, assegure-se de possuir uma conta Azure ativa. Caso não tenha, acesse o [portal.azure.com]((https://portal.azure.com)) e registre-se gratuitamente.




 > 💡 **Dica:** Utilize o  [Azure Well-Architected Framework](https://learn.microsoft.com/en-us/azure/well-architected/) para o planejamento e otimização da sua infraestrutura.



### 1. Grupo de Recursos 
O Grupo de Recursos no Azure é essencial pra gerenciar todos os componentes da sua infraestrutura, permitindo uma melhor visualização e controle de custos.

- No Portal do Azure, busque por "*Grupos de Recursos*" ou "*Resource Groups*".
- Clique em **Criar** e preencha os dados abaixo:
  - <u>Nome</u>: Escolha um nome que descreva claramente o propósito do grupo.
  - <u>Região</u>: Selecione a região mais próxima para otimizar latência e custos.
- Clique em Revisar + Criar e finalize a criação.

### 2. Rede Virtual 
A Rede Virtual (VNet) conecta os recursos internos da sua infraestrutura, permitindo comunicação segura entre diferentes serviços.

- No Portal do Azure, pesquise por "*Redes Virtuais*" ou "*Virtual Networks*".
- Clique em **Criar** e preencha os detalhes:
  - <u>Nome</u>: Defina um nome que identifique a VNet facilmente.
  - <u>Grupo de Recursos</u>: Selecione o grupo criado anteriormente.
  - <u>Região</u>: Escolha a mesma região do grupo de recursos para otimizar a latência.
  - <u>Intervalo de IPs</u>: Defina o espaço de endereços IP para a rede virtual.
  - Adicione uma sub-rede inicial e associe os recursos que precisam se comunicar.
- Finalize clicando em **Revisar + Criar.**

### 3. Regras de Segurança 
Segurança é um pilar essencial para construir uma arquitetura confiável. Definir regras de segurança adequadas é crucial para proteger seus dados.

- No Portal, pesquise por "*NSG*".
- Clique em **Criar** e defina as regras:
  - Controle o tráfego de entrada e saída com base em IPs, portas e protocolos.
  - Permita tráfego necessário, como HTTP/HTTPS, ou restrinja portas críticas.
  - Associe os NSGs à sua VNet e sub-redes para garantir que apenas tráfego autorizado seja permitido.

### 4. Máquinas Virtuais 
Com a infraestrutura básica pronta, agora é o momento de provisionar as Máquinas Virtuais (VMs).

- No Portal do Azure, pesquise por "*Máquinas Virtuais*".
- Clique em **Criar**.
- Selecione o sistema operacional e o tamanho da VM conforme as necessidades da aplicação.
- Associe a VM à sua Rede Virtual.
- Configure as credenciais de acesso e defina o NSG para gerenciar o tráfego.
- Revise as configurações e clique em Criar.

### 5. Balanceamento de Carga
Para garantir alta disponibilidade e distribuição eficiente do tráfego, você pode configurar um Balanceador de Carga no Azure.

- No Portal, busque por "*Balanceadores de Carga*".
- Clique em **Criar** e selecione o tipo de balanceador.
  - <u>Público</u>: Para balanceamento de tráfego externo.
  - <u>Interno</u>: Para balanceamento dentro da rede privada.
- Defina as regras de balanceamento e associe o balanceador às VMs.

### 6. Serviços de Banco de Dados 
Bancos de dados são essenciais para a maioria das aplicações. No Azure, você pode optar por soluções como SQL Server, MySQL ou Cosmos DB.

- No Portal do Azure, busque por "*Banco de Dados*".
- Escolha o tipo de banco de dados (SQL, MySQL, etc.).
- Defina o nome, credenciais de administrador e as configurações de escalabilidade.
- Associe o banco de dados à sua Rede Virtual para garantir segurança na comunicação.

### 7. Monitoramento e Alertas
Manter o monitoramento constante da sua infraestrutura permite reagir rapidamente em caso de problemas.

- No painel, pesquise por "*Monitor*" e configure Logs de Diagnóstico para cada recurso.
- Defina Alertas para monitorar o uso de CPU, memória, rede e disco.
- Considere integrar com o *Azure Log Analytics* para ter uma visão consolidada dos logs e eventos críticos.

### 8. Backups e Redundância
A proteção dos dados é fundamental. Configure backups automáticos e redundância geográfica para garantir a disponibilidade dos seus serviços.

- Ative o **Backup do Azure** para suas VMs e bancos de dados.
- Defina políticas de backup e retenção adequadas à sua aplicação.
- Para dados críticos, habilite Replicação Geográfica, garantindo a segurança em caso de falhas regionais.

### 9. Revisão e Otimização 
Manter sua infraestrutura eficiente requer revisões periódicas. Identifique recursos subutilizados ou configurados incorretamente.

- Utilize o **Azure Cost Management** para monitorar e otimizar os custos.
- Automatize tarefas repetitivas com Azure Automation ou Runbooks.
- Revise as regras de segurança e permissões regularmente para garantir conformidade com as melhores práticas.

---

### Conclusão

Parabéns!🎉 Você concluiu com sucesso a construção e o gerenciamento de uma infraestrutura no Azure.

---

### Considerações Finais 🎓

Para um aprofundamento adicional, recomenda-se a consulta à [documentação oficial do Azure](https://learn.microsoft.com/pt-br/azure/?product=popular), bem como a utilização dos recursos educacionais disponibilizados através da plataforma Microsoft Learn.
