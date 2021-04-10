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
# <a name="contains-predicate"></a><span data-ttu-id="ca828-103">CONTIENE predicato</span><span class="sxs-lookup"><span data-stu-id="ca828-103">CONTAINS Predicate</span></span>

<span data-ttu-id="ca828-104">Il predicato CONTAINs fa parte della clausola WHERE e supporta la ricerca di parole e frasi nelle colonne di testo.</span><span class="sxs-lookup"><span data-stu-id="ca828-104">The CONTAINS predicate is part of the WHERE clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="ca828-105">Il predicato CONTAINs include funzionalità per la corrispondenza delle parole, la corrispondenza di forme flessori di parole, la ricerca tramite caratteri jolly e la ricerca con prossimità.</span><span class="sxs-lookup"><span data-stu-id="ca828-105">The CONTAINS predicate has features for matching words, matching inflectional forms of words, searching using wildcard characters, and searching using proximity.</span></span> <span data-ttu-id="ca828-106">È anche possibile applicare pesi in un predicato CONTAINs per impostare l'importanza delle colonne in cui viene trovato il termine di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ca828-106">You can also apply weights in a CONTAINS predicate to set the importance of the columns where the search term is found.</span></span> <span data-ttu-id="ca828-107">Il predicato CONTAINs è più adatto per corrispondenze esatte, a differenza del predicato [FREETEXT](-search-sql-freetext.md) , che è più adatto per individuare documenti contenenti combinazioni di parole di ricerca distribuite in tutta la colonna.</span><span class="sxs-lookup"><span data-stu-id="ca828-107">The CONTAINS predicate is better suited for exact matches, in contrast to the [FREETEXT](-search-sql-freetext.md) predicate, which is better suited to finding documents containing combinations of the search words spread throughout the column.</span></span> <span data-ttu-id="ca828-108">Le ricerche non rilevano la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ca828-108">Searches are not case-sensitive.</span></span>

<span data-ttu-id="ca828-109">Di seguito è riportata la sintassi di base del predicato CONTAINs:</span><span class="sxs-lookup"><span data-stu-id="ca828-109">The following is the basic syntax of the CONTAINS predicate:</span></span>

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

<span data-ttu-id="ca828-110">Il riferimento alla colonna full-text \_ è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ca828-110">The fulltext\_column reference is optional.</span></span> <span data-ttu-id="ca828-111">Con esso, è possibile limitare la ricerca a una singola colonna o a un gruppo di colonne rispetto al quale viene testato il predicato CONTAINs.</span><span class="sxs-lookup"><span data-stu-id="ca828-111">With it, you can limit the search to a single column or a column group against which the CONTAINS predicate is tested.</span></span> <span data-ttu-id="ca828-112">Quando la colonna full-text viene specificata come "ALL" o " \* ", viene eseguita la ricerca di tutte le proprietà di testo indicizzato.</span><span class="sxs-lookup"><span data-stu-id="ca828-112">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="ca828-113">Sebbene non sia necessario che la colonna sia una proprietà di testo, i risultati potrebbero non essere significativi se la colonna è un altro tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="ca828-113">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="ca828-114">Il nome della colonna può essere un [identificatore](-search-sql-identifiers.md)regolare o delimitato ed è necessario separarlo dalla condizione con una virgola.</span><span class="sxs-lookup"><span data-stu-id="ca828-114">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="ca828-115">Se non viene specificata alcuna colonna full-text, viene usata la colonna System. search. Contents, che è il corpo del documento.</span><span class="sxs-lookup"><span data-stu-id="ca828-115">If no fulltext column is specified, the System.Search.Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="ca828-116">La parte LCID del predicato specifica le impostazioni locali di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ca828-116">The LCID portion of the predicate specifies the search locale.</span></span> <span data-ttu-id="ca828-117">Indica al motore di ricerca di usare il Word breaker e i moduli flessivi appropriati per la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ca828-117">This instructs the search engine to use the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="ca828-118">Per specificare le impostazioni locali, fornire l'identificatore del codice lingua (LCID) di Windows standard.</span><span class="sxs-lookup"><span data-stu-id="ca828-118">To specify the locale, provide the Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="ca828-119">Ad esempio, 1033 è il LCID per Stati Uniti-English.</span><span class="sxs-lookup"><span data-stu-id="ca828-119">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="ca828-120">Posizionare il LCID come ultimo elemento all'interno delle parentesi della clausola CONTAINs.</span><span class="sxs-lookup"><span data-stu-id="ca828-120">Place the LCID as the last item inside the parentheses of the CONTAINS clause.</span></span> <span data-ttu-id="ca828-121">Per informazioni importanti sulla ricerca e sui linguaggi, vedere [uso delle ricerche localizzate](-search-sql-usinglocsearches.md).</span><span class="sxs-lookup"><span data-stu-id="ca828-121">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="ca828-122">Le impostazioni locali di ricerca predefinite sono le impostazioni locali predefinite del sistema.</span><span class="sxs-lookup"><span data-stu-id="ca828-122">The default search locale is the system default locale.</span></span>

