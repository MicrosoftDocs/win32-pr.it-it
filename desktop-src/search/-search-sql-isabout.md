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
# <a name="isabout-term"></a><span data-ttu-id="4c041-103">Termini</span><span class="sxs-lookup"><span data-stu-id="4c041-103">ISABOUT Term</span></span>

<span data-ttu-id="4c041-104">**Deprecato**</span><span class="sxs-lookup"><span data-stu-id="4c041-104">**Deprecated**</span></span>

<span data-ttu-id="4c041-105">Questa funzionalità è stata rimossa a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4c041-105">This feature has been removed as of Windows 8.</span></span> <span data-ttu-id="4c041-106">Se si scrivono nuove applicazioni, evitare di utilizzare questa funzionalità deprecata.</span><span class="sxs-lookup"><span data-stu-id="4c041-106">If you write new applications, avoid using this deprecated feature.</span></span> <span data-ttu-id="4c041-107">Se si modificano le applicazioni esistenti, si consiglia vivamente di rimuovere qualsiasi dipendenza da questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="4c041-107">If you modify existing applications, you are strongly encouraged to remove any dependency on this feature.</span></span>

<span data-ttu-id="4c041-108">Il termine outabout corrisponde alle colonne rispetto a un gruppo di uno o più termini di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4c041-108">The ISABOUT term matches columns against a group of one or more search terms.</span></span> <span data-ttu-id="4c041-109">Ha la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="4c041-109">It has the following syntax:</span></span>


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



<span data-ttu-id="4c041-110">Il termine facoltativo RANKMETHOD specifica il metodo di calcolo utilizzato per classificare i documenti che corrispondono a uno o più componenti.</span><span class="sxs-lookup"><span data-stu-id="4c041-110">The optional RANKMETHOD term specifies the calculation method used to rank the documents that match one or more of the components.</span></span> <span data-ttu-id="4c041-111">Se non viene specificato alcun RANKMETHOD, viene usato il metodo di classificazione del coefficiente Jaccard predefinito.</span><span class="sxs-lookup"><span data-stu-id="4c041-111">If no RANKMETHOD is specified, the default Jaccard Coefficient ranking method is used.</span></span>

<span data-ttu-id="4c041-112">Il termine dell'espressione può avere uno o più componenti.</span><span class="sxs-lookup"><span data-stu-id="4c041-112">The ISABOUT term can have one or more components.</span></span> <span data-ttu-id="4c041-113">Le colonne specificate nel predicato [Contains](-search-sql-contains.md) vengono verificate in base a ogni componente.</span><span class="sxs-lookup"><span data-stu-id="4c041-113">The columns specified in the [CONTAINS](-search-sql-contains.md) predicate are tested against each component.</span></span> <span data-ttu-id="4c041-114">Il documento viene incluso nei risultati se almeno uno dei componenti corrisponde a.</span><span class="sxs-lookup"><span data-stu-id="4c041-114">The document is included in the results if at least one of the components matches.</span></span> <span data-ttu-id="4c041-115">Virgole separate da più componenti.</span><span class="sxs-lookup"><span data-stu-id="4c041-115">Commas separate multiple components.</span></span>

<span data-ttu-id="4c041-116">La parte del componente presenta la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="4c041-116">The component part has the following syntax:</span></span>


```
<match_term> [<weight_term>]
```



<span data-ttu-id="4c041-117">È possibile utilizzare il termine di peso facoltativo per modificare l'importanza relativa di ogni termine nel termine.</span><span class="sxs-lookup"><span data-stu-id="4c041-117">You can use the optional WEIGHT term to change the relative importance of each term within the ISABOUT term.</span></span> <span data-ttu-id="4c041-118">Se non viene applicato alcun termine di peso, viene implicito il peso predefinito di 1,0.</span><span class="sxs-lookup"><span data-stu-id="4c041-118">If no weight term is applied, the default 1.0 weight is implied.</span></span>

