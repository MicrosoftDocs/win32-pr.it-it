---
description: Il termine outabout corrisponde alle colonne rispetto a un gruppo di uno o più termini di ricerca.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: Termini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f79fc2fa4a56b3ca6b3b412141f096b282e3aa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750383"
---
# <a name="isabout-term"></a>Termini

**Deprecato**

Questa funzionalità è stata rimossa a partire da Windows 8. Se si scrivono nuove applicazioni, evitare di utilizzare questa funzionalità deprecata. Se si modificano le applicazioni esistenti, si consiglia vivamente di rimuovere qualsiasi dipendenza da questa funzionalità.

Il termine outabout corrisponde alle colonne rispetto a un gruppo di uno o più termini di ricerca. Ha la sintassi seguente:


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



Il termine facoltativo RANKMETHOD specifica il metodo di calcolo utilizzato per classificare i documenti che corrispondono a uno o più componenti. Se non viene specificato alcun RANKMETHOD, viene usato il metodo di classificazione del coefficiente Jaccard predefinito.

Il termine dell'espressione può avere uno o più componenti. Le colonne specificate nel predicato [Contains](-search-sql-contains.md) vengono verificate in base a ogni componente. Il documento viene incluso nei risultati se almeno uno dei componenti corrisponde a. Virgole separate da più componenti.

La parte del componente presenta la sintassi seguente:


```
<match_term> [<weight_term>]
```



È possibile utilizzare il termine di peso facoltativo per modificare l'importanza relativa di ogni termine nel termine. Se non viene applicato alcun termine di peso, viene implicito il peso predefinito di 1,0.

Nella tabella seguente vengono descritti i possibili tipi di termini delle corrispondenze.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td>Una singola parola senza spazi o altra punteggiatura.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<col style="width: 100%" />
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
<td>Parole o frasi con l'asterisco (*) aggiunto alla fine. Per ulteriori informazioni, vedere <a href="-search-sql-wildcards.md">utilizzo dei caratteri jolly nel predicato CONTAINS</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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



 

## <a name="isabout-column-weighting"></a>Informazioni sulla ponderazione delle colonne

Il termine noabout classifica i documenti corrispondenti in base alla precisione di ogni documento corrispondente al set di termini di corrispondenza nella query. È possibile usare la ponderazione delle colonne per inserire più importanza nella corrispondenza di alcuni termini di corrispondenza rispetto ad altri. È possibile applicare un valore di peso a ogni termine delle corrispondenze del termine di ricerca. Il peso viene applicato a un singolo termine di corrispondenza ed è indicato dalla parola chiave "WEIGHT". Il termine WEIGHT presenta due sintassi alternative:


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



Il valore del peso deve essere compreso tra 0 e 1,0, con non più di tre posizioni decimali. Se si specifica un valore di peso al di fuori di questo intervallo, viene restituito un messaggio di errore. Il valore di classificazione non ponderato per un termine viene moltiplicato per il valore del peso per il termine.

Se per un termine di corrispondenza non viene specificato alcun peso, viene implicato il valore predefinito 1,0.

### <a name="example"></a>Esempio

Nell'esempio seguente vengono applicati i pesi ai due termini di corrispondenza, usando la sintassi Long e short per i valori di peso.


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

 

 



