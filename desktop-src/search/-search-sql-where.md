---
description: Le condizioni che determinano se un documento viene incluso nei risultati restituiti dalla query vengono specificate dalla clausola WHERE.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: Clausola WHERE (ricerca di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45a37334d656b0a321abdcdd4a5d045eb9d4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306108"
---
# <a name="where-clause-windows-search"></a><span data-ttu-id="da8ce-103">Clausola WHERE (ricerca di Windows)</span><span class="sxs-lookup"><span data-stu-id="da8ce-103">WHERE Clause (Windows Search)</span></span>

<span data-ttu-id="da8ce-104">Le condizioni che determinano se un documento viene incluso nei risultati restituiti dalla query vengono specificate dalla clausola WHERE.</span><span class="sxs-lookup"><span data-stu-id="da8ce-104">The conditions that determine whether a document is included in the results returned by the query are specified by the WHERE clause.</span></span> <span data-ttu-id="da8ce-105">Al livello più alto, esistono due parti della sintassi della clausola WHERE:</span><span class="sxs-lookup"><span data-stu-id="da8ce-105">At the highest level, there are two parts to the WHERE clause syntax:</span></span>


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



<span data-ttu-id="da8ce-106">L'alias facoltativo del gruppo di <\_> parte della clausola semplifica le query complesse assegnando un alias a un gruppo di una o più colonne.</span><span class="sxs-lookup"><span data-stu-id="da8ce-106">The optional <group\_alias> portion of the clause simplifies complex queries by assigning an alias to a group of one or more columns.</span></span> <span data-ttu-id="da8ce-107">Questo può migliorare la leggibilità di query complesse che cercano le stesse informazioni in più colonne specificate dagli URL.</span><span class="sxs-lookup"><span data-stu-id="da8ce-107">This can improve the readability of complex queries that search for the same information across multiple columns specified by URLs.</span></span> <span data-ttu-id="da8ce-108">Per ulteriori informazioni sugli alias di gruppo, vedere [con il predicato alias gruppo As](-search-sql-with-as.md).</span><span class="sxs-lookup"><span data-stu-id="da8ce-108">For more information about group aliases, see [WITH -- AS Group Alias Predicate](-search-sql-with-as.md).</span></span>

<span data-ttu-id="da8ce-109">La <search condition> parte della clausola WHERE è uno o più predicati di ricerca che specificano i criteri di corrispondenza per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="da8ce-109">The <search condition> portion of the WHERE clause is one or more search predicates that specify matching criteria for the search.</span></span> <span data-ttu-id="da8ce-110">I predicati di ricerca sono espressioni che asseriscono un certo valore.</span><span class="sxs-lookup"><span data-stu-id="da8ce-110">Search predicates are expressions that assert some fact about some value.</span></span>

<span data-ttu-id="da8ce-111">Il risultato di una condizione di ricerca è un valore booleano, **true** se il documento soddisfa le condizioni di ricerca specificate; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="da8ce-111">The result of a search condition is a Boolean value, either **TRUE** if the document meets the specified search conditions, or **FALSE** if it does not.</span></span> <span data-ttu-id="da8ce-112">Se il risultato è **true**, viene restituito il documento.</span><span class="sxs-lookup"><span data-stu-id="da8ce-112">If the result is **TRUE**, the document is returned.</span></span> <span data-ttu-id="da8ce-113">Se il risultato è **false**, il documento non viene restituito.</span><span class="sxs-lookup"><span data-stu-id="da8ce-113">If the result is **FALSE**, the document is not returned.</span></span> <span data-ttu-id="da8ce-114">Ai documenti restituiti in una query di ricerca di Microsoft Windows sono assegnati valori di classificazione in base alle condizioni di ricerca corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="da8ce-114">Documents returned in a Microsoft Windows Search query are assigned rank values according to how well they match the search conditions.</span></span> <span data-ttu-id="da8ce-115">Ogni condizione di ricerca di query può includere una clausola [RANKBY](-search-sql-rankby.md) che supporta la modifica dei valori di rango restituiti.</span><span class="sxs-lookup"><span data-stu-id="da8ce-115">Each of the query search conditions can include a [RANKBY](-search-sql-rankby.md) clause that supports modifying the returned rank values.</span></span>

<span data-ttu-id="da8ce-116">La [funzione ReuseWhere](-search-sql-reusewhere.md) esegue più query che utilizzano le stesse condizioni di ricerca più efficienti.</span><span class="sxs-lookup"><span data-stu-id="da8ce-116">The [ReuseWhere function](-search-sql-reusewhere.md) makes multiple queries that use the some of the same search conditions more efficient.</span></span> <span data-ttu-id="da8ce-117">La clausola WHERE in una query specifica il set di elementi che corrispondono a una query.</span><span class="sxs-lookup"><span data-stu-id="da8ce-117">The WHERE clause in a query specifies the set of items that match in a query.</span></span> <span data-ttu-id="da8ce-118">Le query successive possono condividere il lavoro eseguito per il valutazione precedente usando la funzione ReuseWhere nella nuova clausola WHERE della query.</span><span class="sxs-lookup"><span data-stu-id="da8ce-118">Subsequent queries can share the work performed for the previous evalution by using the ReuseWhere function in the new query WHERE clause.</span></span>

## <a name="search-predicates"></a><span data-ttu-id="da8ce-119">Cerca predicati</span><span class="sxs-lookup"><span data-stu-id="da8ce-119">Search Predicates</span></span>

<span data-ttu-id="da8ce-120">Una condizione di ricerca è costituita da uno o più predicati o da condizioni di ricerca che descrivono ciò che l'utente sta cercando (ad esempio, dove System. DateCreated >' 2006-04-19').</span><span class="sxs-lookup"><span data-stu-id="da8ce-120">A search condition consists of one or more predicates or search conditions that describe what the user is searching for (for example, WHERE System.DateCreated >'2006-04-19').</span></span> <span data-ttu-id="da8ce-121">I predicati di ricerca possono essere combinati usando gli operatori logici **and**, **or** o **not**.</span><span class="sxs-lookup"><span data-stu-id="da8ce-121">Search predicates can be combined using the logical operators **AND**, **OR**, or **NOT**.</span></span> <span data-ttu-id="da8ce-122">L'operatore unario facoltativo **not** può essere utilizzato solo con **e** e solo per negare il valore logico di un predicato o di una condizione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="da8ce-122">The optional unary operator **NOT** can be used only with **AND** and only to negate the logical value of a predicate or search condition.</span></span> <span data-ttu-id="da8ce-123">È possibile usare le parentesi per raggruppare e annidare i termini logici.</span><span class="sxs-lookup"><span data-stu-id="da8ce-123">You can use parentheses to group and nest logical terms.</span></span>

<span data-ttu-id="da8ce-124">Nella tabella seguente viene illustrato l'ordine di precedenza per gli operatori logici.</span><span class="sxs-lookup"><span data-stu-id="da8ce-124">The following table shows the order of precedence for the logical operators.</span></span>



| <span data-ttu-id="da8ce-125">Ordine (precedenza)</span><span class="sxs-lookup"><span data-stu-id="da8ce-125">Order (precedence)</span></span> | <span data-ttu-id="da8ce-126">Operatore logico</span><span class="sxs-lookup"><span data-stu-id="da8ce-126">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="da8ce-127">Primo (massimo)</span><span class="sxs-lookup"><span data-stu-id="da8ce-127">First (highest)</span></span>    | <span data-ttu-id="da8ce-128">**NOT**</span><span class="sxs-lookup"><span data-stu-id="da8ce-128">**NOT**</span></span>          |
| <span data-ttu-id="da8ce-129">Second</span><span class="sxs-lookup"><span data-stu-id="da8ce-129">Second</span></span>             | <span data-ttu-id="da8ce-130">**AND**</span><span class="sxs-lookup"><span data-stu-id="da8ce-130">**AND**</span></span>          |
| <span data-ttu-id="da8ce-131">Terzo (minimo)</span><span class="sxs-lookup"><span data-stu-id="da8ce-131">Third (lowest)</span></span>     | <span data-ttu-id="da8ce-132">**OR**</span><span class="sxs-lookup"><span data-stu-id="da8ce-132">**OR**</span></span>           |



 

<span data-ttu-id="da8ce-133">Gli operatori logici dello stesso tipo sono associativi e non esiste alcun ordine di calcolo specificato.</span><span class="sxs-lookup"><span data-stu-id="da8ce-133">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="da8ce-134">È ad esempio possibile calcolare (a **e** B) **e** (c **e** d) (a **e** d) **e** (B **e** C) senza alcuna modifica nel risultato logico.</span><span class="sxs-lookup"><span data-stu-id="da8ce-134">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (A **AND** D) **AND** (B **AND** C) with no change in the logical result.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="da8ce-135">Errato: WHERE **not** Contains (' computer ')</span><span class="sxs-lookup"><span data-stu-id="da8ce-135">Incorrect: WHERE **NOT** CONTAINS ('computer')</span></span>
>
> <span data-ttu-id="da8ce-136">Corretto: WHERE CONTAINs (' software ') **e not** Contains (' computer ')</span><span class="sxs-lookup"><span data-stu-id="da8ce-136">Correct: WHERE CONTAINS ('software') **AND NOT** CONTAINS ('computer')</span></span>

 

<span data-ttu-id="da8ce-137">Nelle query complesse, è consigliabile inserire più enfasi sulle corrispondenze in alcune colonne rispetto alle altre.</span><span class="sxs-lookup"><span data-stu-id="da8ce-137">In complex queries, you might want to place more emphasis on matches in some columns than in others.</span></span> <span data-ttu-id="da8ce-138">Ad esempio, durante la ricerca di documenti che discutono "progettazione software", trovare il termine di ricerca nel titolo del documento è più probabile che sia una corrispondenza migliore rispetto alla ricerca delle singole parole nel testo del documento.</span><span class="sxs-lookup"><span data-stu-id="da8ce-138">For example, when searching for documents that discuss "software design", finding the search term in the document title is more likely to be a good match than finding the individual words in the text of the document.</span></span> <span data-ttu-id="da8ce-139">Per influenzare la classificazione dei documenti in questo modo, il linguaggio di query di ricerca di Microsoft Windows supporta la ponderazione delle condizioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="da8ce-139">To influence the ranking of documents in this manner, the Microsoft Windows Search query language supports weighting the search conditions.</span></span> <span data-ttu-id="da8ce-140">Per ulteriori informazioni sulla ponderazione delle colonne, vedere il predicato [Contains](-search-sql-contains.md) e il [predicato FREETEXT](-search-sql-freetext.md).</span><span class="sxs-lookup"><span data-stu-id="da8ce-140">For more information about column weighting, see [CONTAINS Predicate](-search-sql-contains.md) and [FREETEXT Predicate](-search-sql-freetext.md).</span></span>

<span data-ttu-id="da8ce-141">Sono disponibili tre gruppi di predicati di ricerca in Windows Search: ricerca full-text, non full-text e profondità cartella.</span><span class="sxs-lookup"><span data-stu-id="da8ce-141">There are three groups of search predicates in Windows Search: full-text, non-full-text, and folder depth searches.</span></span> <span data-ttu-id="da8ce-142">I predicati di ricerca full-text in genere corrispondono al significato del contenuto, del titolo e di altre colonne e supportano la corrispondenza linguistica (ad esempio, moduli Word alternativi, frasi e ricerca vicina).</span><span class="sxs-lookup"><span data-stu-id="da8ce-142">Full-text search predicates typically match the meaning of the content, title, and other columns, and support linguistic matching (for example, alternative word forms, phrases, and proximity searching).</span></span> <span data-ttu-id="da8ce-143">I predicati di ricerca non full-text, invece, corrispondono al valore delle colonne specificate e non includono alcuna elaborazione linguistica speciale, ma in molti casi offrono criteri di ricerca basati su caratteri.</span><span class="sxs-lookup"><span data-stu-id="da8ce-143">In contrast, non-full-text search predicates match the value of the specified columns and do not include any special linguistic processing, but in several cases offer character-based pattern matching.</span></span> <span data-ttu-id="da8ce-144">I predicati di profondità della cartella limitano l'ambito di ricerca a un percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="da8ce-144">Folder depth predicates restrict the search scope to a specified path.</span></span>

> [!Note]  
> <span data-ttu-id="da8ce-145">Se la query restituisce un documento perché un predicato non full-text restituisce **true** per quel documento, il valore di pertinenza viene calcolato come 1000.</span><span class="sxs-lookup"><span data-stu-id="da8ce-145">If the query returns a document because a non-full-text predicate evaluates to **TRUE** for that document, the rank value is calculated as 1000.</span></span> <span data-ttu-id="da8ce-146">L'utilizzo della [funzione di coercizione Rank](-search-sql-rankby.md) può modificare il valore di pertinenza.</span><span class="sxs-lookup"><span data-stu-id="da8ce-146">Using the [rank coercion function](-search-sql-rankby.md) can modify the rank value.</span></span>

 

<span data-ttu-id="da8ce-147">Nelle tabelle seguenti vengono descritti i predicati di ricerca full-text, non full-text e Depth.</span><span class="sxs-lookup"><span data-stu-id="da8ce-147">The following tables describe the full-text, non-full-text, and folder depth search predicates.</span></span>



| <span data-ttu-id="da8ce-148">Predicato full-text</span><span class="sxs-lookup"><span data-stu-id="da8ce-148">Full-text predicate</span></span>                  | <span data-ttu-id="da8ce-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da8ce-149">Description</span></span>                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da8ce-150">CONTAINS</span><span class="sxs-lookup"><span data-stu-id="da8ce-150">CONTAINS</span></span>](-search-sql-contains.md) | <span data-ttu-id="da8ce-151">Supporta ricerche complesse per i termini nelle colonne di testo del documento, ad esempio titolo, contenuto.</span><span class="sxs-lookup"><span data-stu-id="da8ce-151">Supports complex searches for terms in document text columns (for example, title, contents).</span></span> <span data-ttu-id="da8ce-152">Consente di cercare forme flesse dei termini di ricerca, di verificare la vicinanza dei termini e di eseguire confronti logici.</span><span class="sxs-lookup"><span data-stu-id="da8ce-152">Can search for inflected forms of the search terms, test for proximity of the terms, and perform logical comparisons.</span></span> <span data-ttu-id="da8ce-153">I termini di ricerca possono includere caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="da8ce-153">Search terms can include wildcard characters.</span></span> |
| [<span data-ttu-id="da8ce-154">FREETEXT</span><span class="sxs-lookup"><span data-stu-id="da8ce-154">FREETEXT</span></span>](-search-sql-freetext.md) | <span data-ttu-id="da8ce-155">Cerca i documenti che corrispondono al significato della frase di ricerca.</span><span class="sxs-lookup"><span data-stu-id="da8ce-155">Searches for documents that match the meaning of the search phrase.</span></span> <span data-ttu-id="da8ce-156">Parole correlate e frasi simili corrisponderanno, con la colonna Rank calcolata in base alla precisione del documento corrispondente alla frase di ricerca.</span><span class="sxs-lookup"><span data-stu-id="da8ce-156">Related words and similar phrases will match, with the rank column calculated based on how closely the document matches the search phrase.</span></span> <span data-ttu-id="da8ce-157">I termini di ricerca non possono includere caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="da8ce-157">Search terms cannot include wildcard characters.</span></span>  |



 



| <span data-ttu-id="da8ce-158">Predicato non full-text</span><span class="sxs-lookup"><span data-stu-id="da8ce-158">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="da8ce-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da8ce-159">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da8ce-160">LIKE</span><span class="sxs-lookup"><span data-stu-id="da8ce-160">LIKE</span></span>](-search-sql-like.md)                                               | <span data-ttu-id="da8ce-161">I valori della colonna vengono confrontati usando semplici criteri di ricerca con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="da8ce-161">Column values are compared using simple pattern matching with wildcard characters.</span></span>                                                                                                    |
| [<span data-ttu-id="da8ce-162">Confronto di valori letterali</span><span class="sxs-lookup"><span data-stu-id="da8ce-162">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="da8ce-163">I valori delle colonne vengono confrontati con stringhe, date, timestamp, numerici e altri valori letterali.</span><span class="sxs-lookup"><span data-stu-id="da8ce-163">Column values are compared against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="da8ce-164">Questo predicato supporta l'uguaglianza e le disuguaglianze, ad esempio maggiore di e minore di.</span><span class="sxs-lookup"><span data-stu-id="da8ce-164">This predicate supports equality and inequalities such as greater than and less than.</span></span> |
| [<span data-ttu-id="da8ce-165">Confronti multivalore (matrice)</span><span class="sxs-lookup"><span data-stu-id="da8ce-165">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="da8ce-166">Le colonne multivalore vengono confrontate con una matrice multivalore di valori letterali.</span><span class="sxs-lookup"><span data-stu-id="da8ce-166">Multivalued columns are compared against a multivalued array of literals.</span></span>                                                                                                             |
| [<span data-ttu-id="da8ce-167">NULL</span><span class="sxs-lookup"><span data-stu-id="da8ce-167">NULL</span></span>](-search-sql-null.md)                                               | <span data-ttu-id="da8ce-168">I valori di colonna non definiti per il documento possono essere rilevati usando il predicato **null** .</span><span class="sxs-lookup"><span data-stu-id="da8ce-168">Column values that are undefined for the document can be detected by using the **NULL** predicate.</span></span>                                                                                    |



 



| <span data-ttu-id="da8ce-169">Profondità cartella</span><span class="sxs-lookup"><span data-stu-id="da8ce-169">Folder Depth</span></span>                             | <span data-ttu-id="da8ce-170">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da8ce-170">Description</span></span>                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da8ce-171">AMBITO</span><span class="sxs-lookup"><span data-stu-id="da8ce-171">SCOPE</span></span>](-search-sql-folderdepth.md)     | <span data-ttu-id="da8ce-172">Esegue un attraversamento profondo del percorso specificato, inclusa la cartella specifica e tutte le sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="da8ce-172">Performs a deep traversal of the specified path, including the specific folder and all subfolders.</span></span> |
| [<span data-ttu-id="da8ce-173">DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="da8ce-173">DIRECTORY</span></span>](-search-sql-folderdepth.md) | <span data-ttu-id="da8ce-174">Esegue un attraversamento superficiale del percorso specificato, eseguendo la ricerca solo nella cartella specifica.</span><span class="sxs-lookup"><span data-stu-id="da8ce-174">Performs a shallow traversal of the specified path, searching only the specific folder.</span></span>            |



 

## <a name="examples"></a><span data-ttu-id="da8ce-175">Esempio</span><span class="sxs-lookup"><span data-stu-id="da8ce-175">Examples</span></span>

<span data-ttu-id="da8ce-176">Per esempi della clausola WHERE, vedere i singoli argomenti del predicato collegati nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="da8ce-176">For examples of the WHERE clause, see the individual predicate topics linked in the preceding table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da8ce-177">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da8ce-177">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="da8ce-178">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="da8ce-178">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="da8ce-179">ReuseWhere (funzione)</span><span class="sxs-lookup"><span data-stu-id="da8ce-179">ReuseWhere function</span></span>](-search-sql-reusewhere.md)
</dt> <dt>

[<span data-ttu-id="da8ce-180">Proprietà del set di righe</span><span class="sxs-lookup"><span data-stu-id="da8ce-180">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> <dt>

[<span data-ttu-id="da8ce-181">Clausola FROM</span><span class="sxs-lookup"><span data-stu-id="da8ce-181">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="da8ce-182">Panoramica della sintassi SQL di ricerca</span><span class="sxs-lookup"><span data-stu-id="da8ce-182">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="da8ce-183">CON il predicato alias gruppo AS</span><span class="sxs-lookup"><span data-stu-id="da8ce-183">WITH -- AS Group Alias Predicate</span></span>](-search-sql-with-as.md)
</dt> <dt>

[<span data-ttu-id="da8ce-184">Predicati di ambito e DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="da8ce-184">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> <dt>

[<span data-ttu-id="da8ce-185">RANGO per clausola</span><span class="sxs-lookup"><span data-stu-id="da8ce-185">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

<span data-ttu-id="da8ce-186">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="da8ce-186">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="da8ce-187">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="da8ce-187">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="da8ce-188">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="da8ce-188">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



