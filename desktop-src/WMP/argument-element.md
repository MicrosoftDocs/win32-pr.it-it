---
title: Elemento argument
description: L'elemento Argument contiene una parte di una stringa di condizione.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- Finestra degli elementi argomento Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c4adc0b853054d448bc9955f3bd8c64115ac2ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329206"
---
# <a name="argument-element"></a>Elemento argument

L'elemento **argument** contiene una parte di una stringa di condizione. Una stringa di condizione ha in genere una parte della condizione e una parte del valore. Ad esempio, nella stringa di condizione "Artist uguale a Joe", la parte della condizione è "Equals" e la parte del valore è "Joe".

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a>Attributi

**nome** (obbligatorio)

Nome di una parte della stringa della condizione.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                         |
|-----------|----------------------------------|
| Padre    | [frammento](fragment-element.md) |
| Figlio     | nessuno                             |



 

## <a name="remarks"></a>Osservazioni

Quando l'attributo **Name** di un elemento **Fragment** è una caratteristica dell'elemento multimediale, ad esempio Album Artist o genre, l'elemento **Fragment** deve contenere due elementi **argument** : uno che specifica una condizione e un altro che specifica un valore. La tabella seguente mostra due valori possibili per l'attributo **Name** e come vengono usati gli elementi **argument** per specificare le condizioni e i valori.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore di attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Condizione</td>
<td>Il contenuto dell'elemento <strong>argument</strong> è la parte della condizione di una stringa di condizione. Nella condizione, ad esempio, &quot; la stringa Artist è uguale a Joe &quot; , la parte della condizione è &quot; uguale a &quot; . La parte della condizione di una stringa di condizione deve essere una delle seguenti: Equals, non uguale a, Contains, non contiene, è minore di, è maggiore di, è, non è, è precedente a, è successiva a, è più recente di, superiore, inferiore, crescente, decrescente, casuale, è almeno, non è maggiore di.</td>
</tr>
<tr class="even">
<td>Valore</td>
<td>Il contenuto dell'elemento <strong>argument</strong> è la parte relativa al valore di una stringa di condizione. Nella condizione, ad esempio, &quot; la stringa Artist è uguale a Joe &quot; , la parte relativa al valore è &quot; Joe &quot; . Esempio<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Quando l'attributo **Name** di un elemento **Fragment** è "Limit Total Size to" o "Limit Total Duration to", l'elemento **Fragment** deve contenere due elementi **argument** : uno che specifica un formato e uno che specifica un numero. La tabella seguente illustra due valori possibili per l'attributo **Name** e come vengono usati gli elementi **argument** per limitare le dimensioni o la durata di una playlist.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Quando l'attributo <strong>Name</strong> dell'elemento <strong>Fragment</strong> è &quot; limitato alle dimensioni totali &quot; , il contenuto dell'elemento <strong>argument</strong> deve essere uno dei seguenti: kilobyte, megabyte o gigabyte. quando l'attributo <strong>Name</strong> dell'elemento <strong>Fragment</strong> è &quot; limite Total Duration a &quot; , il contenuto dell'elemento <strong>argument</strong> deve essere uno dei seguenti: seconds, minutes, hours o Days.<br/></td>
</tr>
<tr class="even">
<td>Number</td>
<td>Il contenuto dell'elemento <strong>argument</strong> è un numero che limita la dimensione o la durata della playlist. Esempi<br/>
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



 

Quando l'attributo **Name** di un elemento **Fragment** è "Limit number of items", l'elemento **Fragment** deve contenere un elemento **argument** che specifica il numero di elementi. Nella tabella seguente viene illustrato come utilizzare il valore numerico dell'attributo **Name** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore di attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Number</td>
<td>Il contenuto dell'elemento <strong>argument</strong> è un numero che limita il numero di elementi in una playlist. Esempio<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





