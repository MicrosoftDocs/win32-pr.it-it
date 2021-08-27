---
title: Elemento argument
description: L'elemento argument contiene una parte di una stringa di condizione.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- Elemento argument Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f5a689b74bd18138361d9377358ddee5cf5979f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630192"
---
# <a name="argument-element"></a>Elemento argument

**L'elemento** argument contiene una parte di una stringa di condizione. Una stringa di condizione include in genere una parte di condizione e una parte di valore. Ad esempio, nella stringa di condizione "Artist Equals Joe", la parte della condizione è "Equals" e la parte del valore è "Joe".

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a>Attributi

**name** (obbligatorio)

Nome di una parte della stringa della condizione.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                         |
|-----------|----------------------------------|
| Padre    | [Frammento](fragment-element.md) |
| Figlio     | nessuno                             |



 

## <a name="remarks"></a>Osservazioni

Quando l'attributo  **name** di un elemento frammento è una caratteristica  dell'elemento multimediale, ad esempio Album Artist o Genre, l'elemento frammento deve contenere due elementi **argomento:** uno che specifica una condizione e un altro che specifica un valore. Nella tabella seguente vengono illustrati due valori possibili per **l'attributo name** e **come** vengono usati gli elementi dell'argomento per specificare condizioni e valori.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valore di attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Condition</td>
<td>Il contenuto <strong>dell'elemento argomento</strong> è la parte della condizione di una stringa di condizione. Ad esempio, nella stringa della condizione &quot; Artist Equals Joe &quot; la parte relativa alla condizione è Uguale a &quot; &quot; . La parte della condizione di una stringa di condizione deve essere una delle seguenti: Uguale a, Non uguale a, Contiene, Non contiene, è minore di, è maggiore di, È, Non è, È prima, è più recente di, è più recente di, Sopra, Sotto, Crescente, Decrescente, Casuale, è almeno, non è più di.</td>
</tr>
<tr class="even">
<td>Valore</td>
<td>Il contenuto <strong>dell'elemento argomento</strong> è la parte del valore di una stringa di condizione. Ad esempio, nella stringa di condizione &quot; Artist Equals Joe &quot; , la parte del valore è Joe &quot; &quot; . Esempio:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Quando l'attributo  **name** di un elemento frammento è "Limit Total  Size To"  o "Limit Total Duration To", l'elemento fragment deve contenere due elementi argomento: uno che specifica un formato e uno che specifica un numero. La tabella seguente illustra due valori possibili  per l'attributo **name** e come vengono usati gli elementi dell'argomento per limitare le dimensioni o la durata di una playlist.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valore di attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Formato</td>
<td>Quando l'attributo <strong></strong> <strong>name</strong> dell'elemento fragment è Limit Total Size To , il contenuto dell'elemento argument deve essere uno dei &quot; &quot; seguenti: <strong></strong> Kilobyte, Megabyte o Gigabyte. Quando <strong></strong> <strong></strong> l'attributo name dell'elemento fragment è Limit Total Duration To , il contenuto dell'elemento argument deve essere uno dei &quot; &quot; seguenti: Seconds, Minutes, Hours o Days. <strong></strong><br/></td>
</tr>
<tr class="even">
<td>Numero</td>
<td>Il contenuto <strong>dell'elemento argomento</strong> è un numero che limita le dimensioni o la durata della playlist. Esempi:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Quando **l'attributo name** di un elemento **fragment** è "Limit Number  of Items", l'elemento **fragment** deve contenere un elemento argument che specifica il numero di elementi. Nella tabella seguente viene illustrato come usare il valore Number **dell'attributo name.**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valore di attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Numero</td>
<td>Il contenuto <strong>dell'elemento argomento</strong> è un numero che limita il numero di elementi in una playlist. Esempio:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento fragment**](fragment-element.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi della playlist multimediale**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





