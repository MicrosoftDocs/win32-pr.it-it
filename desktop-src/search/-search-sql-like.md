---
description: Il predicato LIKE esegue il confronto dei criteri di ricerca sulla colonna specificata.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: Predicato LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306124"
---
# <a name="like-predicate"></a><span data-ttu-id="0d69b-103">Predicato LIKE</span><span class="sxs-lookup"><span data-stu-id="0d69b-103">LIKE Predicate</span></span>

<span data-ttu-id="0d69b-104">Il predicato LIKE esegue il confronto dei criteri di ricerca sulla colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="0d69b-104">The LIKE predicate performs pattern-matching comparison on the specified column.</span></span> <span data-ttu-id="0d69b-105">Viene usata la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="0d69b-105">It uses the following syntax:</span></span>


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<span data-ttu-id="0d69b-106"><column>Può essere un [identificatore](-search-sql-identifiers.md)regolare o delimitato.</span><span class="sxs-lookup"><span data-stu-id="0d69b-106">The <column> can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span> <span data-ttu-id="0d69b-107">La colonna è limitata alle proprietà dell'archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="0d69b-107">The column is limited to the properties in the property store.</span></span>

<span data-ttu-id="0d69b-108">Il \_ valore letterale carattere jolly <> è un valore letterale stringa.</span><span class="sxs-lookup"><span data-stu-id="0d69b-108">The <wildcard\_literal> is a string literal.</span></span> <span data-ttu-id="0d69b-109">È racchiuso tra virgolette e, facoltativamente, può contenere caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="0d69b-109">It is enclosed in quotation marks and optionally can contain wildcard characters.</span></span> <span data-ttu-id="0d69b-110">Se necessario, la stringa di corrispondenza può contenere più caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="0d69b-110">The match string can contain multiple wildcard characters if needed.</span></span> <span data-ttu-id="0d69b-111">Nella tabella seguente vengono descritti i caratteri jolly riconosciuti dal predicato LIKE.</span><span class="sxs-lookup"><span data-stu-id="0d69b-111">The following table describes the wildcard characters that the LIKE predicate recognizes.</span></span>



