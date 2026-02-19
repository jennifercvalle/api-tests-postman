##  Sobre o Projeto

Este projeto contém testes manuais de API realizados na plataforma CoinMarketCap, utilizando a ferramenta Postman.

O objetivo foi praticar testes de API como QA Júnior, validando regras de negócio, segurança, respostas da API e tratamento de erros.

---

##  Ferramentas Utilizadas

- Postman
- API CoinMarketCap (https://coinmarketcap.com/api/documentation/v1/#operation/getV2CryptocurrencyQuotesLatest)

---

##  Endpoints Testados

- https://pro-api.coinmarketcap.com/v2/cryptocurrency/quotes/latest

---

## Cenários de testes


<table>
  <tr>
   <td>ID:
   </td>
   <td>1
   </td>
  </tr>
  <tr>
   <td>Endpoint:
   </td>
   <td>pro-api.coinmarketcap.com/v2/cryptocurrency/quotes/latest
   </td>
  </tr>
  <tr>
   <td>Método:
   </td>
   <td>Get
   </td>
  </tr>
  <tr>
   <td>Cenário:
   </td>
   <td>Acessar API com API KEY inválida
   </td>
  </tr>
  <tr>
   <td>Parâmetros:
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Resultado Esperado:
   </td>
   <td>Retornar erro de requisição inválida
   </td>
  </tr>
  <tr>
   <td>Resultado Obtido:
   </td>
   <td><code>{</code>
<p>
<code>   "status": {</code>
<p>
<code>       "timestamp": "2026-02-19T19:37:21.882Z",</code>
<p>
<code>       "error_code": 1001,</code>
<p>
<code>       "error_message": "This API Key is invalid.",</code>
<p>
<code>       "elapsed": 0,</code>
<p>
<code>       "credit_count": 0</code>
<p>
<code>   }</code>
<p>
<code>}</code>
   </td>
  </tr>
  <tr>
   <td>Status:
   </td>
   <td>APROVADO 
   </td>
  </tr>

  <tr>
   <td>Evidência:
   </td>
   <td>
       <img src="evidence_images/image1.png" width="" alt="alt_text" title="image_tooltip">
   </td>
  </tr>


</table>



<table>
  <tr>
   <td>ID:
   </td>
   <td>2
   </td>
  </tr>
  <tr>
   <td>Endpoint:
   </td>
   <td>pro-api.coinmarketcap.com/v2/cryptocurrency/quotes/latest
   </td>
  </tr>
  <tr>
   <td>Método:
   </td>
   <td>Get
   </td>
  </tr>
  <tr>
   <td>Cenário:
   </td>
   <td>Acessar API com campo vazio na API KEY 
   </td>
  </tr>
  <tr>
   <td>Parâmetros:
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Resultado Esperado:
   </td>
   <td>Retornar erro de mensagem de formato inválido
   </td>
  </tr>
  <tr>
   <td>Resultado Obtido:
   </td>
   <td><code>{</code>
<p>
<code>    "status": {</code>
<p>
<code>        "timestamp": "2026-02-19T19:36:57.128Z",</code>
<p>
<code>        "error_code": 1002,</code>
<p>
<code>        "error_message": "API key missing.",</code>
<p>
<code>        "elapsed": 0,</code>
<p>
<code>        "credit_count": 0</code>
<p>
<code>    }</code>
<p>
<code>}</code>
   </td>
  </tr>
  <tr>
   <td>Status:
   </td>
   <td>APROVADO 
   </td>
  </tr>
  <tr>
   <td>Evidência:
   </td>
   <td>
       <img src="evidence_images/image2.png" width="" alt="alt_text" title="image_tooltip">
   </td>
  </tr>
</table>



<table>
  <tr>
   <td>ID:
   </td>
   <td>3
   </td>
  </tr>
  <tr>
   <td>Endpoint:
   </td>
   <td>pro-api.coinmarketcap.com/v2/cryptocurrency/quotes/latest
   </td>
  </tr>
  <tr>
   <td>Método:
   </td>
   <td>Get
   </td>
  </tr>
  <tr>
   <td>Cenário:
   </td>
   <td>Consultar o preço de uma criptomoeda e validar o valor com o site
   </td>
  </tr>
  <tr>
   <td>Parâmetros:
   </td>
   <td>symbol=BTC,ETH
   </td>
  </tr>
  <tr>
   <td>Resultado Esperado:
   </td>
   <td>Retorne preço corretamente
   </td>
  </tr>
  <tr>
   <td>Resultado Obtido:
   </td>
   <td><code> "USD": {</code>
<p>
<code>                        "price": 67021.27998566446,</code>
<p>
<code>}</code>
   </td>
  </tr>
  <tr>
   <td>Status:
   </td>
   <td>APROVADO 
   </td>
  </tr>
  <tr>
   <td>Evidência:
   </td>
   <td>
       <img src="evidence_images/image3.png" width="" alt="alt_text" title="image_tooltip">
     <img src="evidence_images/image4.png" width="" alt="alt_text" title="image_tooltip">
   </td>
  </tr>
</table>



<table>
  <tr>
   <td>ID:
   </td>
   <td>4
   </td>
  </tr>
  <tr>
   <td>Endpoint:
   </td>
   <td>pro-api.coinmarketcap.com/v2/cryptocurrency/quotes/latest
   </td>
  </tr>
  <tr>
   <td>Método:
   </td>
   <td>Get
   </td>
  </tr>
  <tr>
   <td>Cenário:
   </td>
   <td>Consultar o preço de uma criptomoeda e converter o valor em moeda fiduciária
   </td>
  </tr>
  <tr>
   <td>Parâmetros:
   </td>
   <td>symbol=BTC/ convert=BRL
   </td>
  </tr>
  <tr>
   <td>Resultado Esperado:
   </td>
   <td>Retorne valor convertido corretamente
   </td>
  </tr>
  <tr>
   <td>Resultado Obtido:
   </td>
   <td><code>"quote": {</code>
<p>
<code>                   "BRL": {</code>
<p>
<code>                       "price": 350065.80569959665,</code>
   </td>
  </tr>
  <tr>
   <td>Status:
   </td>
   <td>APROVADO 
   </td>
  </tr>
  <tr>
   <td>Evidência:
   </td>
   <td>
       <img src="evidence_images/image5.png" width="" alt="alt_text" title="image_tooltip">
   </td>
  </tr>
</table>



<table>
  <tr>
   <td>ID:
   </td>
   <td>5
   </td>
  </tr>
  <tr>
   <td>Endpoint:
   </td>
   <td>pro-api.coinmarketcap.com/v2/cryptocurrency/quotes/latest
   </td>
  </tr>
  <tr>
   <td>Método:
   </td>
   <td>Get
   </td>
  </tr>
  <tr>
   <td>Cenário:
   </td>
   <td>Validar formatos nas respostas da API se condizem com a documentação
   </td>
  </tr>
  <tr>
   <td>Parâmetros:
   </td>
   <td>symbol=BTC
   </td>
  </tr>
  <tr>
   <td>Resultado Esperado:
   </td>
   <td>Formato retorna exatamente conforme descrito na documentação
   </td>
  </tr>
  <tr>
   <td>Resultado Obtido:
   </td>
   <td><code>"BTC": [</code>
<p>
<code>           {</code>
<p>
<code>               "id": 1,</code>
<p>
<code>               "name": "Bitcoin",</code>
<p>
<code>               "symbol": "BTC",</code>
<p>
<code>               "slug": "bitcoin",</code>
<p>
<code>               "num_market_pairs": 12562,</code>
<p>
<code>               "date_added": "2010-07-13T00:00:00.000Z",</code>
<p>
<code>               "tags": [</code>
<p>
<code>                 …</code>
<p>
<code>               ],</code>
<p>
<code>               "max_supply": 21000000,</code>
<p>
<code>               "circulating_supply": 19992006,</code>
<p>
<code>               "total_supply": 19992006,</code>
<p>
<code>               "is_active": 1,</code>
<p>
<code>               "infinite_supply": false,</code>
<p>
<code>               "minted_market_cap": 1339180744008.09,</code>
<p>
<code>               "platform": null,</code>
<p>
<code>               "cmc_rank": 1,</code>
<p>
<code>               "is_fiat": 0,</code>
<p>
<code>               "self_reported_circulating_supply": null,</code>
<p>
<code>               "self_reported_market_cap": null,</code>
<p>
<code>               "tvl_ratio": null,</code>
<p>
<code>               "last_updated": "2026-02-19T20:35:00.000Z",</code>
<p>
<code>               "quote": {</code>
<p>
<code>                   "USD": {</code>
<p>
<code>                       "price": 66985.81142923291,</code>
<p>
<code>                       "volume_24h": 32142817352.32578,</code>
<p>
<code>                       "volume_change_24h": 0.5372,</code>
<p>
<code>                       "percent_change_1h": 0.14967025,</code>
<p>
<code>                       "percent_change_24h": 0.85585978,</code>
<p>
<code>                       "percent_change_7d": 2.26595325,</code>
<p>
<code>                       "percent_change_30d": -25.16908177,</code>
<p>
<code>                       "percent_change_60d": -24.12589059,</code>
<p>
<code>                       "percent_change_90d": -19.99924961,</code>
<p>
<code>                       "market_cap": 1339180744008.093,</code>
<p>
<code>                       "market_cap_dominance": 58.3193,</code>
<p>
<code>                       "fully_diluted_market_cap": 1406702040013.89,</code>
<p>
<code>                       "tvl": null,</code>
<p>
<code>                       "last_updated": "2026-02-19T20:35:00.000Z"</code>
<p>
<code>                   }</code>
<p>
<code>               }</code>
<p>
<code>           },</code>
   </td>
  </tr>
  <tr>
   <td>Status:
   </td>
   <td>APROVADO 
   </td>
  </tr>
  <tr>
   <td>Evidência:
   </td>
   <td>
       <img src="evidence_images/image6.png" width="" alt="alt_text" title="image_tooltip">
   </td>
  </tr>
</table>



<table>
  <tr>
   <td>ID:
   </td>
   <td>6
   </td>
  </tr>
  <tr>
   <td>Endpoint:
   </td>
   <td>pro-api.coinmarketcap.com/v2/cryptocurrency/quotes/latest
   </td>
  </tr>
  <tr>
   <td>Método:
   </td>
   <td>Get
   </td>
  </tr>
  <tr>
   <td>Cenário:
   </td>
   <td>Verificar o preço de uma moeda com campo symbol vazio
   </td>
  </tr>
  <tr>
   <td>Parâmetros:
   </td>
   <td>symbol=
   </td>
  </tr>
  <tr>
   <td>Resultado Esperado:
   </td>
   <td>Retorna erro com mensagem de campo vazio
   </td>
  </tr>
  <tr>
   <td>Resultado Obtido:
   </td>
   <td><code>{</code>
<p>
<code>    "status": {</code>
<p>
<code>        "timestamp": "2026-02-19T20:49:07.162Z",</code>
<p>
<code>        "error_code": 400,</code>
<p>
<code>        "error_message": "\"symbol\" is not allowed to be empty",</code>
<p>
<code>        "elapsed": 0,</code>
<p>
<code>        "credit_count": 0</code>
<p>
<code>    }</code>
<p>
<code>}</code>
   </td>
  </tr>
  <tr>
   <td>Status:
   </td>
   <td>APROVADO 
   </td>
  </tr>
  <tr>
   <td>Evidência:
   </td>
   <td>
       <img src="evidence_images/image7.png" width="" alt="alt_text" title="image_tooltip">
   </td>
  </tr>
</table>



<table>
  <tr>
   <td>ID:
   </td>
   <td>7
   </td>
  </tr>
  <tr>
   <td>Endpoint:
   </td>
   <td>pro-api.coinmarketcap.com/v2/cryptocurrency/quotes/latest
   </td>
  </tr>
  <tr>
   <td>Método:
   </td>
   <td>Get
   </td>
  </tr>
  <tr>
   <td>Cenário:
   </td>
   <td>Verificar o preço de uma moeda com campo symbol inválido
   </td>
  </tr>
  <tr>
   <td>Parâmetros:
   </td>
   <td>symbol=JFHEIRUHIUTGBNJNG
   </td>
  </tr>
  <tr>
   <td>Resultado Esperado:
   </td>
   <td>Retorne erro 
   </td>
  </tr>
  <tr>
   <td>Resultado Obtido:
   </td>
   <td><code>{</code>
<p>
<code>    "status": {</code>
<p>
<code>        "timestamp": "2026-02-19T20:50:36.037Z",</code>
<p>
<code>        "error_code": 0,</code>
<p>
<code>        "error_message": null,</code>
<p>
<code>        "elapsed": 20,</code>
<p>
<code>        "credit_count": 1,</code>
<p>
<code>        "notice": null</code>
<p>
<code>    },</code>
<p>
<code>    "data": {</code>
<p>
<code>        "JFHEIRUHIUTGBNJNG": []</code>
<p>
<code>    }</code>
<p>
<code>}</code>
   </td>
  </tr>
  <tr>
   <td>Status:
   </td>
   <td>REPROVADO
   </td>
  </tr>
  <tr>
   <td>Observação:
   </td>
   <td>Retornou status 200, porém,  ele responde que encontrou a moeda mas retorna com objeto vazio.
   </td>
  </tr>
  <tr>
   <td>Evidência:
   </td>
   <td>
       <img src="evidence_images/image8.png" width="" alt="alt_text" title="image_tooltip">
   </td>
  </tr>
</table>
