##  BFF (Backend For Frontend)

Esse material tem como objetivo especificar as boas praticas de utilização do BFF(Backend for frontend) na empresa.

## O que é um BFF?

BFF é um sigla para back-end for front-end — termo criado em 2015 por Phil Calçado, e é um padrão para API que permite equipes a iterarem recursos mais rapidamente e terem controle sobre o backend, sem afetar o frontend e também gerar experiências específicas de acordo com cada pessoa usuária de um determinado produto.

## Pra que serve? qual sua responsabilidade?

## Mono BFF ou Micro BFF's?

Racional:

| Caso de uso   | Mono BFF      | Micro BFF     | 
| ------------- | ------------- | ------------- |
| BFF será mantido por mais de uma equipe! | X  | ✔️  |
| Em caso de indisponibilidade acarretará em alto impacto para a operação!  | X   | ✔️  | 

## Quais as funcionalidades obrigatórias?
- Cache:
  - Utilize armazenamento em cache, para garantir a resilência do seu sistema, em caso de indisponibilidade dos microservices, o seu sistema continua operando normalmente.
- Retry:
  - Implemente um mecanimo de retentativa em caso obtiver falha na primeira chamada.
- Filtro:
  - Utilize o BFF para filtrar/retornar apenas informações que sejam necessárias para a camada de UI.
- Paralelismo:
  - Opte por realizar chamadas em paralelas ao invés de chamadas sequênciais.
  - Chamadas em paralelas diminuem o tempo de resposta.
    - Chamada sequencial, representa a soma de todas as requests.
    - Enquanto a chamada em paralela, representa o maior tempo entre as requests.
- Monitoramento:
  - Crie logs e gere alertas que te ajudem a identificar possíveis erros. 
- Logs:
  - Crie logs que te ajudem a identificar possíveis erros. 
- ⚠ Chamar múltiplas requests... Composição no BFF, iremos considerar como boa prática? Ou iremos manter a composição a nível de microservices? A partir de quantas chamadas ou integrações devemos considerar abstrair a composição nos microservices? Existem as duas abordageens.
- BFF fazendo a composição:
<img src="https://user-images.githubusercontent.com/12093535/197595185-30e6a9ee-0254-419d-8238-3178782cd5e9.png" width="350" height="350">
- Microservice fazendo a Composição
<img src="https://user-images.githubusercontent.com/12093535/197595233-074853c0-3ce2-4ec7-91eb-3fe02c1e6356.png" width="350" height="350">


## Quais as funcionalidades opcionais ?

- Utilize o BFF para fazer Mocks.
- Utilize um BFF por experiência do usuário, se as experiências do iOS e do Android são muito semelhantes, é mais fácil justificar ter um único BFF, caso contrário ter BBFs separados faz mais sentido.
<img src="https://user-images.githubusercontent.com/12093535/197592299-40f5ecc5-92bb-4e28-8d77-1bf60bce36e7.png" width="350" height="350">

## O que não devemos fazer?

- Não devemos manter regras de negócio.

## Exemplos:

### Fontes:

O que é BFF:
https://brasil.uxdesign.cc/quem-%C3%A9-o-bff-na-fila-do-p%C3%A3o-ef58d87bbab0

Pattern: Backends For Frontends:
https://samnewman.io/patterns/architectural/bff/

<img src="https://user-images.githubusercontent.com/12093535/197590032-0dc49c6c-715f-4970-b0e7-7063d0e48592.png" width="280" height="350">
