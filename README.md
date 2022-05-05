# Objetivo
Criar API REST com autenticação JWT seguindo a metodologia DDD para realizar um CRUD através do ORM EntityFramework 6.0 por meio do Code-First e fazendo o uso de migrations para gerar o banco de dados no PostGreSQL.

# Entidades que devem ser criadas no Banco de Dados

<details>
  <summary><b>1 - User</b></summary>
  
  ~~~
  User{
  Id: GUID
  Name: string
  PassWord: usando criptografia SHA1
  Login: string
  Email: string
  BirthDay: DateTime
  LastAcess: DateTime
  CreateDate: DateTime
  }
  ~~~

</details>
<p>

<details>
  <summary><b>2 - Product</b></summary>
  
  ~~~
  Product{
  Id: GUID
  IsActive: bool
  Description: string
  IsDue: Bool
  DueDate: DateTime
  Amount: int
  CreateDate: DateTime
  }
  ~~~

</details>
<p>


<details>
  <summary><b>3 - ProductPrice</b></summary>
  
  ~~~
  ProductPrice{
  Id: GUID
  ProductId: FK_ProductId
  Value: double
  }
  ~~~

</details>
<p>

<details>
  <summary><b>4 - ProductHistorySell</b></summary>
  
  ~~~
  ProductHistorySell{
  Id: GUID
  ProductName: string
  PriceCurrent: double
  AmountProduct: int
  UserName: string
  }
  ~~~

</details>
<p>



# Endpoint a ser criado
~~~
- User
  - GetById
  - Create
  - Update
  - Delete
~~~
~~~
- Product
  - Create
  - GetById
  - Update
  - GetByName
~~~

~~~
- ProductHistorySell
  - GetById
  - GetByName
  - Create
  - Delete
  - Update
  - DisableProduto
  - EnableProduto
~~~

# Estrutura DDD da API a ser criada

<details>
  <summary><b>1 - Aplication</b></summary>
  
  - Controllers

</details>
<p>

<details>
  <summary><b>3 - Domain</b></summary>
  
  - DTO
  - Entities
  - Interfaces
  - Utils

</details>
<p>
  
<details>
  <summary><b>3 - Service</b></summary>
  
  - Interfaces
  - Services

</details>
<p>
  
<details>
  <summary><b>3 - Infra</b></summary>
  
  - Context
  - Mapping
  - Repository

</details>
<p>
  
  
 
