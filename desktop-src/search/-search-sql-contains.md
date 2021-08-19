---
description: Il predicato CONTAINS fa parte della clausola WHERE e supporta la ricerca di parole e frasi nelle colonne di testo.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: Predicato CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c821431bb5f00319fe47414dcce5240775f2ce78335998c1bb30b84dc9fe17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863714"
---
# <a name="contains-predicate"></a>Predicato CONTAINS

Il predicato CONTAINS fa parte della clausola WHERE e supporta la ricerca di parole e frasi nelle colonne di testo. Il predicato CONTAINS include funzionalità per la corrispondenza delle parole, la corrispondenza di forme gonfie di parole, la ricerca con caratteri jolly e la ricerca tramite prossimità. È anche possibile applicare pesi in un predicato CONTAINS per impostare l'importanza delle colonne in cui viene trovato il termine di ricerca. Il predicato CONTAINS è più adatto per le corrispondenze esatte, a differenza del predicato [FREETEXT,](-search-sql-freetext.md) più adatto per trovare documenti contenenti combinazioni di parole di ricerca distribuite in tutta la colonna. Le ricerche non rilevano la distinzione tra maiuscole e minuscole.

Di seguito è riportata la sintassi di base del predicato CONTAINS:

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

Il riferimento alla \_ colonna full-text è facoltativo. È possibile limitare la ricerca a una singola colonna o a un gruppo di colonne in base al quale viene testato il predicato CONTAINS. Quando la colonna full-text viene specificata come "ALL" o "", viene cercata tutte le proprietà del testo \* indicizzato. Anche se la colonna non deve essere una proprietà di testo, i risultati potrebbero non avere significato se la colonna è un altro tipo di dati. Il nome della colonna può essere [](-search-sql-identifiers.md)un identificatore normale o delimitato ed è necessario separarlo dalla condizione con una virgola. Se non viene specificata alcuna colonna full-text, viene utilizzata la colonna System.Search.Contents, ovvero il corpo del documento.

La parte LCID del predicato specifica le impostazioni locali di ricerca. Questo indica al motore di ricerca di usare il word breaker e i moduli gonfiali appropriati per la query di ricerca. Per specificare le impostazioni locali, specificare l'Windows LCID (Standard Language Code Identifier). Ad esempio, 1033 è l'LCID per Stati Uniti-inglese. Inserire l'LCID come ultimo elemento all'interno delle parentesi della clausola CONTAINS. Per informazioni importanti sulla ricerca e sulle lingue, vedere [Uso delle ricerche localizzate.](-search-sql-usinglocsearches.md)

> [!NOTE]  
> Le impostazioni locali di ricerca predefinite sono le impostazioni locali predefinite del sistema.

La parte contains condition deve essere racchiusa tra virgolette singole per singole parole o virgolette doppie per le frasi ed è costituita da uno o più termini di ricerca del contenuto combinati usando gli operatori logici \_ **AND** **o OR**. È possibile usare l'operatore unario **facoltativo NOT** dopo un **operatore AND** per negare il valore logico di un termine di ricerca contenuto.

> [!NOTE]  
> L'operatore **NOT** può verificarsi solo dopo **AND**. Non è possibile usare **l'operatore NOT** se è presente una sola condizione di corrispondenza o dopo **l'operatore OR.**

È possibile usare le parentesi per raggruppare e annidare i termini di ricerca del contenuto. Nella tabella seguente viene descritto l'ordine di precedenza per gli operatori logici.

| Order (precedenza) | Operatore logico |
|--------------------|------------------|
| Primo (più alto)    | **NOT**          |
| Secondo             | **AND**          |
| Terzo (più basso)     | **OR**           |

Gli operatori logici dello stesso tipo sono associativi e non esiste un ordine di calcolo specificato. Ad esempio, (A **AND** B) **AND** (C **AND** D) può essere calcolato (B **AND** C) **AND** (A **AND** D) senza alcuna modifica nel risultato logico.

Nella tabella seguente vengono descritti i tipi di termini di ricerca del contenuto.

<!-- markdownlint-disable MD033 -->
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
<td>Singola parola senza spazi o altri segni di punteggiatura. Le virgolette doppie non sono necessarie.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
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
(&#39;&quot;computer software&quot;&#39;)

Or, to use a double quote mark:

... WHERE CONTAINS
(&#39;&quot;computer &quot;&quot;science&quot;&quot; &quot;&#39;)</code></pre></td>
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
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;compu*&quot;&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;,
&quot;computation&quot;, and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Colonna full-text</td>
<td>Nome della colonna della proprietà rispetto al quale trovare la corrispondenza con la query rimanente.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (System.Author,&#39;&quot;James&quot; OR &quot;Juan&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Boolean</td>
<td>Parole, frasi e stringhe con caratteri jolly combinate usando gli operatori <strong>booleani AND</strong>, <strong>OR</strong>o <strong>NOT</strong>. Racchiudere i termini booleani tra virgolette doppie.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer monitor&quot; AND
  &quot;software program&quot; AND
  &quot;install component&quot;&#39;)

...WHERE CONTAINS
 (&#39; &quot;computer&quot; AND
  &quot;software&quot; AND
  &quot;install&quot; &#39; )

...WHERE CONTAINS
(&#39;&quot;computer software install&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Near</td>
<td>Parole, frasi o caratteri jolly separati dalla funzione NEAR. Per altre informazioni, vedere <a href="-search-sql-near.md">NEAR Term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer&quot; NEAR &quot;software&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>FormsOf</td>
<td>Corrisponde a una parola e alle versioni inflessizionali di tale parola. Per altre informazioni, vedere <a href="-search-sql-formsof.md">FORMSOF Term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;FORMSOF
 (INFLECTIONAL, &quot;happy&quot;))

Matches &quot;happy&quot;, &quot;happier&quot;,
&quot;happiest&quot;, &quot;happily&quot;, and so on.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>IsAbout</td>
<td>Combina i risultati corrispondenti su più parole, frasi o termini di ricerca con caratteri jolly. Ogni termine di ricerca può essere ponderato facoltativamente. Facoltativamente, è possibile specificare il metodo di calcolo della classificazione, che combina i pesi e il numero di elementi corrispondenti al documento. Per altre informazioni, vedere <a href="-search-sql-isabout.md">Termine ISABOUT</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;ISABOUT ( &quot;computer&quot; WEIGHT (0.75) ,
    &quot;software&quot; WEIGHT (0.25) ,
    &quot;development&quot; WEIGHT (0.255)
 ) RANKMETHOD INNER PRODUCT
&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

Questa sezione include gli argomenti seguenti:

- [Uso di caratteri jolly nel predicato CONTAINS](-search-sql-wildcards.md)
- [Termine FORMSOF](-search-sql-formsof.md)
- [Termine ISABOUT](-search-sql-isabout.md)
- [NEAR Term](-search-sql-near.md)

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[Clausola WHERE](-search-sql-where.md)

### <a name="conceptual"></a>Informazioni concettuali

[Predicati full-text](-search-sql-fulltextpredicates.md)

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
