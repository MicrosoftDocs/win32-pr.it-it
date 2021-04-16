---
description: Il termine NEAR viene usato per specificare che due termini di ricerca del contenuto devono essere relativamente vicini tra loro per essere riconosciuti come corrispondenti per il predicato CONTAINs.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: A breve termine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342956"
---
# <a name="near-term"></a>A breve termine

Il termine NEAR viene usato per specificare che due termini di ricerca del contenuto devono essere relativamente vicini tra loro per essere riconosciuti come corrispondenti per il predicato [Contains](-search-sql-contains.md) .

La sintassi per il termine vicino è la seguente:


```
<content_search_term> NEAR | ~ <content_search_term>
```



Il termine NEAR può essere rappresentato dalla parola chiave "NEAR" o da una tilde (~).

Quando le parole unite accanto alla query vengono trovate all'interno di circa 50 parole tra loro all'interno della colonna in cui viene eseguita la ricerca, il termine vicino restituisce una corrispondenza. Più vicine sono le due parole, maggiore è il numero di dimensioni calcolato per il breve termine. Oltre alle due parole, minore è il rango.

> [!Note]  
> Il numero di parole tra i termini di ricerca trovati è approssimativo e dipende dall'aspetto delle parole non significative, ad esempio "a" o "The", e come wordbreaker tokenize testo. Può essere minore di 50.

 


Nella tabella seguente vengono descritti i tipi di termini di ricerca di contenuto che possono essere utilizzati con un predicato CONTAINs in un breve termine.



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
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> Se le parole corrispondenti specificate con il termine NEAR si trovano nella colonna cercata, ma sono più lontane di 50 parole, il risultato viene comunque restituito, ma ha un [rango](-search-sql-understandingrelevancevalues.md) pari a 0.

 

### <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato il concatenamento dei termini NEAR, usando le forme brevi e lunghe del termine:


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Utilizzo di caratteri jolly nel predicato CONTAINs](-search-sql-wildcards.md)
</dt> </dl>

 

 



