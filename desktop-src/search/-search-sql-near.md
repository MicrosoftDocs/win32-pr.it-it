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
# <a name="near-term"></a><span data-ttu-id="e5bee-103">A breve termine</span><span class="sxs-lookup"><span data-stu-id="e5bee-103">NEAR Term</span></span>

<span data-ttu-id="e5bee-104">Il termine NEAR viene usato per specificare che due termini di ricerca del contenuto devono essere relativamente vicini tra loro per essere riconosciuti come corrispondenti per il predicato [Contains](-search-sql-contains.md) .</span><span class="sxs-lookup"><span data-stu-id="e5bee-104">The NEAR term is used to specify that two content search terms must be relatively close to one another to be recognized as matching for the [CONTAINS](-search-sql-contains.md) predicate.</span></span>

<span data-ttu-id="e5bee-105">La sintassi per il termine vicino è la seguente:</span><span class="sxs-lookup"><span data-stu-id="e5bee-105">The syntax for the NEAR term is:</span></span>


```
<content_search_term> NEAR | ~ <content_search_term>
```



<span data-ttu-id="e5bee-106">Il termine NEAR può essere rappresentato dalla parola chiave "NEAR" o da una tilde (~).</span><span class="sxs-lookup"><span data-stu-id="e5bee-106">The NEAR term can be represented by the keyword "NEAR" or by a tilde (~).</span></span>

<span data-ttu-id="e5bee-107">Quando le parole unite accanto alla query vengono trovate all'interno di circa 50 parole tra loro all'interno della colonna in cui viene eseguita la ricerca, il termine vicino restituisce una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="e5bee-107">When the words joined by NEAR in the query are found within approximately 50 words of each other inside the column being searched, the NEAR term returns a match.</span></span> <span data-ttu-id="e5bee-108">Più vicine sono le due parole, maggiore è il numero di dimensioni calcolato per il breve termine.</span><span class="sxs-lookup"><span data-stu-id="e5bee-108">The closer together the two words are, the higher the calculated rank for the NEAR term.</span></span> <span data-ttu-id="e5bee-109">Oltre alle due parole, minore è il rango.</span><span class="sxs-lookup"><span data-stu-id="e5bee-109">The farther apart the two words are, the lower the rank.</span></span>

> [!Note]  
> <span data-ttu-id="e5bee-110">Il numero di parole tra i termini di ricerca trovati è approssimativo e dipende dall'aspetto delle parole non significative, ad esempio "a" o "The", e come wordbreaker tokenize testo.</span><span class="sxs-lookup"><span data-stu-id="e5bee-110">The number of words between found search terms is approximate and depends on the appearance of noise words, like "a" or "the", and how wordbreakers tokenize text.</span></span> <span data-ttu-id="e5bee-111">Può essere minore di 50.</span><span class="sxs-lookup"><span data-stu-id="e5bee-111">It may be less than 50.</span></span>

 


<span data-ttu-id="e5bee-112">Nella tabella seguente vengono descritti i tipi di termini di ricerca di contenuto che possono essere utilizzati con un predicato CONTAINs in un breve termine.</span><span class="sxs-lookup"><span data-stu-id="e5bee-112">The following table describes content search term types that can be used with a NEAR term in a CONTAINS predicate.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5bee-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5bee-113">Type</span></span></th>
<th><span data-ttu-id="e5bee-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5bee-114">Description</span></span></th>
<th><span data-ttu-id="e5bee-115">Esempi</span><span class="sxs-lookup"><span data-stu-id="e5bee-115">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5bee-116">Word</span><span class="sxs-lookup"><span data-stu-id="e5bee-116">Word</span></span></td>
<td><span data-ttu-id="e5bee-117">Una singola parola senza spazi o altra punteggiatura.</span><span class="sxs-lookup"><span data-stu-id="e5bee-117">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="e5bee-118">Le virgolette doppie non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="e5bee-118">Double quotation marks are not necessary.</span></span></td>
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
<td><span data-ttu-id="e5bee-119">Frase</span><span class="sxs-lookup"><span data-stu-id="e5bee-119">Phrase</span></span></td>
<td><span data-ttu-id="e5bee-120">Più parole o spazi inclusi.</span><span class="sxs-lookup"><span data-stu-id="e5bee-120">Multiple words or included spaces.</span></span></td>
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
<td><span data-ttu-id="e5bee-121">Wildcard (Carattere jolly)</span><span class="sxs-lookup"><span data-stu-id="e5bee-121">Wildcard</span></span></td>
<td><span data-ttu-id="e5bee-122">Parole o frasi con l'asterisco (\*) aggiunto alla fine.</span><span class="sxs-lookup"><span data-stu-id="e5bee-122">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="e5bee-123">Per ulteriori informazioni, vedere <a href="-search-sql-wildcards.md">utilizzo dei caratteri jolly nel predicato CONTAINS</a>.</span><span class="sxs-lookup"><span data-stu-id="e5bee-123">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
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
> <span data-ttu-id="e5bee-124">Se le parole corrispondenti specificate con il termine NEAR si trovano nella colonna cercata, ma sono più lontane di 50 parole, il risultato viene comunque restituito, ma ha un [rango](-search-sql-understandingrelevancevalues.md) pari a 0.</span><span class="sxs-lookup"><span data-stu-id="e5bee-124">If the match words specified with the NEAR term are both found in the column being searched, but are farther apart than 50 words, the result is still returned, but has a [rank](-search-sql-understandingrelevancevalues.md) of 0.</span></span>

 

### <a name="example"></a><span data-ttu-id="e5bee-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="e5bee-125">Example</span></span>

<span data-ttu-id="e5bee-126">Nell'esempio seguente viene illustrato il concatenamento dei termini NEAR, usando le forme brevi e lunghe del termine:</span><span class="sxs-lookup"><span data-stu-id="e5bee-126">The following example shows chaining of NEAR terms, using both the short and long forms of the term:</span></span>


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a><span data-ttu-id="e5bee-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5bee-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e5bee-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e5bee-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e5bee-129">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="e5bee-129">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="e5bee-130">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e5bee-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e5bee-131">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="e5bee-131">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="e5bee-132">Utilizzo di caratteri jolly nel predicato CONTAINs</span><span class="sxs-lookup"><span data-stu-id="e5bee-132">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
</dt> </dl>

 

 



