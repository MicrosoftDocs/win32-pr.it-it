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
ms.openlocfilehash: 29b0c234d2410d512e2f034f92cbc4a2d6ad7449
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880265"
---
# <a name="argument-element"></a>Elemento argument

**L'elemento** argument contiene una parte di una stringa di condizione. Una stringa di condizione include in genere una parte di condizione e una parte di valore. Ad esempio, nella stringa di condizione "Artista uguale a Joe", la parte della condizione è "Uguale a" e la parte del valore è "Joe".

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

Quando l'attributo  **name** di un elemento frammento è una caratteristica  dell'elemento  multimediale, ad esempio Album Artist o Genre, l'elemento frammento deve contenere due elementi argomento: uno che specifica una condizione e un altro che specifica un valore. Nella tabella seguente vengono illustrati due valori  possibili per l'attributo **name** e come vengono usati gli elementi dell'argomento per specificare condizioni e valori.



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
<td>Il contenuto dell'elemento <strong>argomento</strong> è la parte della condizione di una stringa di condizione. Ad esempio, nella stringa di condizione &quot; Artista Uguale a Joe , la parte della condizione è Uguale a &quot; &quot; &quot; . La parte della condizione di una stringa di condizione deve essere una delle seguenti: Uguale a, Non uguale a, Contiene, Non contiene, è minore di, è maggiore di, è maggiore di, È, Non è, è precedente, è più recente di, è più recente di, Sopra, Sotto, Crescente, Decrescente, Casuale, è almeno, non è più di.</td>
</tr>
<tr class="even">
<td>Valore</td>
<td>Il contenuto dell'elemento <strong>argomento</strong> è la parte del valore di una stringa di condizione. Ad esempio, nella stringa di condizione &quot; Artista Uguale a Joe , la parte del valore è Joe &quot; &quot; &quot; . Esempio:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals&lt;/argument&gt;
  <argument name = &quot;Value&quot;>Joe&lt;/argument&gt;
&lt;/fragment&gt;</code></pre></td>
</tr>
</tbody>
</table>



 

Quando l'attributo  **name** di un elemento frammento è "Limit Total Size To" o "Limit Total Duration To", l'elemento **frammento** deve contenere due elementi **argomento:** uno che specifica un formato e uno che specifica un numero. Nella tabella seguente vengono illustrati due valori  possibili per l'attributo **name** e come vengono usati gli elementi dell'argomento per limitare le dimensioni o la durata di una playlist.



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
<td>Quando l'attributo <strong></strong> <strong>name</strong> dell'elemento fragment è Limit Total Size To , il contenuto dell'elemento argument deve essere uno dei &quot; &quot; seguenti: <strong></strong> Kilobytes, Megabytes o Gigabytes. Quando <strong></strong> <strong></strong> l'attributo name dell'elemento fragment è Limit Total Duration To , il contenuto dell'elemento argument deve essere uno dei &quot; &quot; seguenti: Seconds, Minutes, Hours o Days. <strong></strong><br/></td>
</tr>
<tr class="even">
<td>Numero</td>
<td>Il contenuto <strong>dell'elemento argomento</strong> è un numero che limita le dimensioni o la durata della playlist. Esempi:<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes&lt;/argument&gt;
  <argument name = &quot;Number&quot;>5&lt;/argument&gt;
&lt;/fragment&gt;

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes&lt;/argument&gt;
  <argument name = &quot;Number&quot;>20&lt;/argument&gt;
&lt;/fragment&gt;</code></pre></td>
</tr>
</tbody>
</table>



 

Quando **l'attributo name** di un elemento **frammento** è "Limit  Number of Items", l'elemento **fragment** deve contenere un elemento argument che specifica il numero di elementi. Nella tabella seguente viene illustrato come usare il valore Number **dell'attributo name.**



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
  <argument name = &quot;Number&quot;>15&lt;/argument&gt;
&lt;/fragment&gt;</code></pre></td>
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

 

 





