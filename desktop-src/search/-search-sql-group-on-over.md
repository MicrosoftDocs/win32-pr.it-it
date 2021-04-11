---
description: GRUPPO su...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: RAGGRUPPA IN... SOPRA... Istruzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d7087305f0a5a86f0288ed92ec4bda5b8c882c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128542"
---
# <a name="group-on--over--statement"></a><span data-ttu-id="668a4-103">RAGGRUPPA IN... SOPRA... Istruzione</span><span class="sxs-lookup"><span data-stu-id="668a4-103">GROUP ON ... OVER ... Statement</span></span>

<span data-ttu-id="668a4-104">GRUPPO su... SOPRA... l'istruzione restituisce un set di righe gerarchico in cui i risultati della ricerca sono divisi in gruppi in base a una colonna specificata e a intervalli di raggruppamento facoltativi.</span><span class="sxs-lookup"><span data-stu-id="668a4-104">The GROUP ON... OVER... statement returns a hierarchical rowset in which search results are divided into groups based on a specified column and optional grouping ranges.</span></span> <span data-ttu-id="668a4-105">Se si raggruppa sulla colonna [System. Kind](../properties/props-system-kind.md) , il set di risultati è diviso in più gruppi: uno per i documenti, uno per le comunicazioni e così via.</span><span class="sxs-lookup"><span data-stu-id="668a4-105">If you group on the [System.Kind](../properties/props-system-kind.md) column, the result set is divided into multiple groups: one for documents, one for communications, and so on.</span></span> <span data-ttu-id="668a4-106">Se si esegue il raggruppamento in [System. Size](../properties/props-system-size.md) e l'intervallo di gruppi 100 KB, il set di risultati è diviso in tre gruppi: elementi di dimensioni < 100 KB, elementi di dimensioni >= 100 KB ed elementi senza valore size.</span><span class="sxs-lookup"><span data-stu-id="668a4-106">If you group on [System.Size](../properties/props-system-size.md) and group range 100 KB, the result set is divided into three groups: items of size < 100 KB, items of size >= 100 KB, and items with no size value.</span></span> <span data-ttu-id="668a4-107">È anche possibile aggregare i raggruppamenti con funzioni.</span><span class="sxs-lookup"><span data-stu-id="668a4-107">You can also aggregate groupings with functions.</span></span>

<span data-ttu-id="668a4-108">In questo argomento vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="668a4-108">This topic covers the following subjects:</span></span>