<span data-ttu-id="4c041-119">Nella tabella seguente vengono descritti i possibili tipi di termini delle corrispondenze.</span><span class="sxs-lookup"><span data-stu-id="4c041-119">The following table describes possible match term types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c041-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c041-120">Type</span></span></th>
<th><span data-ttu-id="4c041-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c041-121">Description</span></span></th>
<th><span data-ttu-id="4c041-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="4c041-122">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c041-123">Word</span><span class="sxs-lookup"><span data-stu-id="4c041-123">Word</span></span></td>
<td><span data-ttu-id="4c041-124">Una singola parola senza spazi o altra punteggiatura.</span><span class="sxs-lookup"><span data-stu-id="4c041-124">A single word without spaces or other punctuation.</span></span></td>
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
<td><span data-ttu-id="4c041-125">Frase</span><span class="sxs-lookup"><span data-stu-id="4c041-125">Phrase</span></span></td>
<td><span data-ttu-id="4c041-126">Più parole o spazi inclusi.</span><span class="sxs-lookup"><span data-stu-id="4c041-126">Multiple words or included spaces.</span></span></td>
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
<td><span data-ttu-id="4c041-127">Wildcard (Carattere jolly)</span><span class="sxs-lookup"><span data-stu-id="4c041-127">Wildcard</span></span></td>
<td><span data-ttu-id="4c041-128">Parole o frasi con l'asterisco (\*) aggiunto alla fine.</span><span class="sxs-lookup"><span data-stu-id="4c041-128">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="4c041-129">Per ulteriori informazioni, vedere <a href="-search-sql-wildcards.md">utilizzo dei caratteri jolly nel predicato CONTAINS</a>.</span><span class="sxs-lookup"><span data-stu-id="4c041-129">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
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



 

## <a name="isabout-column-weighting"></a><span data-ttu-id="4c041-130">Informazioni sulla ponderazione delle colonne</span><span class="sxs-lookup"><span data-stu-id="4c041-130">ISABOUT Column Weighting</span></span>

<span data-ttu-id="4c041-131">Il termine noabout classifica i documenti corrispondenti in base alla precisione di ogni documento corrispondente al set di termini di corrispondenza nella query.</span><span class="sxs-lookup"><span data-stu-id="4c041-131">The ISABOUT term ranks matching documents based on how closely each document matches the set of match terms in the query.</span></span> <span data-ttu-id="4c041-132">È possibile usare la ponderazione delle colonne per inserire più importanza nella corrispondenza di alcuni termini di corrispondenza rispetto ad altri.</span><span class="sxs-lookup"><span data-stu-id="4c041-132">You can use column weighting to place more importance on matching some match terms than others.</span></span> <span data-ttu-id="4c041-133">È possibile applicare un valore di peso a ogni termine delle corrispondenze del termine di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4c041-133">Each match term in the ISABOUT term can have a weight value applied.</span></span> <span data-ttu-id="4c041-134">Il peso viene applicato a un singolo termine di corrispondenza ed è indicato dalla parola chiave "WEIGHT".</span><span class="sxs-lookup"><span data-stu-id="4c041-134">The weight is applied to a single match term and is indicated by the keyword "WEIGHT".</span></span> <span data-ttu-id="4c041-135">Il termine WEIGHT presenta due sintassi alternative:</span><span class="sxs-lookup"><span data-stu-id="4c041-135">The WEIGHT term has two alternative syntaxes:</span></span>


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



<span data-ttu-id="4c041-136">Il valore del peso deve essere compreso tra 0 e 1,0, con non più di tre posizioni decimali.</span><span class="sxs-lookup"><span data-stu-id="4c041-136">The weight value must be between 0 and 1.0, with no more than three decimal places.</span></span> <span data-ttu-id="4c041-137">Se si specifica un valore di peso al di fuori di questo intervallo, viene restituito un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="4c041-137">Specifying a weight value outside this range results in an error message.</span></span> <span data-ttu-id="4c041-138">Il valore di classificazione non ponderato per un termine viene moltiplicato per il valore del peso per il termine.</span><span class="sxs-lookup"><span data-stu-id="4c041-138">The unweighted ranking value for a term is multiplied by the weight value for the term.</span></span>

<span data-ttu-id="4c041-139">Se per un termine di corrispondenza non viene specificato alcun peso, viene implicato il valore predefinito 1,0.</span><span class="sxs-lookup"><span data-stu-id="4c041-139">If no weight is specified for a match term, the default value, 1.0, is implied.</span></span>

### <a name="example"></a><span data-ttu-id="4c041-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="4c041-140">Example</span></span>

<span data-ttu-id="4c041-141">Nell'esempio seguente vengono applicati i pesi ai due termini di corrispondenza, usando la sintassi Long e short per i valori di peso.</span><span class="sxs-lookup"><span data-stu-id="4c041-141">The following example applies weights to the two ISABOUT match terms, using both the long and short syntax for weight values.</span></span>


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a><span data-ttu-id="4c041-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c041-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4c041-143">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4c041-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4c041-144">Predicato FREETEXT</span><span class="sxs-lookup"><span data-stu-id="4c041-144">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="4c041-145">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="4c041-145">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



