# 📋 Desafio: Criando e Configurando uma Máquina Virtual Windows no Microsoft Azure

Este documento apresenta um guia passo a passo para criar e configurar uma máquina virtual (VM) Windows simples no Microsoft Azure, utilizando uma conta gratuita. 

O passo a passo também inclui a criação de conta e repositório no GitHub e criação de conta no Azure.

O objetivo é praticar a criação e documentação de processos técnicos, servindo como material de apoio para estudos e futuras implementações. 

As etapas são destinadas exclusivamente a fins educacionais e não para ambientes de produção.

> _Este material é voltado para estudantes, iniciantes e profissionais em formação na área de computação em nuvem._
---

## 🎯 Objetivos do Desafio

Ao concluir este Passo a Passo, você aplicará conceitos de computação em nuvem em um ambiente prático no Azure.
- Documentar processos técnicos de forma clara, estruturada e reproduzível.
- Criar uma conta e um repositório no GitHub e configurar o repositório
- Criar uma conta e uma Máquina Virtual Windows no Azure.

---

## 🚀 Pré-requisitos

- Um computador com acesso à internet e um navegador moderno (Edge, Chrome, Firefox, etc.).
- Uma conta de e-mail válida para criar contas no GitHub e Azure.
- Cartão de crédito/débito para verificação da conta Azure (não será cobrado para serviços gratuitos).
  - Dica: utilize um Cartão de Crédito Virtual e Temporário para não ter nenhuma cobrança surpresa se esquecer de excluir os serviços após os estudos.
  - Lembre-se: **Fique atento** aos serviços utilizados para que não haja cobranças imprevistas.
---

## 🧩 Sumário

