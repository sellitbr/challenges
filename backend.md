# Desafio de Backend

Na Sellit, somos uma plataforma completa para venda de produtos, infoprodutos e serviços, oferecendo um ecossistema robusto para potencializar suas vendas.

Quando programamos, nós seguimos uma série de melhores práticas e padrões de projeto (que você pode ler sobre em livros como Código Limpo, Arquitetura Limpa, O Programador Pragmático, Domain-Driven Design, Microservice Patterns, etc...).

Já que escrever **um bom código é inegociável** no nosso dia a dia, esperamos que as pessoas que queiram entrar no nosso time pensem da mesma maneira. Este teste foi criado para encontrar esses programadores.

## 1. O que queremos que você faça

Esperamos que você desenvolva um serviço que disponibilize uma API REST ou GraphQL que implemente essas funcionalidades e requisitos técnicos:

### 1.1. Criar um produto:

Salvar no banco de dados **todas** as seguintes informações representadas por este JSON junto com as regras subsequentes:

```json
{
  "id": "01J49K9MD3PCHX289ZA5BCT713",
  "category_id": "01J49KJC72PV5AY2SBMNS2ZE5K",
  "name": "Transforme Sua Carreira com Estratégias Comprovadas",
  "description": "Descubra como maximizar seu potencial, construir redes influentes ​e garantir uma promoção rápida. Seu futuro começa aqui!",
  "producer_name": "Thiago Bastos",
  "producer_email": "me@thiago-bastos.com",
  "cover": "https://example.com/img/cover.jpg",
  "thumbnail": "https://example.com/img/thumbnail.jpg",
  "price": 29.9,
  "updated_at": "2021-08-01T00:00:00Z",
  "created_at": "2021-08-01T00:00:00Z"
}
```

- `id:` Identificador único do produto no formato ULID. Este campo deve ser único entre todos os produto.
- `category_id:` Identificador único da categoria do produto no formato ULID. Este campo deve ser único entre todas as - categorias.
- `name:` Nome do produto ou serviço, representado como uma string.
- `description:` Descrição do produto ou serviço, explicando suas características e benefícios, representado como uma string.
- `producer_name:` Nome do produtor ou responsável pelo produto/serviço, representado como uma string.
- `producer_email:` Endereço de e-mail do produtor ou responsável, representado como uma string.
- `cover:` URL da imagem de capa do produto ou serviço, representado como uma string.
- `thumbnail:` URL da imagem em miniatura do produto ou serviço, representado como uma string.
- `price:` Preço do produto ou serviço, representado como um número decimal.
- `updated_at:` Data e hora da última atualização do registro, no formato ISO 8601.
- `created_at:` Data e hora da criação do registro, no formato ISO 8601.

Você pode usar as seguintes ferramentas para gerar dados fictícios de produtos para testar o seu serviço:

- [JSONDataAI](https://jsondataai.com)
- [DummyJSON](https://dummyjson.com)

Estas ferramentas permitem que você crie centenas de informações de produtos para testar a sua aplicação — **não** esperamos que estes produtos estejam pré-carregados em sua base de dados.

### 1.2. Carregar produto pelo `id`:

Retornar um produto específico baseado no seu campo `id` com todos os campos apresentados acima.

### 1.3. Buscar produtos:

Dado o nome do produto ou o nome do fornecedor pelo usuário da API (campos `name` e `producer_name`), procure o produto que **mais se aproxime** do termo informado."

### 1.4. Requerimentos Técnicos:

* Use Next.js com TypeScript para o desenvolvimento do serviço;
* Utilize PostgreSQL como banco de dados;
* Nosso ORM preferido é o Drizzle;
* O seu projeto deve ser **multi-plataforma**;
* Você deve escrever um arquivo de documentação (`DEVELOPER.md`) explicando como executar o seu serviço **localmente** e como colocá-lo em produção (*foque na simplicidade e não se esqueça que iremos testar seu serviço por nossa própria conta, sem qualquer assistência sua*).

## Método de Avaliação

Vamos avaliar seu teste com base em uma série de [atributos de qualidade](https://en.wikipedia.org/wiki/List_of_system_quality_attributes). Consideramos a **corretude** essencial, desclassificando seu teste caso não esteja 100% de acordo. Os outros atributos serão considerados, mas não são eliminatórios por si só. Esses são os atributos de qualidade que esperamos que você atenda:

- **Corretude:** O código deve seguir **todos** os requisitos apresentados no item [1.](#1-o-que-queremos-que-você-faça).
- **Performance:** A capacidade de lidar eficientemente com um grande número de produtos na base de dados e responder rapidamente às consultas.
- **Testabilidade:** O quão bem testado é o código e a facilidade de adicionar novos testes.
- **Manutenibilidade:** Facilidade de adicionar novas funcionalidades ao código.
- **Separação de conceitos:** Implementação clara da separação de responsabilidades no código, seguindo o princípio de [separação de conceitos](https://en.wikipedia.org/wiki/Separation_of_concerns).

## Como Entregar

- Coloque seu código em um **repositório público no Github** e mencione o @sellitbot em uma issue.
  Essa conta no Github (@sellitbot) é utilizada exclusivamente pelos engenheiros da Sellit para baixar o seu código e revisá-lo.
- **Após finalizar o desafio, por favor submeta as informações por meio deste formulário:**
  https://tally.so/r/meLqJ0

Boa sorte!
