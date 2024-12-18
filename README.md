Aqui está o README formatado e organizado para você colocar no GitHub:  

---

# 💻 Sistema de PDV para Distribuidora de Bebidas  

Este é um sistema de **Ponto de Venda (PDV)** desenvolvido em **C#** para facilitar o gerenciamento de vendas e estoque em uma distribuidora de bebidas. Com funcionalidades modernas e uma interface intuitiva, o sistema atende às principais demandas do setor, incluindo cadastro de produtos, vendas em tempo real, controle de estoque e relatórios detalhados.  

---

## 📋 Funcionalidades  

- **📦 Cadastro de Bebidas:**  
  - Adicione produtos ao sistema com informações detalhadas: nome, código, preço, categoria, estoque e imagem.  
  - Atualize ou remova produtos diretamente no painel de cadastro.  

- **🛒 Frente de Caixa:**  
  - Busque produtos em tempo real pelo nome ou código.  
  - Adicione produtos ao carrinho, insira a quantidade desejada e veja o total da compra instantaneamente.  
  - Calcule o troco automaticamente.  

- **📊 Relatórios de Vendas:**  
  - Gere relatórios diários e mensais em formato Excel com informações detalhadas, como:  
    - Nome do produto, quantidade vendida, preço total por item e faturamento total.  

- **🔒 Sistema de Login:**  
  - Acesso diferenciado para **administrador** e **usuários normais**.  
  - Apenas o administrador pode gerenciar contas de usuários.  

---

## 🚀 Como Configurar e Usar  

### 1️⃣ Requisitos  
- **XAMPP** para gerenciar o banco de dados MySQL.  
- **Visual Studio** para compilar e rodar o projeto.  

---

### 2️⃣ Configuração do Banco de Dados  

O banco de dados é gerenciado pelo **MySQL** através do XAMPP. Siga os passos abaixo para configurar:  

#### **Instale o XAMPP**  
- Baixe o XAMPP pelo site oficial: [https://www.apachefriends.org](https://www.apachefriends.org).  
- Após instalar, abra o XAMPP e inicie os serviços **Apache** e **MySQL**.  

#### **Crie o banco de dados no phpMyAdmin**  
1. Acesse o phpMyAdmin no navegador pelo endereço: [http://localhost/phpmyadmin](http://localhost/phpmyadmin).  
2. Clique em **"Novo"** no menu lateral esquerdo.  
3. Dê o nome **banco_pdv** ao banco de dados e clique em **"Criar"**.  
4. Vá até a aba **"Importar"**, clique em **"Escolher arquivo"** e selecione o arquivo `banco_pdv.sql` disponível no repositório.  
5. Clique em **"Executar"** para carregar as tabelas do sistema.  

---

### 3️⃣ Configuração da Conexão  

Certifique-se de que o arquivo `App.config` do projeto está configurado corretamente:  

```xml
<connectionStrings>
    <add name="MySqlConnection" 
         connectionString="Server=localhost;Database=banco_pdv;Uid=root;Pwd=;" 
         providerName="MySql.Data.MySqlClient" />
</connectionStrings>
```  

#### **Detalhes:**  
- **Server=localhost:** O endereço do servidor MySQL.  
- **Database=banco_pdv:** O nome do banco de dados que você criou.  
- **Uid=root:** O nome de usuário padrão do MySQL no XAMPP.  
- **Pwd=;** Deixe a senha vazia (a menos que você tenha configurado uma).  

---

### 4️⃣ Como Executar  

1. **Clone o repositório:**  
   ```bash
   git clone https://github.com/seu-usuario/pdv-distribuidora.git
   ```  

2. **Compile o projeto no Visual Studio:**  
   - Abra o projeto no Visual Studio.  
   - Compile para gerar o executável na pasta `bin/Debug`.  

3. **Execute o sistema:**  
   - Certifique-se de que o XAMPP está rodando (Apache e MySQL ativos).  
   - Execute o arquivo gerado na pasta `bin/Debug`.  

4. **Acesse o sistema:**  
   - **Administrador:**  
     - Usuário: `adm`  
     - Senha: `administrador`  
   - **Usuário comum:** Utilize as contas criadas pelo administrador.  

---

## 🎯 Como Contribuir  

1. Faça um fork deste repositório.  
2. Crie uma branch com sua feature:  
   ```bash
   git checkout -b minha-feature
   ```  
3. Commit suas mudanças:  
   ```bash
   git commit -m 'Minha nova feature'
   ```  
4. Faça o push para a branch:  
   ```bash
   git push origin minha-feature
   ```  
5. Abra um Pull Request.  

---

## 🛠️ Tecnologias Utilizadas  

- **C#:** Desenvolvimento do sistema.  
- **MySQL:** Banco de dados.  
- **XAMPP:** Gerenciamento do servidor local.  
- **Visual Studio:** IDE para desenvolvimento.  