1. [Criando uma Conta e um Repositório no GitHub](#criando-uma-conta-e-um-repositório-no-github)
2. [Criando uma Conta no Azure](#criando-uma-conta-no-azure)
3. [Criando uma Máquina Virtual no Azure](#criando-uma-máquina-virtual-no-azure)

---

## 🛠️ Criando uma Conta e um Repositório no GitHub

O GitHub é uma plataforma online para controle de versão e hospedagem de código. Ele serve para armazenar, compartilhar e gerenciar projetos de desenvolvimento de software, principalmente utilizando o sistema de controle de versões Git. É uma ferramenta essencial para desenvolvedores e equipes que buscam colaborar em projetos, acompanhar mudanças, e manter um histórico detalhado de versões. 


### Passo a Passo

1. **Acesse o site do GitHub**:
   - Vá para [github.com](https://github.com).
   - Clique em **Sign up** (no canto superior direito).

2. **Crie uma conta**:
   - Insira seu e-mail, crie uma senha e escolha um nome de usuário.
   - Siga as instruções para verificar seu e-mail.
   - Escolha o plano gratuito (Free Plan).

3. **Crie um repositório**:
   - Após fazer login, clique no botão **+** (canto superior direito) e selecione **New repository**.
   - Em **Repository name**, dê um nome ao repositório, por exemplo: `desafio-azure-vm`.
   - Escolha a visibilidade **Public** (ou Private, se preferir).
   - Em **Initialize this repository with**, marque a opção **Add a README file** para criar um README inicial.
     - Definição: O arquivo README.md no GitHub é fundamental para apresentar e documentar um projeto. Ele serve como uma introdução rápida, explicando o propósito do projeto, como utilizá-lo e onde obter ajuda. É como um manual para quem está interessado em contribuir ou usar o código.
   - No final da página, clique em **Create repository**.

4. **Edite o arquivo README.md**:
   - Após o repositório criado, surgirá uma nova tela com os arquivos do Repositório, que no nosso caso conterá somente o arquivo `README.md`.
   - Clique na figura do **Lápis** mais à direita do nome do arquivo para que o Editor seja aberto.
   - Faça alterações no arquivo.
   - Clique em **Commit changes ...** no canto superior direito para salvar.
   - Digite uma mensagem/texto resumida comentando sobre a alteração efetuada.
   - Clique em **Commit changes** 

### Dicas
- Use Markdown para formatar o README (ex.: `#` para títulos, `##` para subtítulos, `-` para listas).
- Mantenha o repositório organizado com commits claros, como "Adiciona README com tutorial Azure".
- Consulte a [documentação do GitHub](https://docs.github.com/en/get-started) para aprender mais sobre Markdown e repositórios.
- A DIO possui a [Formação Github Certification](https://web.dio.me/track/formacao-github-certification) focando em habilidades essenciais como controle de versão, colaboração e administração no ecossistema Git e GitHub. 
---

## 🌐 Criando uma Conta no Azure

O Microsoft Azure oferece uma conta gratuita com US$200 em créditos por 30 dias e acesso a serviços gratuitos, como VMs básicas, por 12 meses.

### Passo a Passo

1. **Acesse o site do Azure**:
   - Vá para [azure.microsoft.com/free](https://azure.microsoft.com/free).
   - Clique em **Start free**.

2. **Faça login ou crie uma conta Microsoft**:
   - Use um e-mail existente ou crie uma nova conta Microsoft.
   - Preencha as informações solicitadas (nome, telefone, etc.).

3. **Verifique sua identidade**:
   - Insira um número de telefone para receber um código de verificação.
   - Forneça um cartão de crédito/débito para validação (não será cobrado, a menos que você ative serviços pagos).

4. **Aceite os termos**:
   - Revise e aceite o contrato de assinatura e a política de privacidade.
   - Clique em **Sign up** para concluir.

5. **Acesse o portal do Azure**:
   - Após a criação, vá para [portal.azure.com](https://portal.azure.com) e faça login.
   - Você verá o painel inicial do Azure.

### Dicas
- Monitore os créditos no painel do Azure para evitar exceder o limite gratuito.
- Use a [calculadora de preços do Azure](https://azure.microsoft.com/pricing/calculator/) para estimar custos de serviços fora da camada gratuita.
- Desative ou exclua recursos após o uso para evitar cobranças acidentais.
- A DIO possui o curso [Introdução a nuvem com Azure](https://web.dio.me/course/introducao-a-nuvem-com-azure/learning/4c68228b-28fe-4d69-84b8-139ee9884502) onde possui uma aula a respeito.
---

## 🖥️ Criando uma Máquina Virtual no Azure

Nesta seção, você criará uma máquina virtual Windows simples usando o Portal do Azure. A configuração será básica, utilizando a camada gratuita e a região **East US** (Leste dos EUA), que geralmente oferece boa disponibilidade.

### Passo a Passo

1. **Acesse o Portal do Azure**:
   - Faça login em [portal.azure.com](https://portal.azure.com).

2. **Navegue até Máquinas Virtuais**:
   - Na barra de pesquisa superior, digite **Máquinas virtuais**.
   - Clique em **Máquinas virtuais** nos resultados.
   - Na página que abrir, clique em **Criar** > **Máquina virtual do Azure**.

3. **Configure os Detalhes Básicos**:
   - **Assinatura**: Selecione sua assinatura gratuita (ex.: Free Trial).
   - **Grupo de recursos**: Clique em **Criar novo**, nomeie como `myResourceGroup` e clique em **OK**.
   - **Nome da máquina virtual**: Insira `myWindowsVM`.
   - **Região**: Escolha **(US) East US**.
   - **Opções de disponibilidade**: Selecione **Nenhuma opção de redundância de infraestrutura necessária** (para manter simples).
   - **Imagem**: Escolha **Windows Server 2022 Datacenter: Azure Edition - x64 Gen2** (disponível na camada gratuita).
   - **Tamanho**: Clique em **Ver todos os tamanhos** e selecione **B1s** (1 vCPU, 1 GiB de RAM, elegível para camada gratuita).
   - **Conta de administrador**:
     - **Nome de usuário**: Insira `azureuser`.
     - **Senha**: Crie uma senha com pelo menos 12 caracteres, incluindo letras maiúsculas, minúsculas, números e símbolos (ex.: `Azure@12345678`).
     - Confirme a senha.
   - **Regras de porta de entrada pública**: Selecione **Permitir portas selecionadas** e escolha **RDP (3389)** para acesso remoto.
   - Clique em **Avançar: Discos**.

4. **Configure os Discos**:
   - **Tipo de disco do SO**: Selecione **SSD Standard** (econômico).
   - Mantenha as opções padrão para discos de dados (nenhum adicional).
   - Clique em **Avançar: Rede**.

5. **Configure a Rede**:
   - **Rede virtual**: Aceite o padrão `(new) myWindowsVM-vnet`.
   - **Sub-rede**: Aceite o padrão `(new) default`.
   - **IP público**: Aceite o padrão `(new) myWindowsVM-ip`.
   - **Grupo de segurança de rede**: Selecione **Básico**.
   - **Portas de entrada pública**: Confirme que **RDP (3389)** está selecionado.
   - Clique em **Avançar: Gerenciamento**.

6. **Configure o Gerenciamento**:
   - **Monitoramento**: Desative **Diagnósticos de inicialização** para economizar recursos.
   - **Desligamento automático**: Opcional, mas você pode ativar para desligar a VM automaticamente (ex.: 22:00).
   - Clique em **Avançar: Avançado** e, em seguida, **Avançar: Marcas** (pule essas seções mantendo os padrões).

7. **Revise e Crie**:
   - Clique em **Revisar + Criar**.
   - O Azure validará as configurações. Se tudo estiver correto, clique em **Criar**.
   - A implantação levará alguns minutos. Quando concluída, clique em **Ir para o recurso**.

8. **Conecte-se à VM**:
   - Na página da VM, clique em **Conectar** > **RDP**.
   - Clique em **Baixar arquivo RDP**.
   - Abra o arquivo RDP em seu computador e clique em **Conectar**.
   - Na janela de Segurança do Windows, selecione **Mais opções** > **Usar uma conta diferente**.
   - Insira o nome de usuário como `localhost\azureuser` e a senha definida (ex.: `Azure@12345678`).
   - Ignore qualquer aviso de certificado e clique em **Sim** para conectar.
   - Você verá a área de trabalho do Windows Server.

9. **Teste a VM (Opcional)**:
   - Para verificar a funcionalidade, instale o servidor web IIS:
     - Abra o PowerShell na VM (clique em Iniciar, digite `PowerShell` e execute como administrador).
     - Execute o comando:
       ```powershell
       Install-WindowsFeature -name Web-Server -IncludeManagementTools
       ```
     - Volte ao Portal do Azure, abra as **Regras de porta de entrada** na seção **Rede** da VM e adicione a porta **HTTP (80)**.
     - Copie o **IP público** da VM (na aba **Visão geral**).
     - Abra um navegador e cole o IP. Você verá a página de boas-vindas do IIS.

10. **Exclua Recursos**:
    - Para evitar custos, exclua a VM e o grupo de recursos após o uso:
      - No Portal do Azure, vá para **Grupos de recursos**.
      - Selecione `myResourceGroup`.
      - Clique em **Excluir grupo de recursos**, digite o nome do grupo para confirmar e clique em **Excluir**.

### Dicas
- A DIO possui o curso [Introdução a nuvem com Azure](https://web.dio.me/course/introducao-a-nuvem-com-azure/learning/4c68228b-28fe-4d69-84b8-139ee9884502) onde possui uma aula a respeito.

### 📌 Resumo
- Você criou uma VM Windows Server 2022 com a instância **B1s** na região **East US**, configurou acesso remoto via RDP e, opcionalmente, testou um servidor web IIS.
- O grupo de recursos `myResourceGroup` organizou todos os recursos criados.
- A exclusão do grupo de recursos garantiu que não haverá custos adicionais.

### ✅ Anotações
- A instância **B1s** é elegível para a camada gratuita (750 horas/mês por 12 meses, sujeito a limites).
- O Windows Server 2022 foi escolhido por ser amplamente suportado e estável para testes.
- O protocolo RDP requer a porta 3389 aberta, mas mantenha apenas as portas necessárias para segurança.

### 💡 Dicas sobre o Uso do Azure
- **Gerencie Custos**: Sempre verifique o [Cost Management](https://portal.azure.com/#blade/Microsoft_Azure_CostManagement/Menu/Overview) no portal para monitorar gastos.
- **Automatize Desligamento**: Use o recurso de desligamento automático para VMs não utilizadas.
- **Explore o Azure Cloud Shell**: Disponível no portal, permite executar comandos CLI/PowerShell sem instalar ferramentas localmente.
- **Use Grupos de Recursos**: Eles ajudam a organizar e excluir recursos relacionados de uma só vez.
- **Consulte a Documentação**: A [documentação do Azure](https://learn.microsoft.com/azure) é detalhada e inclui tutoriais adicionais.

---

## 🧠 Conclusão

Este README documenta o processo de criação de uma máquina virtual Windows no Azure, desde a configuração de contas no GitHub e Azure até a implantação e exclusão de recursos. Seguindo estas etapas, você praticou conceitos de computação em nuvem e documentação técnica, criando um material reproduzível para estudos futuros.
