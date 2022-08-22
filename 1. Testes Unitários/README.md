# Testes Unitários


# Padrão nomenclatura para testes unitários
A escolha de um padrão para nomenclatura de testes unitários, tem como objetivo auxiliar a leitura, de forma que facilite o desenvolvedor identificar o método, condição e resultado esperado do método pelo qual você está testando, facilitando o entendimento do teste sem mesmo ter aberto o conteúdo do seu método.



# Padrão nomenclatura
O nosso padrão é dividido em 3 etapas:


1. Defina o nome do método ao qual está sendo testado:
 - getCustomerByDocument_

2. Defina a condição do método que está sendo testado através da Clausula When: 
 - WhenSendDocumentValid_

3. Informe o resultado esperado através da Clausula “Expected”: 

 - ExpectedCustomer


Exemplo de implementação:


Exemplo código 1.0

```
@Test
private Customer getCustomerByDocument_WhenSendDocumentValid_ExpectedCustomer(){

}
```
Exemplo código 2.0

```
@Test(expected = BusinessExpeption.class)
private Order getOrderByOrderNumber_WhenSendOrderNumberInvalid_ExpectedBusinessExpeption(){

}
```