<span data-ttu-id="ca828-123">La parte della condizione Contains \_ deve essere racchiusa tra virgolette singole per le singole parole o virgolette doppie per le frasi ed è costituita da uno o più termini di ricerca del contenuto combinati usando gli operatori logici **and** o **or**.</span><span class="sxs-lookup"><span data-stu-id="ca828-123">The contains\_condition portion must be enclosed in single quotation marks for single words or double quotation marks for phrases, and consists of one or more content search terms that are combined using the logical operators **AND** or **OR**.</span></span> <span data-ttu-id="ca828-124">È possibile utilizzare l'operatore unario facoltativo **non** dopo un operatore **and** per negare il valore logico di un termine di ricerca del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ca828-124">You can use the optional unary operator **NOT** after an **AND** operator to negate the logical value of a content search term.</span></span>

> [!NOTE]  
> <span data-ttu-id="ca828-125">L'operatore **not** può verificarsi solo dopo **e**.</span><span class="sxs-lookup"><span data-stu-id="ca828-125">The **NOT** operator can occur only after **AND**.</span></span> <span data-ttu-id="ca828-126">Non è possibile usare l'operatore **not** se è presente solo una condizione di corrispondenza o dopo l'operatore **or** .</span><span class="sxs-lookup"><span data-stu-id="ca828-126">You cannot use the **NOT** operator if there is only one match condition, or after the **OR** operator.</span></span>

<span data-ttu-id="ca828-127">È possibile usare le parentesi per raggruppare e annidare i termini di ricerca del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ca828-127">You can use parentheses to group and nest content search terms.</span></span> <span data-ttu-id="ca828-128">Nella tabella seguente viene descritto l'ordine di precedenza per gli operatori logici.</span><span class="sxs-lookup"><span data-stu-id="ca828-128">The following table describes the order of precedence for the logical operators.</span></span>

| <span data-ttu-id="ca828-129">Ordine (precedenza)</span><span class="sxs-lookup"><span data-stu-id="ca828-129">Order (precedence)</span></span> | <span data-ttu-id="ca828-130">Operatore logico</span><span class="sxs-lookup"><span data-stu-id="ca828-130">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="ca828-131">Primo (massimo)</span><span class="sxs-lookup"><span data-stu-id="ca828-131">First (highest)</span></span>    | <span data-ttu-id="ca828-132">**NOT**</span><span class="sxs-lookup"><span data-stu-id="ca828-132">**NOT**</span></span>          |
| <span data-ttu-id="ca828-133">Second</span><span class="sxs-lookup"><span data-stu-id="ca828-133">Second</span></span>             | <span data-ttu-id="ca828-134">**AND**</span><span class="sxs-lookup"><span data-stu-id="ca828-134">**AND**</span></span>          |
| <span data-ttu-id="ca828-135">Terzo (minimo)</span><span class="sxs-lookup"><span data-stu-id="ca828-135">Third (lowest)</span></span>     | <span data-ttu-id="ca828-136">**OR**</span><span class="sxs-lookup"><span data-stu-id="ca828-136">**OR**</span></span>           |