-   [<span data-ttu-id="668a4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="668a4-109">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="668a4-110">Intervalli di gruppi</span><span class="sxs-lookup"><span data-stu-id="668a4-110">Group Ranges</span></span>](#group-ranges)
-   [<span data-ttu-id="668a4-111">Assegnazione di etichette ai gruppi</span><span class="sxs-lookup"><span data-stu-id="668a4-111">Labeling Groups</span></span>](#labeling-groups)
-   [<span data-ttu-id="668a4-112">Ordinamento di gruppi</span><span class="sxs-lookup"><span data-stu-id="668a4-112">Ordering Groups</span></span>](#ordering-groups)
-   [<span data-ttu-id="668a4-113">Annidamento di gruppi</span><span class="sxs-lookup"><span data-stu-id="668a4-113">Nesting Groups</span></span>](#nesting-groups)
-   [<span data-ttu-id="668a4-114">Raggruppamento di proprietà vettoriali</span><span class="sxs-lookup"><span data-stu-id="668a4-114">Grouping on Vector Properties</span></span>](#grouping-on-vector-properties)
-   [<span data-ttu-id="668a4-115">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="668a4-115">More Examples</span></span>](#more-examples)
-   [<span data-ttu-id="668a4-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="668a4-116">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="668a4-117">Sintassi</span><span class="sxs-lookup"><span data-stu-id="668a4-117">Syntax</span></span>

<span data-ttu-id="668a4-118">GRUPPO su... SOPRA... la sintassi dell'istruzione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="668a4-118">The GROUP ON ... OVER ... statement has the following syntax:</span></span>


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



<span data-ttu-id="668a4-119">dove gli intervalli di raggruppamento vengono definiti come segue:</span><span class="sxs-lookup"><span data-stu-id="668a4-119">where grouping ranges are defined as follows:</span></span>


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



<span data-ttu-id="668a4-120">Il gruppo in <column> può essere un [identificatore](-search-sql-identifiers.md) regolare o delimitato per una proprietà nell'archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="668a4-120">The GROUP ON <column> can be a regular or delimited [identifier](-search-sql-identifiers.md) for a property in the property store.</span></span>

<span data-ttu-id="668a4-121">Il parametro facoltativo <group ranges> è un elenco di uno o più valori (numero, data o stringa) usati per dividere i risultati in gruppi.</span><span class="sxs-lookup"><span data-stu-id="668a4-121">The optional <group ranges> is a list of one or more values (number, date, or string) used for dividing the results into groups.</span></span> <span data-ttu-id="668a4-122"><range limit>Identifica un punto di divisione nel set di risultati restituito e <label> identifica un'etichetta intuitiva per un gruppo.</span><span class="sxs-lookup"><span data-stu-id="668a4-122">The <range limit> identifies a division point in the returned result set, and the <label> identifies a user-friendly label for a group.</span></span> <span data-ttu-id="668a4-123">È possibile dividere il set di risultati in tutti i gruppi necessari.</span><span class="sxs-lookup"><span data-stu-id="668a4-123">You can divide the result set into as many groups as you need.</span></span>

<span data-ttu-id="668a4-124">Il primo gruppo di risultati include gli elementi con il valore minimo possibile per la proprietà specificata fino al limite del primo intervallo escluso.</span><span class="sxs-lookup"><span data-stu-id="668a4-124">The first group of results includes items with the minimum possible value for the specified property up to but not including the first range limit.</span></span> <span data-ttu-id="668a4-125">È possibile fare riferimento a questo gruppo con la parola chiave MINVALUE.</span><span class="sxs-lookup"><span data-stu-id="668a4-125">This group can be referred to with the MINVALUE keyword.</span></span> <span data-ttu-id="668a4-126">Il secondo gruppo è a cui è possibile fare riferimento con l'identificatore di limite intervallo e include gli elementi il cui valore per la proprietà specificata è maggiore o uguale al limite di intervallo.</span><span class="sxs-lookup"><span data-stu-id="668a4-126">The second group can be referred to with the range limit specifier itself and includes items whose value for the specified property is equal to or greater than the range limit.</span></span> <span data-ttu-id="668a4-127">Gli elementi che non dispongono di un valore per la proprietà specificata vengono restituiti per ultimi e possono essere definiti con la parola chiave **null** .</span><span class="sxs-lookup"><span data-stu-id="668a4-127">Any items that do not have a value for the specified property are returned last and can be referred to with the **NULL** keyword.</span></span>

<span data-ttu-id="668a4-128">Ad esempio, un limite di intervallo di ' 2006-01-01' per la proprietà [System. DateCreated](../properties/props-system-datecreated.md) divide il set di risultati in elementi con date precedenti a 2006-01-01 (gruppo MinValue), elementi con date in o dopo 2006-01-01 (2006-01-01 gruppo) ed elementi senza data (gruppo **null** ).</span><span class="sxs-lookup"><span data-stu-id="668a4-128">For example, a range limit of '2006-01-01' for the [System.DateCreated](../properties/props-system-datecreated.md) property divides the result set into items with dates before 2006-01-01 (MINVALUE group), items with dates on or after 2006-01-01 (2006-01-01 group), and items with no date (**NULL** group).</span></span>

<span data-ttu-id="668a4-129">All'interno di ogni gruppo, i risultati vengono ordinati in base ai valori nella colonna gruppo per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="668a4-129">Within each group, the results are sorted by the values in the GROUP ON column by default.</span></span> <span data-ttu-id="668a4-130">La clausola [Order by](-search-sql-orderby.md) facoltativa può contenere un identificatore di direzione di ASC per Ascending (da basso a alto) o DESC per la decrescente (da alto a basso) e l' [ordine nella clausola Group by](-search-sql-orderingroup.md) può ordinare ogni gruppo usando regole diverse.</span><span class="sxs-lookup"><span data-stu-id="668a4-130">The optional [ORDER BY](-search-sql-orderby.md) clause can contain a direction specifier of either ASC for ascending (low to high) or DESC for descending (high to low), and the [ORDER IN GROUP BY](-search-sql-orderingroup.md) clause can order each group using different rules.</span></span> <span data-ttu-id="668a4-131">Per ulteriori informazioni, vedere la sezione [gruppi di ordini](#ordering-groups) riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="668a4-131">See the [Ordering Groups](#ordering-groups) section below for more information.</span></span>

## <a name="group-ranges"></a><span data-ttu-id="668a4-132">Intervalli di gruppi</span><span class="sxs-lookup"><span data-stu-id="668a4-132">Group Ranges</span></span>

<span data-ttu-id="668a4-133">Nella tabella seguente viene illustrato il modo in cui i risultati vengono suddivisi in gruppi in base ai limiti di intervallo:</span><span class="sxs-lookup"><span data-stu-id="668a4-133">The following table demonstrates how results are divided into groups based the range limits:</span></span>



| <span data-ttu-id="668a4-134">Esempio ( <column> \[ intervalli di gruppi \] )</span><span class="sxs-lookup"><span data-stu-id="668a4-134">Example (<column> \[group ranges\])</span></span>        | <span data-ttu-id="668a4-135">Risultato</span><span class="sxs-lookup"><span data-stu-id="668a4-135">Result</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668a4-136">System. size \[ 1000, 5000\]</span><span class="sxs-lookup"><span data-stu-id="668a4-136">System.Size \[1000, 5000\]</span></span>                       | <span data-ttu-id="668a4-137">I risultati sono raggruppati in quattro bucket: **MinValue**: Size < 1000</span><span class="sxs-lookup"><span data-stu-id="668a4-137">Results are grouped into four buckets: **MINVALUE**: Size < 1000</span></span><br/> <span data-ttu-id="668a4-138">**1000:** 1000 <= Size < 5000</span><span class="sxs-lookup"><span data-stu-id="668a4-138">**1000:** 1000 <= Size < 5000</span></span><br/> <span data-ttu-id="668a4-139">**5000:** Dimensioni >= 5000</span><span class="sxs-lookup"><span data-stu-id="668a4-139">**5000:** Size >= 5000</span></span><br/> <span data-ttu-id="668a4-140">**Valore null:** Nessun valore per le dimensioni</span><span class="sxs-lookup"><span data-stu-id="668a4-140">**NULL:** No value for Size</span></span><br/>                                                                      |
| <span data-ttu-id="668a4-141">System. Author \[ before (' m'), After (' r ')\]</span><span class="sxs-lookup"><span data-stu-id="668a4-141">System.Author \[BEFORE('m'),AFTER('r')\]</span></span>         | <span data-ttu-id="668a4-142">I risultati sono raggruppati in quattro bucket: **MinValue:** autore < carattere prima di "m"</span><span class="sxs-lookup"><span data-stu-id="668a4-142">Results are grouped into four buckets: **MINVALUE:** Author < character before "m"</span></span><br/> <span data-ttu-id="668a4-143">**m:** carattere prima di "m" <= autore < carattere dopo "r"</span><span class="sxs-lookup"><span data-stu-id="668a4-143">**m:** character before "m" <= Author < character after "r"</span></span><br/> <span data-ttu-id="668a4-144">**r:** carattere dopo "r" <= autore</span><span class="sxs-lookup"><span data-stu-id="668a4-144">**r:** character after "r" <= Author</span></span><br/> <span data-ttu-id="668a4-145">**Valore null:** Nessun valore per autore</span><span class="sxs-lookup"><span data-stu-id="668a4-145">**NULL:** No value for Author</span></span><br/>      |
| <span data-ttu-id="668a4-146">System. Author \[ MinValue/' da a l', "m"/da a z '\]</span><span class="sxs-lookup"><span data-stu-id="668a4-146">System.Author \[MINVALUE/'a to l',"m"/'m to z'\]</span></span> | <span data-ttu-id="668a4-147">I risultati sono raggruppati in tre bucket: **da a a l:** autore < "m"</span><span class="sxs-lookup"><span data-stu-id="668a4-147">Results are grouped into three buckets: **a to l:** Author < "m"</span></span><br/> <span data-ttu-id="668a4-148">**da m a z:** "m" <= autore</span><span class="sxs-lookup"><span data-stu-id="668a4-148">**m to z:** "m" <= Author</span></span> <br/> <span data-ttu-id="668a4-149">**Valore null:** Nessun valore per autore</span><span class="sxs-lookup"><span data-stu-id="668a4-149">**NULL:** No value for Author</span></span><br/>                                                                                                               |
| <span data-ttu-id="668a4-150">System. DateCreated \[ ' 2005-1-01',' 2006-6-01'\]</span><span class="sxs-lookup"><span data-stu-id="668a4-150">System.DateCreated \['2005-1-01','2006-6-01'\]</span></span>   | <span data-ttu-id="668a4-151">I risultati sono raggruppati in quattro bucket:</span><span class="sxs-lookup"><span data-stu-id="668a4-151">Results are grouped into four buckets:</span></span><br/> <span data-ttu-id="668a4-152">**MinValue:** DateCreated < 2005-1-01</span><span class="sxs-lookup"><span data-stu-id="668a4-152">**MINVALUE:** DateCreated < 2005-1-01</span></span><br/> <span data-ttu-id="668a4-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="668a4-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span></span><br/> <span data-ttu-id="668a4-154">**2006-1-01:** DateCreated >= 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="668a4-154">**2006-1-01:** DateCreated >= 2006-6-01</span></span><br/> <span data-ttu-id="668a4-155">**Valore null:** Nessun valore per DateCreated</span><span class="sxs-lookup"><span data-stu-id="668a4-155">**NULL:** No value for DateCreated</span></span><br/> |



 

 

> [!IMPORTANT]
>
> <span data-ttu-id="668a4-156">Errata `GROUP ON System.Author['m','z','a']`</span><span class="sxs-lookup"><span data-stu-id="668a4-156">Incorrect: `GROUP ON System.Author['m','z','a']`</span></span>
>
> <span data-ttu-id="668a4-157">Corretto `GROUP ON System.Author['a','m','z']`</span><span class="sxs-lookup"><span data-stu-id="668a4-157">Correct: `GROUP ON System.Author['a','m','z']`</span></span>

 

 

## <a name="labeling-groups"></a><span data-ttu-id="668a4-158">Assegnazione di etichette ai gruppi</span><span class="sxs-lookup"><span data-stu-id="668a4-158">Labeling Groups</span></span>

<span data-ttu-id="668a4-159">Per migliorare la leggibilità, è possibile etichettare i gruppi usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="668a4-159">To improve readability, you can label groups using the following syntax:</span></span>


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



<span data-ttu-id="668a4-160">L'etichetta è separata dal limite di intervallo con una barra ed è racchiusa tra virgolette singole.</span><span class="sxs-lookup"><span data-stu-id="668a4-160">The label is separated from the range limit with a slash mark and is enclosed in single quotation marks.</span></span> <span data-ttu-id="668a4-161">Se non si specifica un'etichetta, il nome del gruppo è la stringa limite intervallo.</span><span class="sxs-lookup"><span data-stu-id="668a4-161">If you do not specify a label, the group name is the range limit string.</span></span>

<span data-ttu-id="668a4-162">Di seguito è riportato un esempio di assegnazione di etichette ai gruppi:</span><span class="sxs-lookup"><span data-stu-id="668a4-162">The following is an example of labeling groups:</span></span>


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



<span data-ttu-id="668a4-163">In Windows 7 o versioni successive è anche possibile usare un' \[ altra etichetta generica \] per combinare più intervalli di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="668a4-163">In Windows 7 or later, you can also use a generic \[OTHER\] label to combine multiple grouping ranges.</span></span> <span data-ttu-id="668a4-164">I risultati di tutti i gruppi identificati con questa etichetta verranno combinati in un gruppo con questa etichetta.</span><span class="sxs-lookup"><span data-stu-id="668a4-164">Results from all groups identified with this label will be combined into one group with this label.</span></span> <span data-ttu-id="668a4-165">Questo gruppo di risultati viene restituito dopo tutti gli altri gruppi ad eccezione del gruppo **null** .</span><span class="sxs-lookup"><span data-stu-id="668a4-165">This group of results is returned after all other groups except for the **NULL** group.</span></span> <span data-ttu-id="668a4-166">Il gruppo **null** contiene i risultati per gli elementi che non hanno un valore per la proprietà specificata.</span><span class="sxs-lookup"><span data-stu-id="668a4-166">The **NULL** group contains results for items that do not have a value for the specified property.</span></span> <span data-ttu-id="668a4-167">Prima di Windows 7 l' \[ altra \] etichetta veniva considerata come qualsiasi altra etichetta di gruppo.</span><span class="sxs-lookup"><span data-stu-id="668a4-167">Prior to Windows 7 the \[OTHER\] label is treated like any other group label.</span></span>

<span data-ttu-id="668a4-168">Il codice seguente è un esempio di utilizzo dell' \[ altra \] etichetta per i gruppi che verrebbero creati in Windows 7 o versioni successive:</span><span class="sxs-lookup"><span data-stu-id="668a4-168">The following code is an example of using the \[OTHER\] label for groups that would be created in Windows 7 or later:</span></span>


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



<span data-ttu-id="668a4-169">La tabella seguente illustra i gruppi che verrebbero creati dal codice di raggruppamento precedente in Windows 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="668a4-169">The following table shows the groups that would be created by the preceding grouping code in Windows 7 or later.</span></span>



| <span data-ttu-id="668a4-170">Group</span><span class="sxs-lookup"><span data-stu-id="668a4-170">Group</span></span>     | <span data-ttu-id="668a4-171">System.Author</span><span class="sxs-lookup"><span data-stu-id="668a4-171">System.Author</span></span> | <span data-ttu-id="668a4-172">System. FileName</span><span class="sxs-lookup"><span data-stu-id="668a4-172">System.FileName</span></span> |
|-----------|---------------|-----------------|
| <span data-ttu-id="668a4-173">0</span><span class="sxs-lookup"><span data-stu-id="668a4-173">0</span></span>         | <span data-ttu-id="668a4-174">1Bill</span><span class="sxs-lookup"><span data-stu-id="668a4-174">1Bill</span></span>         | <span data-ttu-id="668a4-175">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="668a4-175">Lorem.docx</span></span>      |
| <span data-ttu-id="668a4-176">Q</span><span class="sxs-lookup"><span data-stu-id="668a4-176">Q</span></span>         | <span data-ttu-id="668a4-177">Regina</span><span class="sxs-lookup"><span data-stu-id="668a4-177">Queen</span></span>         | <span data-ttu-id="668a4-178">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="668a4-178">Ipsum.docx</span></span>      |
|           | <span data-ttu-id="668a4-179">Robin</span><span class="sxs-lookup"><span data-stu-id="668a4-179">Robin</span></span>         | <span data-ttu-id="668a4-180">dolor.docx</span><span class="sxs-lookup"><span data-stu-id="668a4-180">dolor.docx</span></span>      |
| <span data-ttu-id="668a4-181">S</span><span class="sxs-lookup"><span data-stu-id="668a4-181">Y</span></span>         | <span data-ttu-id="668a4-182">Zara</span><span class="sxs-lookup"><span data-stu-id="668a4-182">Zara</span></span>          | <span data-ttu-id="668a4-183">amet.docx</span><span class="sxs-lookup"><span data-stu-id="668a4-183">amet.docx</span></span>       |
| <span data-ttu-id="668a4-184">\[ALTRI\]</span><span class="sxs-lookup"><span data-stu-id="668a4-184">\[OTHER\]</span></span> | <span data-ttu-id="668a4-185">Abner</span><span class="sxs-lookup"><span data-stu-id="668a4-185">Abner</span></span>         | <span data-ttu-id="668a4-186">nonummy.docx</span><span class="sxs-lookup"><span data-stu-id="668a4-186">nonummy.docx</span></span>    |
|           | <span data-ttu-id="668a4-187">Bob</span><span class="sxs-lookup"><span data-stu-id="668a4-187">Bob</span></span>           | <span data-ttu-id="668a4-188">laoreet.docx</span><span class="sxs-lookup"><span data-stu-id="668a4-188">laoreet.docx</span></span>    |
|           | <span data-ttu-id="668a4-189">Xaria</span><span class="sxs-lookup"><span data-stu-id="668a4-189">Xaria</span></span>         | <span data-ttu-id="668a4-190">magna.docx</span><span class="sxs-lookup"><span data-stu-id="668a4-190">magna.docx</span></span>      |
| <span data-ttu-id="668a4-191">**NULL**</span><span class="sxs-lookup"><span data-stu-id="668a4-191">**NULL**</span></span>  |               | <span data-ttu-id="668a4-192">aliquam.docx</span><span class="sxs-lookup"><span data-stu-id="668a4-192">aliquam.docx</span></span>    |



 

## <a name="ordering-groups"></a><span data-ttu-id="668a4-193">Ordinamento di gruppi</span><span class="sxs-lookup"><span data-stu-id="668a4-193">Ordering Groups</span></span>

<span data-ttu-id="668a4-194">Sono disponibili tre modi per ordinare gli elementi nei gruppi:</span><span class="sxs-lookup"><span data-stu-id="668a4-194">There are three ways to order items in groups:</span></span>

-   <span data-ttu-id="668a4-195">Ordinamento predefinito: se non si specifica diversamente, i risultati vengono ordinati in base ai valori della colonna GROUP ON, in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="668a4-195">Default ordering: If you do not specify otherwise, the results are ordered by the values in the GROUP ON column, in ascending order.</span></span>
-   <span data-ttu-id="668a4-196">ORDER BY: è possibile specificare l'ordine decrescente in una clausola ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="668a4-196">ORDER BY: You can specify descending order in an ORDER BY clause.</span></span> <span data-ttu-id="668a4-197">È necessario ordinare i risultati in base alla colonna GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="668a4-197">You must order the results by the GROUP ON column.</span></span>
-   <span data-ttu-id="668a4-198">ORDER IN GROUP BY: è possibile specificare un ordine diverso per ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="668a4-198">ORDER IN GROUP BY: You can specify a different order for each group.</span></span> <span data-ttu-id="668a4-199">Se si esegue il raggruppamento in [System. Kind](../properties/props-system-kind.md), è possibile ordinare i documenti in base a [System. Author](../properties/props-system-author.md) e Music by [System. Music. Artist](../properties/props-system-music-artist.md).</span><span class="sxs-lookup"><span data-stu-id="668a4-199">If you group on [System.Kind](../properties/props-system-kind.md), you can order documents by [System.Author](../properties/props-system-author.md) and music by [System.Music.Artist](../properties/props-system-music-artist.md).</span></span>

<span data-ttu-id="668a4-200">Per ulteriori informazioni sull'ordinamento dei risultati, vedere le pagine di riferimento della clausola [Order by](-search-sql-orderby.md) e [Order in Group](-search-sql-orderingroup.md) .</span><span class="sxs-lookup"><span data-stu-id="668a4-200">For more information on ordering results, see the [ORDER BY Clause](-search-sql-orderby.md) and [ORDER IN GROUP Clause](-search-sql-orderingroup.md) reference pages.</span></span>

## <a name="nesting-groups"></a><span data-ttu-id="668a4-201">Annidamento di gruppi</span><span class="sxs-lookup"><span data-stu-id="668a4-201">Nesting Groups</span></span>

<span data-ttu-id="668a4-202">È possibile annidare gruppi con più clausole GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="668a4-202">You can nest groups with multiple GROUP ON clauses.</span></span> <span data-ttu-id="668a4-203">L'ordine specificato nella query viene riflesso direttamente nella gerarchia dei gruppi di output, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="668a4-203">The order specified in the query is directly reflected in the output group hierarchy, as shown in the following example.</span></span>


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| <span data-ttu-id="668a4-204">System. Kind</span><span class="sxs-lookup"><span data-stu-id="668a4-204">System.Kind</span></span>    | <span data-ttu-id="668a4-205">System.Author</span><span class="sxs-lookup"><span data-stu-id="668a4-205">System.Author</span></span> | <span data-ttu-id="668a4-206">System. DateCreated</span><span class="sxs-lookup"><span data-stu-id="668a4-206">System.DateCreated</span></span> |
|----------------|---------------|--------------------|
| <span data-ttu-id="668a4-207">documenti</span><span class="sxs-lookup"><span data-stu-id="668a4-207">documents</span></span>      | <span data-ttu-id="668a4-208">Willa</span><span class="sxs-lookup"><span data-stu-id="668a4-208">Willa</span></span>         | <span data-ttu-id="668a4-209">2006-01-02</span><span class="sxs-lookup"><span data-stu-id="668a4-209">2006-01-02</span></span>         |
|                |               | <span data-ttu-id="668a4-210">2006-01-05</span><span class="sxs-lookup"><span data-stu-id="668a4-210">2006-01-05</span></span>         |
|                | <span data-ttu-id="668a4-211">Zara</span><span class="sxs-lookup"><span data-stu-id="668a4-211">Zara</span></span>          | <span data-ttu-id="668a4-212">2007-06-02</span><span class="sxs-lookup"><span data-stu-id="668a4-212">2007-06-02</span></span>         |
|                |               | <span data-ttu-id="668a4-213">2007-09-10</span><span class="sxs-lookup"><span data-stu-id="668a4-213">2007-09-10</span></span>         |
| <span data-ttu-id="668a4-214">(DIP) interno</span><span class="sxs-lookup"><span data-stu-id="668a4-214">communications</span></span> | <span data-ttu-id="668a4-215">Abner</span><span class="sxs-lookup"><span data-stu-id="668a4-215">Abner</span></span>         | <span data-ttu-id="668a4-216">2006-04-16</span><span class="sxs-lookup"><span data-stu-id="668a4-216">2006-04-16</span></span>         |
|                | <span data-ttu-id="668a4-217">Jean</span><span class="sxs-lookup"><span data-stu-id="668a4-217">Jean</span></span>          | <span data-ttu-id="668a4-218">2007-02-20</span><span class="sxs-lookup"><span data-stu-id="668a4-218">2007-02-20</span></span>         |
|                | <span data-ttu-id="668a4-219">Willa</span><span class="sxs-lookup"><span data-stu-id="668a4-219">Willa</span></span>         | <span data-ttu-id="668a4-220">2006-10-15</span><span class="sxs-lookup"><span data-stu-id="668a4-220">2006-10-15</span></span>         |
|                | <span data-ttu-id="668a4-221">Zara</span><span class="sxs-lookup"><span data-stu-id="668a4-221">Zara</span></span>          | <span data-ttu-id="668a4-222">2008-01-02</span><span class="sxs-lookup"><span data-stu-id="668a4-222">2008-01-02</span></span>         |



 

 

## <a name="grouping-on-vector-properties"></a><span data-ttu-id="668a4-223">Raggruppamento di proprietà vettoriali</span><span class="sxs-lookup"><span data-stu-id="668a4-223">Grouping on Vector Properties</span></span>

<span data-ttu-id="668a4-224">Raggruppamento di proprietà vettoriali, proprietà che possono contenere uno o più valori contemporaneamente, confronta i valori del vettore singolarmente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="668a4-224">Grouping on vector properties, properties that can contain one or more values simultaneously, compares the vector values individually by default.</span></span> <span data-ttu-id="668a4-225">Se, ad esempio, è presente un documento, Lorem.docx con la proprietà System. Author di "Theresa; Zara "e un altro documento, Ipsum.docx con la proprietà System. Author come" Zara ", la query restituisce il set di risultati in due gruppi, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="668a4-225">For example, if there is one document, Lorem.docx, with the System.Author property as "Theresa;Zara" and another document, Ipsum.docx, with the System.Author property as "Zara", the query returns the result set in two groups as shown here:</span></span>


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| <span data-ttu-id="668a4-226">System.Author</span><span class="sxs-lookup"><span data-stu-id="668a4-226">System.Author</span></span> | <span data-ttu-id="668a4-227">System. FileName</span><span class="sxs-lookup"><span data-stu-id="668a4-227">System.FileName</span></span> |
|---------------|-----------------|
| <span data-ttu-id="668a4-228">Teresa</span><span class="sxs-lookup"><span data-stu-id="668a4-228">Theresa</span></span>       | <span data-ttu-id="668a4-229">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="668a4-229">Lorem.docx</span></span>      |
| <span data-ttu-id="668a4-230">Zara</span><span class="sxs-lookup"><span data-stu-id="668a4-230">Zara</span></span>          | <span data-ttu-id="668a4-231">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="668a4-231">Lorem.docx</span></span>      |
|               | <span data-ttu-id="668a4-232">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="668a4-232">Ipsum.docx</span></span>      |



 

<span data-ttu-id="668a4-233">Come si può notare, il raggruppamento di proprietà Vector restituisce righe duplicate.</span><span class="sxs-lookup"><span data-stu-id="668a4-233">As you can see, grouping on vector properties returns duplicate rows.</span></span> <span data-ttu-id="668a4-234">Lorem.docx viene visualizzato due volte perché contiene due autori.</span><span class="sxs-lookup"><span data-stu-id="668a4-234">Lorem.docx appears twice because it has two authors.</span></span>

 

## <a name="more-examples"></a><span data-ttu-id="668a4-235">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="668a4-235">More Examples</span></span>


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a><span data-ttu-id="668a4-236">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="668a4-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="668a4-237">Funzioni di aggregazione</span><span class="sxs-lookup"><span data-stu-id="668a4-237">Aggregate Functions</span></span>](-search-sql-aggregates.md)
</dt> <dt>

[<span data-ttu-id="668a4-238">Clausola ORDER BY</span><span class="sxs-lookup"><span data-stu-id="668a4-238">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> <dt>

[<span data-ttu-id="668a4-239">Clausola ORDER IN GROUP</span><span class="sxs-lookup"><span data-stu-id="668a4-239">ORDER IN GROUP Clause</span></span>](-search-sql-orderingroup.md)
</dt> </dl>

 

 
