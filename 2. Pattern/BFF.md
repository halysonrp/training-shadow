## Boas práticas do BFF

Esse material tem como objetivo especificar as boas praticas de utilização do BFF(Backend for frontend) na empresa.

A adoção de um padrão..... tem como objetivo facilitar 


## O que recomendamos?

- Podemos usar para fazer Mocks.
- Podemos utilizar para o armazenamento em cache, garantindo a resilência, em caso de indisponibilidade dos microservices.
- Utilize o BFF para filtrar informações, ou seja, retornar apenas os atributos necessários para a camada de UI.
- ⚠ Chamar múltiplas requests... Composição no BFF iremos considerar como boa prática? Ou iremos manter a composição a nível de microservices? A partir de quantas chamadas ou integrações devemos considerar abstrair a composição nos microservices? Existem as duas abordageens.
- BFF fazendo a composição:
<img src="https://user-images.githubusercontent.com/12093535/197595185-30e6a9ee-0254-419d-8238-3178782cd5e9.png" width="350" height="350">
- Microservice fazendo a Composição
<img src="https://user-images.githubusercontent.com/12093535/197595233-074853c0-3ce2-4ec7-91eb-3fe02c1e6356.png" width="350" height="350">

- Utilize um BFF por experiência do usuário, se as experiências do iOS e do Android são muito semelhantes, é mais fácil justificar ter um único BFF, caso contrário ter BBFs separados faz mais sentido.
<img src="https://user-images.githubusercontent.com/12093535/197592299-40f5ecc5-92bb-4e28-8d77-1bf60bce36e7.png" width="350" height="350">

## O que não recomendamos?

- Não recomendamos manter regras de negócio.

## Mono BFF ou Micro BFF's?

Racional:

| Caso de uso   | Mono BFF      | Micro BFF     | 
| ------------- | ------------- | ------------- |
| BFF será mantido por mais de uma equipe! | X  | ✔️  |
| Em caso de indisponibilidade acarretará em alto impacto para a operação!  | X   | ✔️  | 




### Fontes:

Pattern: Backends For Frontends:
https://samnewman.io/patterns/architectural/bff/


<img src="https://user-images.githubusercontent.com/12093535/197590032-0dc49c6c-715f-4970-b0e7-7063d0e48592.png" width="280" height="350">
