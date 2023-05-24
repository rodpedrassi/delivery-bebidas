# Boas vindas ao repositório do projeto Delivery de Bebidas!
<details>
  <summary>
    <strong>Do que se trata?</strong>
  </summary><br>

  **Neste projeto, nosso grupo desenvolveu um app de delivery para uma distribuidora de bebidas.**

  A distribuidora de cervejas da dona Tereza está se informatizando! Seu negócio, antes focado em um local específico da cidade, passou a receber uma quantidade massiva de encomendas de outros pontos, expandindo sua atuação via delivery. Isso tudo graças ao excelente preço das bebidas e atendimento da equipe de vendas.

  Agora a distribuidora possui alguns pontos de venda na cidade para agilizar no atendimento dessas áreas. Cada ponto de venda, por sua vez, possui uma pessoa vendedora responsável.

  Como seu antigo sistema, que era um conjunto de planilhas, já não atende a necessidade do negócio por gerar muita manutenção, procuramos desenvolver uma ideia de aplicativo que pudesse agilizar a vida de sua equipe e das pessoas que compram seus produtos. O aplicativo inclui:

- Ter acesso via login: tanto clientes como pessoas vendedoras, assim como a própria dona Tereza, que administra o sistema, devem ter acesso ao aplicativo via login, porém para funções diferentes: (1) A pessoa cliente, que compra da lista de produtos; (2) A pessoa vendedora, que aprova, prepara e entrega; (3) A pessoa administradora, que gerencia quem usa o aplicativo;
- Fazer a comunicação entre clientes e pessoas vendedoras: a pessoa cliente faz o pedido via "carrinho de compras" e a pessoa vendedora aprova, prepara e envia esse pedido. Quando o produto é recebido por quem comprou, essa pessoa marca o pedido como "recebido". Ambos devem possuir detalhes sobre seus pedidos;
- Se a pessoa cliente faz o pedido, o mesmo deve aparecer para a pessoa vendedora em seu dash de pedidos após a atualização da página. A pessoa cliente, por sua vez, deve ter as informações sobre seu pedido quando sua página for atualizada, ou seja, ter informações se o pedido está sendo preparado ou se já saiu pra entrega;

</details>

<details>
  
  <summary>
    <strong>Diagrama entidade de relacionamento</strong>
  </summary><br>
  
   ![Diagrama de ER](./assets/readme/der.png)
  
</details>

<details>
  <summary>
    <strong>Scripts do <code>package.json</code> principal</strong>
  </summary><br>

  **São os scripts da raiz do projeto (`./package.json`) e não das aplicações individuais `./front-end/package.json` e `./back-end/package.json`**:

- `start`: Limpa as portas `3000` e `3001`. Também prepara o campo rodando o `Sequelize` para restaurar o **banco de dados de testes** (final `-test`) e sobe a aplicação com `pm2` em modo `fork` (uma instância para cada aplicação). Nesse modo, as alterações não são assistidas;
  - *uso (na raiz do projeto): `npm start`*

- `stop`: Para e deleta as aplicações rodando no `pm2`;
  - *uso (na raiz do projeto): `npm stop`*

- `dev`: Limpa as portas `3000` e `3001` e sobe a aplicação com `pm2` em modo `fork` (uma instância pra cada aplicação). Nesse modo, as atualizações são assistidas (modo `watch`);
  - *uso (na raiz do projeto): `npm run dev`*

- `dev:prestart`: A partir da raiz, esse comando faz o processo de instalação de dependências (`npm i`) nos dois projetos (`./front-end` e `./back-end`) e roda o `Sequelize` no `./back-end` (lembrar de configurar o `.env` no mesmo);
  - *uso (na raiz do projeto): `npm run dev:prestart`*

- `db:reset`: Roda os scripts do `Sequelize` restaurando o **banco de dados de desenvolvimento** (final `-dev`). Utilize esse script caso ocorra algum problema no seu banco local;
  - *uso (na raiz do projeto): `npm run db:reset`*

- `db:reset:debug`: Roda os scripts do `Sequelize` restaurando o **banco de dados de desenvolvimento** (final `-dev`). Utilize esse script caso ocorra algum problema no seu banco local. Esse comando também é capaz de retornar informações detalhadas de erros (quando ocorrerem no processo);
  - *uso (na raiz do projeto): `npm run db:reset:debug`*

</details>


<details>
  
   <summary>
    <strong>Usuários do sistema</strong>
  </summary><br>
  
  - Cliente:. <br>
    - usuário: zebirita@email.com 
    - senha: "$#zebirita#$" (sem as "") <br>
  - Vendedor:. <br>
    - usuário: fulana@deliveryapp.com 
    - senha: fulana@123 <br>
  - Adm:. <br>
    - usuário: adm@deliveryapp.com 
    - senha: --adm2@21!!-- <br>
  
</details>
