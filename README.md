# API de consultas à Biblioteca Nacional

Esta API busca dados de livros cadastrados na Biblioteca Nacional e os devolve estruturados num JSON.

## Por que foi criado

Durante a concepção do Libmin, o nosso software para gestão de bibliotecas escolares, foi percebida a necessidade de simplificar a forma com que se cadastra os materiais. Já existem protocolos de interoperabilidade entre bibliotecas, mas nem sempre eles estão implementados ou disponíveis.

## Como utilizar

Faça uma consulta para o endpoint abaixo informando a URl do livro que desejar parsear, exemplo:

```bash
curl http://localhost:3000/url?q=https://acervo.bn.gov.br/Sophia_web/acervo/detalhe/1733119
```

Exemplo de resposta:

```json
{
  "title": "A divina comédia",
  "material": "Livro",
  "language": "Português",
  "isbn_code": "9788573261202",
  "dewey": "851 (Edição 23)",
  "location": "Obras Gerais - LOCALIZANDO/FORA DE CONSULTA",
  "uniform_title": "[La divina commedia]InfernoPurgatórioParaiso",
  "publisher": "[São Paulo] : Editora 34, 2019.",
  "physical_description": "1v. ; 24 cm.",
  "general_note": "Dante Alighieri ; tradução e notas de Italo Eugenio Mauro ; prefácio de Otto Maria Carpeaux",
  "subjects": [
    "Poesia italiana"
  ],
  "authors": [
    "Dante Alighieri, 1265-1321",
    "",
    "Mauro, Italo Eugenio 1909-2003",
    ""
  ],
  "cover_image": "https://acervo.bn.gov.br/Sophia_web/capa/capa/1739805"
}
```

## Como colaborar

Se você gostou do <strong>consultas_bn</strong>, fique à vontade para melhorá-lo.

- Faça uma cópia deste projeto
```js
git clone https://github.com/libmin/consultas_bn.git
```

- Acesse o diretório
```js
cd consultas_bn
```

- Instale as dependências
```js
npm install
```

- Inicie o server
```js
npm run dev
```

- Testando (healtcheck)
```bash 
curl http://localhost:3000
```

- Buscando um livro
```bash
curl http://localhost:3000/url?q={url-do-livro-na-bn}
```
