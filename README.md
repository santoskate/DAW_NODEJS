Discentes:
Catarina Santos,
Gaspar Brogueira, 
Carlos Bernardino, 

Docentes: Carlos Costa, Pedro Dias


***************************************************************************************************************************************************
***************************************************************************************************************************************************

Níveis implementados:

Básico --- Completo
Intermédio --- Completo
Avançado
	- Endpoint para enviar contacto ao vendedor de um determinado anúncio. --- Completo
	- Endpoint para criação de anúncio. --- Implementado, mas não funciona
	- Endpoint para adicionar um alerta que envia mail quando encontra um anúncio de acordo com o parameterizado. --- Não implementado


***************************************************************************************************************************************************
***************************************************************************************************************************************************
- Para testar com forms
	- iniciar o servidor - node mains.js
	- entrar em http://localhost:3333/ num browser

Nota: Como os forms foram criados apenas para facilitar os testes da API estes não têm validação de campos vazios, assumindo-se que é necessário estarem todos preenchidos, por from, sem excepção.




- Para testar sem forms
-> PEDIDOS GET

Exemplo por categoria e descrição

http://localhost:3333/search/motociclos-scooters-cat-379/Honda


Exemplo por categoria e preço desde/a aprtir de um determinado valor

http://localhost:3333/search/motociclos-scooters-cat-379/price/bigger/1000


Exemplo por descrição apenas

http://localhost:3333/search/Cao




-> PEDIDOS POST

Exemplo de pesquisa por uma categoria, preço e cidade especifica:

curl -d "category=calcado-cat-22&subject=botas&price=20&city=seixal" http://localhost:3333/search


Exemplo para envio de contacto:

curl -d "anuncio_id=ID_DO_ANUNCIO&text=MENSAGEM&name=NOME&phonenr=NR_TELEFONE&email=INSERIR_EMAIL&copy=1&user_id=ID_DO_ANUNCIANTE&offer_type=0&price=INSERIR_PRECO_DO_ANUNCIO" http://localhost:3333/send


Exemplo para criação de anuncio:

curl -d "form_id=139982339597037600&form_type=price&form_title=Titlo+de+exemplo&category_id=312&price_type=price&price=80&price_call=on&form_desc=Descrição+de+um+granda+teste.+Descrição+de+um+granda+teste.&bbr_district=Setúbal&bbr_state=Seixal&form_email=INSERIR_EMAIL_OXL&password=INSERIR_PASS_OLX&offer_type=0" http://localhost:3333/create