<span data-ttu-id="ca828-137">Gli operatori logici dello stesso tipo sono associativi e non esiste alcun ordine di calcolo specificato.</span><span class="sxs-lookup"><span data-stu-id="ca828-137">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="ca828-138">Ad esempio, (A **e** B) **e** (c **e** d) possono essere calcolati (B **e** C) **e** (a **e** d) senza alcuna modifica nel risultato logico.</span><span class="sxs-lookup"><span data-stu-id="ca828-138">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (B **AND** C) **AND** (A **AND** D) with no change in the logical result.</span></span>

<span data-ttu-id="ca828-139">Nella tabella seguente vengono descritti i tipi di termini di ricerca del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ca828-139">The following table describes the types of content search terms.</span></span>

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca828-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca828-140">Type</span></span></th>
<th><span data-ttu-id="ca828-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca828-141">Description</span></span></th>
<th><span data-ttu-id="ca828-142">Esempi</span><span class="sxs-lookup"><span data-stu-id="ca828-142">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca828-143">Word</span><span class="sxs-lookup"><span data-stu-id="ca828-143">Word</span></span></td>
<td><span data-ttu-id="ca828-144">Una singola parola senza spazi o altra punteggiatura.</span><span class="sxs-lookup"><span data-stu-id="ca828-144">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="ca828-145">Le virgolette doppie non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="ca828-145">Double quotation marks are not necessary.</span></span></td>
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
<td><span data-ttu-id="ca828-146">Frase</span><span class="sxs-lookup"><span data-stu-id="ca828-146">Phrase</span></span></td>
<td><span data-ttu-id="ca828-147">Più parole o spazi inclusi.</span><span class="sxs-lookup"><span data-stu-id="ca828-147">Multiple words or included spaces.</span></span></td>
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
<td><span data-ttu-id="ca828-148">Wildcard (Carattere jolly)</span><span class="sxs-lookup"><span data-stu-id="ca828-148">Wildcard</span></span></td>
<td><span data-ttu-id="ca828-149">Parole o frasi con l'asterisco (\*) aggiunto alla fine.</span><span class="sxs-lookup"><span data-stu-id="ca828-149">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="ca828-150">Per ulteriori informazioni, vedere <a href="-search-sql-wildcards.md">utilizzo dei caratteri jolly nel predicato CONTAINS</a>.</span><span class="sxs-lookup"><span data-stu-id="ca828-150">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
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
<td><span data-ttu-id="ca828-151">Colonna full-text</span><span class="sxs-lookup"><span data-stu-id="ca828-151">Full-text Column</span></span></td>
<td><span data-ttu-id="ca828-152">Nome della colonna di proprietà rispetto al quale trovare la corrispondenza con la query rimanente.</span><span class="sxs-lookup"><span data-stu-id="ca828-152">A property column name against which to match the remaining query.</span></span></td>
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
<td><span data-ttu-id="ca828-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="ca828-153">Boolean</span></span></td>
<td><span data-ttu-id="ca828-154">Parole, frasi e stringhe con caratteri jolly combinate tramite gli operatori booleani <strong>and</strong>, <strong>or</strong>o <strong>not</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca828-154">Words, phrases, and wildcard strings combined by using the Boolean operators <strong>AND</strong>, <strong>OR</strong>, or <strong>NOT</strong>.</span></span> <span data-ttu-id="ca828-155">Racchiudere i termini booleani racchiusi tra virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="ca828-155">Enclose the Boolean terms in double quotation marks.</span></span></td>
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
<td><span data-ttu-id="ca828-156">Near</span><span class="sxs-lookup"><span data-stu-id="ca828-156">Near</span></span></td>
<td><span data-ttu-id="ca828-157">Parole, frasi o caratteri jolly separati dalla funzione accanto a.</span><span class="sxs-lookup"><span data-stu-id="ca828-157">Words, phrases, or wildcards separated by the function NEAR.</span></span> <span data-ttu-id="ca828-158">Per ulteriori informazioni, vedere <a href="-search-sql-near.md">Near Term</a>.</span><span class="sxs-lookup"><span data-stu-id="ca828-158">For more information, see <a href="-search-sql-near.md">NEAR Term</a>.</span></span></td>
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
<td><span data-ttu-id="ca828-159">FormsOf</span><span class="sxs-lookup"><span data-stu-id="ca828-159">FormsOf</span></span></td>
<td><span data-ttu-id="ca828-160">Corrisponde a una parola e alle versioni flessori di tale parola.</span><span class="sxs-lookup"><span data-stu-id="ca828-160">Matches a word and the inflectional versions of that word.</span></span> <span data-ttu-id="ca828-161">Per ulteriori informazioni, vedere <a href="-search-sql-formsof.md">FORMSOF term</a>.</span><span class="sxs-lookup"><span data-stu-id="ca828-161">For more information, see <a href="-search-sql-formsof.md">FORMSOF Term</a>.</span></span></td>
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
<td><span data-ttu-id="ca828-162">IsAbout</span><span class="sxs-lookup"><span data-stu-id="ca828-162">IsAbout</span></span></td>
<td><span data-ttu-id="ca828-163">Combina i risultati della corrispondenza su più parole, frasi o termini di ricerca con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="ca828-163">Combines matching results over multiple word, phrase, or wildcard search terms.</span></span> <span data-ttu-id="ca828-164">Ogni termine di ricerca può essere ponderato facoltativamente.</span><span class="sxs-lookup"><span data-stu-id="ca828-164">Each search term can optionally be weighted.</span></span> <span data-ttu-id="ca828-165">È possibile specificare facoltativamente il metodo di calcolo della pertinenza, che combina i pesi e il numero di elementi corrispondenti al documento.</span><span class="sxs-lookup"><span data-stu-id="ca828-165">You can optionally specify the rank calculation method, which combines the weights and how many of the items the document matches.</span></span> <span data-ttu-id="ca828-166">Per ulteriori informazioni, vedere la pagina relativa al <a href="-search-sql-isabout.md">termine</a>.</span><span class="sxs-lookup"><span data-stu-id="ca828-166">For more information, see <a href="-search-sql-isabout.md">ISABOUT Term</a>.</span></span></td>
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

