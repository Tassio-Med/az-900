# 📘 Manual para Criar uma Máquina Virtual no Azure

Este tutorial detalhado vai te guiar na criação e configuração de uma Máquina Virtual (VM) no Azure utilizando o Portal do Azure.

---

## 📌 Passo a Passo

### Acessando o Portal do Azure

1. Acesse o [Portal do Azure](https://portal.azure.com) e faça login com suas credenciais.
2. No painel principal, digite **"Máquinas Virtuais"** na barra de pesquisa e selecione o resultado exibido.

---

### Iniciando a Criação da Máquina Virtual

1. Clique no botão **"Criar"** e escolha **"Máquina Virtual"**.
2. Isso abrirá o assistente de configuração, onde você precisará fornecer informações importantes sobre a nova VM.

---

### Configurando a VM

#### Informações Básicas
- **Assinatura**: Escolha a assinatura vinculada à sua conta do Azure.
- **Grupo de Recursos**: Crie ou selecione um grupo de recursos existente.
- **Nome da VM**: Escolha um nome descritivo para identificar facilmente a VM.
- **Localização**: Defina a região onde sua VM será hospedada (ex.: East US, West Europe).

#### Definindo Disponibilidade e Tamanho
- **Opções de Disponibilidade**: Escolha entre Alta Disponibilidade, Isolamento ou Nenhuma para melhorar a resiliência da sua máquina.
- **Imagem**: Selecione o sistema operacional que deseja utilizar (ex.: Ubuntu Server, Windows Server 2019).
- **Tamanho da VM**: Selecione o tamanho adequado para as necessidades de CPU e memória. Utilize **Ver todos os tamanhos** para explorar outras opções.

---

### Definindo Acesso e Autenticação

- **Nome do Administrador**: Defina o nome do usuário administrador da VM.
- **Autenticação**: Opte por **Senha** ou **Chave SSH**:
  - Para **Senha**, crie um nome de usuário e uma senha segura.
  - Para **Chave SSH**, insira o nome de usuário e a chave pública SSH.
- **Portas de Acesso**: Defina as portas necessárias para acessar a VM:
  - **RDP (3389)** para Windows.
  - **SSH (22)** para Linux.

---

### Configuração de Armazenamento

- **Tipo de Disco**: Selecione entre **SSD Premium**, **SSD Padrão** ou **HDD**, conforme o desempenho desejado.
- **Discos de Dados**: Caso precise, adicione discos adicionais clicando em **Criar e anexar novo disco**.

---

### Configuração de Rede

- **Rede Virtual**: Escolha uma rede virtual existente ou crie uma nova.
- **Sub-rede**: Selecione ou crie uma sub-rede para a VM.
- **IP Público**: Habilite esta opção para permitir o acesso externo à VM.
- **Grupo de Segurança de Rede (NSG)**: Defina ou crie um NSG para configurar as regras de firewall que controlam o tráfego de rede.

---

### Revisão e Criação

1. Clique em **Revisar + Criar** para revisar todas as configurações.
2. Confirme se todos os dados estão corretos.
3. Clique em **Criar** para iniciar a criação da máquina virtual. O processo pode demorar alguns minutos.

---

### Conectando-se à Máquina Virtual

#### Acessando sua VM

1. Após a implantação, vá até **Máquinas Virtuais** no menu lateral.
2. Selecione a VM criada.
3. Clique em **Conectar** e escolha o método de conexão:
   - **RDP** para VMs Windows.
   - **SSH** para VMs Linux.

#### Conexão em Windows:
- Baixe o arquivo RDP gerado e utilize-o para se conectar à VM via Remote Desktop.

[![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/pt-br/windows)

#### Conexão em Linux:
- Execute o comando SSH fornecido para acessar via terminal.

[![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)](https://www.linux.org/)

---


### 🎉 Conclusão

Parabéns! 🎊 Sua máquina virtual no Azure foi criada com sucesso.

---

### 🎓 Considerações Finais

Para um aprofundamento adicional, recomenda-se a consulta à [documentação oficial do Azure](https://learn.microsoft.com/pt-br/azure/?product=popular), bem como a utilização dos recursos educacionais disponibilizados através da plataforma Microsoft Learn.
