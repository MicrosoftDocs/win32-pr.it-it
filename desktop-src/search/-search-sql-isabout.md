---
description: Il termine ISABOUT corrisponde alle colonne rispetto a un gruppo di uno o più termini di ricerca.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: Termine ISABOUT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee772bbd3be1f9ef3924989dfbaa2a9afd77d4a6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627357"
---
# <a name="isabout-term"></a>Termine ISABOUT

**Deprecato**

Questa funzionalità è stata rimossa a Windows 8. Se si scrivono nuove applicazioni, evitare di usare questa funzionalità deprecata. Se si modificano applicazioni esistenti, è consigliabile rimuovere qualsiasi dipendenza da questa funzionalità.

Il termine ISABOUT corrisponde alle colonne rispetto a un gruppo di uno o più termini di ricerca. Ha la sintassi seguente:


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



Il termine RANKMETHOD facoltativo specifica il metodo di calcolo usato per classificare i documenti che corrispondono a uno o più componenti. Se non viene specificato ALCUN RANKMETHOD, viene usato il metodo di classificazione predefinito Coefficiente Jaccard.

Il termine ISABOUT può avere uno o più componenti. Le colonne specificate nel predicato [CONTAINS](-search-sql-contains.md) vengono testate in base a ogni componente. Il documento viene incluso nei risultati se almeno uno dei componenti corrisponde. Le virgole separano più componenti.

La parte del componente ha la sintassi seguente:


```
<match_term> [<weight_term>]
```



È possibile usare il termine WEIGHT facoltativo per modificare l'importanza relativa di ogni termine all'interno del termine ISABOUT. Se non viene applicato alcun termine di peso, il peso predefinito 1,0 è implicito.

Nella tabella seguente vengono descritti i possibili tipi di termini di corrispondenza.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descrizione</th>
<th>Esempi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Word</td>
<td>Singola parola senza spazi o altri segni di punteggiatura.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer&quot;,&quot;software&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Frase</td>
<td>Più parole o spazi inclusi.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer software&quot;,&quot;hardware&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Wildcard (Carattere jolly)</td>
<td>Parole o frasi con l'asterisco (*) aggiunto alla fine. Per altre informazioni, vedere <a href="-search-sql-wildcards.md">Uso di caratteri jolly nel predicato CONTAINS</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;compu*&quot;,&quot;soft*&quot;)&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;, &quot;computation&quot;, 
and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="isabout-column-weighting"></a>Ponderazione delle colonne ISABOUT

Il termine ISABOUT classifica i documenti corrispondenti in base alla corrispondenza tra ogni documento e il set di termini di corrispondenza nella query. È possibile usare la ponderazione delle colonne per inserire maggiore importanza nella corrispondenza di alcuni termini di corrispondenza rispetto ad altri. A ogni termine di corrispondenza nel termine ISABOUT può essere applicato un valore di peso. Il peso viene applicato a un singolo termine di corrispondenza ed è indicato dalla parola chiave "WEIGHT". Il termine WEIGHT ha due sintassi alternative:


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



Il valore del peso deve essere compreso tra 0 e 1,0, senza più di tre cifre decimali. Se si specifica un valore di peso esterno a questo intervallo, viene visualizzato un messaggio di errore. Il valore di classificazione non ponderato per un termine viene moltiplicato per il valore del peso per il termine.

Se non viene specificato alcun peso per un termine di corrispondenza, il valore predefinito, 1.0, è implicito.

### <a name="example"></a>Esempio

L'esempio seguente applica i pesi ai due termini di corrispondenza ISABOUT, usando sia la sintassi lunga che la sintassi breve per i valori di peso.


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Predicato FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> </dl>

 

 