| <span data-ttu-id="0d69b-112">Wildcard (Carattere jolly)</span><span class="sxs-lookup"><span data-stu-id="0d69b-112">Wildcard</span></span>                | <span data-ttu-id="0d69b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d69b-113">Description</span></span>                                                                                                                                                                                     | <span data-ttu-id="0d69b-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="0d69b-114">Example</span></span>                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d69b-115">% (percentuale)</span><span class="sxs-lookup"><span data-stu-id="0d69b-115">% (percent)</span></span>             | <span data-ttu-id="0d69b-116">Trova la corrispondenza di zero o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="0d69b-116">Matches zero or more of any characters.</span></span>                                                                                                                                                         | <span data-ttu-id="0d69b-117">"comp% r" corrisponde a "comp" seguito da zero o più caratteri, terminando con un r.</span><span class="sxs-lookup"><span data-stu-id="0d69b-117">'comp%r' matches 'comp' followed by zero or more of any characters, ending in an r.</span></span>                                                                                                                                  |
| <span data-ttu-id="0d69b-118">\_ sottolineatura</span><span class="sxs-lookup"><span data-stu-id="0d69b-118">\_ (underscore)</span></span>         | <span data-ttu-id="0d69b-119">Individua un qualsiasi singolo carattere.</span><span class="sxs-lookup"><span data-stu-id="0d69b-119">Matches any single character.</span></span>                                                                                                                                                                   | <span data-ttu-id="0d69b-120">"Comp \_ ter" corrisponde a "comp" seguito da un carattere qualsiasi, seguito da "ter".</span><span class="sxs-lookup"><span data-stu-id="0d69b-120">'comp\_ter' matches 'comp' followed by exactly one of any character, followed by 'ter'.</span></span>                                                                                                                              |
| <span data-ttu-id="0d69b-121">\[\](parentesi quadre)</span><span class="sxs-lookup"><span data-stu-id="0d69b-121">\[ \] (square brackets)</span></span> | <span data-ttu-id="0d69b-122">Corrisponde a qualsiasi carattere singolo compreso nell'intervallo o nel set specificato.</span><span class="sxs-lookup"><span data-stu-id="0d69b-122">Matches any single character within the specified range or set.</span></span> <span data-ttu-id="0d69b-123">Ad esempio, \[ a-z \] specifica un intervallo; \[ aeiou \] specifica il set di vocali.</span><span class="sxs-lookup"><span data-stu-id="0d69b-123">For example, \[a-z\] specifies a range; \[aeiou\] specifies the set of vowels.</span></span>                                                  | <span data-ttu-id="0d69b-124">"Comp \[ a-z \] re" corrisponde a "comp" seguito da un singolo carattere compreso tra a e z, seguito da' s'.</span><span class="sxs-lookup"><span data-stu-id="0d69b-124">'comp\[a-z\]re' matches 'comp' followed by a single character in the range of a through z, followed by 're'.</span></span> <span data-ttu-id="0d69b-125">"Comp \[ Ao \] " corrisponde a "comp" seguito da un singolo carattere che deve essere un oggetto o un o.</span><span class="sxs-lookup"><span data-stu-id="0d69b-125">'comp\[ao\]' matches 'comp' followed by a single character that must be either an a or an o.</span></span><br/> |
| <span data-ttu-id="0d69b-126">\[^ \] cursore</span><span class="sxs-lookup"><span data-stu-id="0d69b-126">\[^ \] (caret)</span></span>          | <span data-ttu-id="0d69b-127">Corrisponde a qualsiasi carattere singolo non compreso nell'intervallo o nel set specificato.</span><span class="sxs-lookup"><span data-stu-id="0d69b-127">Matches any single character that is not within the specified range or set.</span></span> <span data-ttu-id="0d69b-128">Ad esempio, \[ ^ a-z \] specifica un intervallo che esclude dalla a alla z; \[ ^ aeiou \] specifica un set che esclude le vocali.</span><span class="sxs-lookup"><span data-stu-id="0d69b-128">For example, \[^a-z\] specifies a range that excludes a through z; \[^aeiou\] specifies a set that excludes vowels.</span></span> | <span data-ttu-id="0d69b-129">"Comp \[ ^ u \] " corrisponde a "comp" seguito da un singolo carattere diverso da u.</span><span class="sxs-lookup"><span data-stu-id="0d69b-129">'comp\[^u\]' matches 'comp' followed by any single character that is not a u.</span></span>                                                                                                                                        |



 

<span data-ttu-id="0d69b-130">Se si creano predicati con più intervalli, è necessario che gli intervalli siano in ordine.</span><span class="sxs-lookup"><span data-stu-id="0d69b-130">If you create predicates with multiple ranges, the ranges must be in order.</span></span>

> [!Note]  
> <span data-ttu-id="0d69b-131">Per trovare la corrispondenza con i caratteri jolly come caratteri letterali per la corrispondenza e non come caratteri jolly, inserire il carattere tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="0d69b-131">To match the wildcard characters as literal characters for matching and not as wildcard characters, place the character inside square brackets.</span></span> <span data-ttu-id="0d69b-132">Ad esempio, per trovare la corrispondenza con il segno di percentuale, usare ' \[ % \] '</span><span class="sxs-lookup"><span data-stu-id="0d69b-132">For example, to match the percent sign, use '\[%\]'</span></span>

 

## <a name="examples"></a><span data-ttu-id="0d69b-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="0d69b-133">Examples</span></span>


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a><span data-ttu-id="0d69b-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d69b-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0d69b-135">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0d69b-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0d69b-136">Confronto di valori letterali</span><span class="sxs-lookup"><span data-stu-id="0d69b-136">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="0d69b-137">Confronti multivalore (matrice)</span><span class="sxs-lookup"><span data-stu-id="0d69b-137">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="0d69b-138">Predicato NULL</span><span class="sxs-lookup"><span data-stu-id="0d69b-138">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="0d69b-139">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0d69b-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0d69b-140">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="0d69b-140">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="0d69b-141">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="0d69b-141">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




