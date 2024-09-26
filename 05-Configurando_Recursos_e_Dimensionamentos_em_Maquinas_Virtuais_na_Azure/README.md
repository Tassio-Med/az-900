# 📘 Manual para Configuração e Dimensionamento de Máquinas Virtuais no Azure

Este guia abrangente foi criado para ajudá-lo a criar, configurar e ajustar suas máquinas virtuais (VMs) no Azure de maneira eficiente, garantindo que os recursos atendam adequadamente às suas necessidades de desempenho e custo.

## Iniciando sua Jornada no Azure

Primeiramente, assegure-se de possuir uma conta Azure ativa. Caso não tenha, acesse o [portal.azure.com]((https://portal.azure.com)) e registre-se gratuitamente.





 > ⚠️ **Atenção:** Verifique se você possui permissões para criar e gerenciar VMs na sua assinatura.



## 1. Criar a Máquina Virtual
- No painel, busque por "*Máquinas Virtuais*" ou clique em **Criar Recurso** para iniciar a criação de uma nova VM.
- Selecione uma assinatura e escolha um grupo de recursos existente ou crie um novo.
- Defina o nome da VM e escolha a região mais próxima dos seus usuários para obter melhor performance.
- Escolha o sistema operacional desejado e a imagem correspondente.
- Defina as credenciais de login:
  - <u>Windows</u>: Defina nome de usuário e senha.

    ![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)


  - <u>Linux</u>: Utilize chaves SSH para garantir uma conexão mais segura.

    ![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)


## 2. Tamanho da Máquina Virtual
O tamanho da VM determina a quantidade de CPU, memória e armazenamento temporário disponível. Escolha um tamanho adequado à sua carga de trabalho:

- <u>Tamanhos Gerais</u>: Adequados para aplicações comuns com uso equilibrado.
- <u>Tamanhos Otimizados para Memória</u>: Ideais para bancos de dados e aplicações que demandam muita RAM.
- <u>Tamanhos Otimizados para Computação</u>: Recomendados para cargas que exigem alto poder de processamento.

## 3. Armazenamento
Na aba de **Discos**, escolha o tipo de disco mais adequado para sua VM:

- **SSD Premium**: Recomendado para aplicações de alta performance.
- **SSD Padrão**: Adequado para cargas moderadas.
- **HDD Padrão**: Ideal para cargas que exigem menor custo e desempenho.

Você pode adicionar discos adicionais para separar dados ou backups.

## 4. Redes
Na aba de **Rede**, associe a VM a uma Rede Virtual (VNet) existente ou crie uma nova. Configure também as seguintes opções:

- **Sub-rede**: Conecte sua VM a uma sub-rede para isolar recursos.
- **Grupo de Segurança de Rede (NSG)**: Defina regras de firewall para limitar o tráfego de entrada e saída. Habilite apenas as portas necessárias (RDP para Windows ou SSH para Linux).
- **Endereço IP Público**: Atribua ou remova um IP público conforme necessário.

## 5. Escalabilidade 
### Escalabilidade Automática 🔄
Para lidar com flutuações de demanda, configure a autoescala da sua VM:

- Acesse as configurações de *Escalabilidade Automática*.
- Defina regras com base em métricas como uso de CPU, memória ou outros critérios.
- Defina limites mínimos e máximos.

>💡**Dica**: Se preferir controle manual, o Azure permite alterar o tamanho da VM após a criação. No menu **Dimensionar**, ajuste o tipo de instância, adicionando memória, CPU ou armazenamento conforme necessário.

## 6. Segurança e Monitoramento
### Segurança 🔒
- **Grupo de Segurança de Rede (NSG)**: Defina regras de firewall que protejam sua VM, bloqueando tráfego desnecessário.
- **Credenciais Fortes**: Use senhas seguras e, se possível, armazene credenciais no *Azure Key Vault*.
- **Atualizações**: Mantenha o sistema operacional e os aplicativos atualizados para evitar vulnerabilidades.

### Monitoramento 📊 
- **Monitoramento de Desempenho**: Utilize o *Azure Monitor* para rastrear o uso de CPU, memória e rede da VM.
> ⚠️ **Atenção**:  Configure alertas automáticos para notificá-lo quando a utilização dos recursos ultrapassar certos limites.
- **Logs de Diagnóstico**: Ative logs para coletar dados detalhados sobre o desempenho da VM.

## 7. Backup e Recuperação
Configurar backups regulares é essencial para garantir a recuperação dos dados em caso de falhas. No painel de **Backup**, você pode:

- Habilitar backup automático.
- Definir políticas de retenção e agendamento conforme suas necessidades.
- Criar um plano de recuperação para restaurar dados em cenários de falha.

## 8. Provisionamento da Máquina Virtual

Clique em **Criar** e aguarde enquanto o Azure provisiona sua máquina virtual.

## 9. Conectar-se à Máquina Virtual
- No menu "*Conectar*" do Portal do Azure encontre a sua opção.
  - <u>VMs Windows</u>: Utilize o *Remote Desktop (RDP)*.

    ![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)

  - <u>VMs Linux</u>: Utilize *SSH*.

    ![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)


---

### Conclusão

Parabéns!🎉 Você concluiu com sucesso a configuração de recursos e o dimensionamento de máquinas virtuais na Azure.

---

### Considerações Finais 🎓

Para um aprofundamento adicional, recomenda-se a consulta à [documentação oficial do Azure](https://learn.microsoft.com/pt-br/azure/?product=popular), bem como a utilização dos recursos educacionais disponibilizados através da plataforma Microsoft Learn.