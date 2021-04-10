---
description: Il predicato CONTAINs fa parte della clausola WHERE e supporta la ricerca di parole e frasi nelle colonne di testo.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: CONTIENE predicato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908f4c67d5c1d5bcf00c60bd8cb271928682a907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878798"
---
# <a name="contains-predicate"></a>CONTIENE predicato

Il predicato CONTAINs fa parte della clausola WHERE e supporta la ricerca di parole e frasi nelle colonne di testo. Il predicato CONTAINs include funzionalità per la corrispondenza delle parole, la corrispondenza di forme flessori di parole, la ricerca tramite caratteri jolly e la ricerca con prossimità. È anche possibile applicare pesi in un predicato CONTAINs per impostare l'importanza delle colonne in cui viene trovato il termine di ricerca. Il predicato CONTAINs è più adatto per corrispondenze esatte, a differenza del predicato [FREETEXT](-search-sql-freetext.md) , che è più adatto per individuare documenti contenenti combinazioni di parole di ricerca distribuite in tutta la colonna. Le ricerche non rilevano la distinzione tra maiuscole e minuscole.

Di seguito è riportata la sintassi di base del predicato CONTAINs:

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

Il riferimento alla colonna full-text \_ è facoltativo. Con esso, è possibile limitare la ricerca a una singola colonna o a un gruppo di colonne rispetto al quale viene testato il predicato CONTAINs. Quando la colonna full-text viene specificata come "ALL" o " \* ", viene eseguita la ricerca di tutte le proprietà di testo indicizzato. Sebbene non sia necessario che la colonna sia una proprietà di testo, i risultati potrebbero non essere significativi se la colonna è un altro tipo di dati. Il nome della colonna può essere un [identificatore](-search-sql-identifiers.md)regolare o delimitato ed è necessario separarlo dalla condizione con una virgola. Se non viene specificata alcuna colonna full-text, viene usata la colonna System. search. Contents, che è il corpo del documento.

La parte LCID del predicato specifica le impostazioni locali di ricerca. Indica al motore di ricerca di usare il Word breaker e i moduli flessivi appropriati per la query di ricerca. Per specificare le impostazioni locali, fornire l'identificatore del codice lingua (LCID) di Windows standard. Ad esempio, 1033 è il LCID per Stati Uniti-English. Posizionare il LCID come ultimo elemento all'interno delle parentesi della clausola CONTAINs. Per informazioni importanti sulla ricerca e sui linguaggi, vedere [uso delle ricerche localizzate](-search-sql-usinglocsearches.md).

> [!NOTE]  
> Le impostazioni locali di ricerca predefinite sono le impostazioni locali predefinite del sistema.

La parte della condizione Contains \_ deve essere racchiusa tra virgolette singole per le singole parole o virgolette doppie per le frasi ed è costituita da uno o più termini di ricerca del contenuto combinati usando gli operatori logici **and** o **or**. È possibile utilizzare l'operatore unario facoltativo **non** dopo un operatore **and** per negare il valore logico di un termine di ricerca del contenuto.

> [!NOTE]  
> L'operatore **not** può verificarsi solo dopo **e**. Non è possibile usare l'operatore **not** se è presente solo una condizione di corrispondenza o dopo l'operatore **or** .

È possibile usare le parentesi per raggruppare e annidare i termini di ricerca del contenuto. Nella tabella seguente viene descritto l'ordine di precedenza per gli operatori logici.

| Ordine (precedenza) | Operatore logico |
|--------------------|------------------|
| Primo (massimo)    | **NOT**          |
| Second             | **AND**          |
| Terzo (minimo)     | **OR**           |

Gli operatori logici dello stesso tipo sono associativi e non esiste alcun ordine di calcolo specificato. Ad esempio, (A **e** B) **e** (c **e** d) possono essere calcolati (B **e** C) **e** (a **e** d) senza alcuna modifica nel risultato logico.

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
<td>Una singola parola senza spazi o altra punteggiatura. Le virgolette doppie non sono necessarie.</td>
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
<td>Nome della colonna di proprietà rispetto al quale trovare la corrispondenza con la query rimanente.</td>
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
<td>Parole, frasi e stringhe con caratteri jolly combinate tramite gli operatori booleani <strong>and</strong>, <strong>or</strong>o <strong>not</strong>. Racchiudere i termini booleani racchiusi tra virgolette doppie.</td>
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
<td>Parole, frasi o caratteri jolly separati dalla funzione accanto a. Per ulteriori informazioni, vedere <a href="-search-sql-near.md">Near Term</a>.</td>
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
<td>Corrisponde a una parola e alle versioni flessori di tale parola. Per ulteriori informazioni, vedere <a href="-search-sql-formsof.md">FORMSOF term</a>.</td>
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
<td>Combina i risultati della corrispondenza su più parole, frasi o termini di ricerca con caratteri jolly. Ogni termine di ricerca può essere ponderato facoltativamente. È possibile specificare facoltativamente il metodo di calcolo della pertinenza, che combina i pesi e il numero di elementi corrispondenti al documento. Per ulteriori informazioni, vedere la pagina relativa al <a href="-search-sql-isabout.md">termine</a>.</td>
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

- [Utilizzo di caratteri jolly nel predicato CONTAINs](-search-sql-wildcards.md)
- [Termine FORMSOF](-search-sql-formsof.md)
- [Termini](-search-sql-isabout.md)
- [A breve termine](-search-sql-near.md)

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[Clausola WHERE](-search-sql-where.md)

### <a name="conceptual"></a>Informazioni concettuali

[Predicati full-text](-search-sql-fulltextpredicates.md)

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