<span data-ttu-id="ca828-167">Questa sezione include gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca828-167">This section includes the following topics:</span></span>

- [<span data-ttu-id="ca828-168">Utilizzo di caratteri jolly nel predicato CONTAINs</span><span class="sxs-lookup"><span data-stu-id="ca828-168">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
- [<span data-ttu-id="ca828-169">Termine FORMSOF</span><span class="sxs-lookup"><span data-stu-id="ca828-169">FORMSOF Term</span></span>](-search-sql-formsof.md)
- [<span data-ttu-id="ca828-170">Termini</span><span class="sxs-lookup"><span data-stu-id="ca828-170">ISABOUT Term</span></span>](-search-sql-isabout.md)
- [<span data-ttu-id="ca828-171">A breve termine</span><span class="sxs-lookup"><span data-stu-id="ca828-171">NEAR Term</span></span>](-search-sql-near.md)

## <a name="related-topics"></a><span data-ttu-id="ca828-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca828-172">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="ca828-173">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ca828-173">Reference</span></span>

[<span data-ttu-id="ca828-174">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="ca828-174">WHERE Clause</span></span>](-search-sql-where.md)

### <a name="conceptual"></a><span data-ttu-id="ca828-175">Informazioni concettuali</span><span class="sxs-lookup"><span data-stu-id="ca828-175">Conceptual</span></span>

[<span data-ttu-id="ca828-176">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="ca828-176">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)

[<span data-ttu-id="ca828-177">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="ca828-177">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
