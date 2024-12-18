Sistema de PDV para Distribuidora de Bebidas

Este é um sistema de ponto de venda (PDV) desenvolvido em C# para atender às necessidades de uma distribuidora de bebidas. O sistema oferece funcionalidades como cadastro de produtos, gerenciamento de estoque, vendas em tempo real e geração de relatórios.

Funcionalidades

Cadastro de Bebidas: Inclua produtos com nome, código, preço, categoria, estoque e imagem.
Controle de Estoque: Atualização automática do estoque após vendas.
Frente de Caixa (PDV):
Busca em tempo real de produtos por nome ou código.
Adição de produtos ao carrinho com cálculo do valor total e troco.
Relatórios de Vendas: Relatórios diários e mensais gerados em Excel com informações detalhadas.
Sistema de Login: Diferenciação entre administrador e usuários normais, permitindo gerenciamento de contas pelo administrador.

Configuração do Banco de Dados

Este sistema utiliza o banco de dados MySQL, que funciona localmente com o XAMPP. Siga os passos abaixo para configurar o banco de dados:

Instale o XAMPP:

Faça o download e instale o XAMPP pelo site oficial: https://www.apachefriends.org.
Inicie os serviços Apache e MySQL:

Abra o XAMPP e clique em "Start" para iniciar os serviços Apache e MySQL.
Crie o banco de dados no phpMyAdmin:

Acesse o phpMyAdmin no navegador pelo endereço http://localhost/phpmyadmin.
Clique em "Novo" no menu lateral esquerdo e crie um banco de dados chamado banco_pdv.
Vá até a aba "Importar", clique em "Escolher arquivo" e selecione o arquivo banco_pdv.sql do repositório. Clique em "Executar" para criar as tabelas do sistema.
Configure a conexão no sistema:
Certifique-se de que o arquivo App.config do projeto está com a seguinte string de conexão:

xml
Copiar código
<connectionStrings>
    <add name="MySqlConnection" 
         connectionString="Server=localhost;Database=banco_pdv;Uid=root;Pwd=;" 
         providerName="MySql.Data.MySqlClient" />
</connectionStrings>
Nota: Se você configurar uma senha para o MySQL, altere o valor de Pwd na string de conexão para refletir essa mudança.

Execute o sistema:

Certifique-se de que o XAMPP está rodando.
Compile e execute o sistema no Visual Studio ou pelo executável gerado na pasta bin/Debug.
