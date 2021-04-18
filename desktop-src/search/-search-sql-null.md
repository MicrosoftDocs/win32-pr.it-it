---
description: Il predicato NULL indica se il documento contiene un valore per la colonna indicata.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Predicato NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02a04313ac2b86afe809633bee5ad2cbcf764e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306117"
---
# <a name="null-predicate"></a><span data-ttu-id="33d47-103">Predicato NULL</span><span class="sxs-lookup"><span data-stu-id="33d47-103">NULL Predicate</span></span>

<span data-ttu-id="33d47-104">Il predicato **null** indica se il documento contiene un valore per la colonna indicata.</span><span class="sxs-lookup"><span data-stu-id="33d47-104">The **NULL** predicate indicates whether the document has a value for the indicated column.</span></span>

<span data-ttu-id="33d47-105">Il predicato **null** presenta la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="33d47-105">The **NULL** predicate has the following syntax:</span></span>


```
...WHERE <column> IS [NOT] NULL
```



<span data-ttu-id="33d47-106">La parola chiave NOT facoltativa nega il risultato.</span><span class="sxs-lookup"><span data-stu-id="33d47-106">The optional NOT keyword negates the result.</span></span> <span data-ttu-id="33d47-107">La colonna può essere un [identificatore](-search-sql-identifiers.md)regolare o delimitato.</span><span class="sxs-lookup"><span data-stu-id="33d47-107">The column can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33d47-108">Per verificare se una colonna ha il valore **null** , è necessario utilizzare il predicato **null** .</span><span class="sxs-lookup"><span data-stu-id="33d47-108">To test whether a column has the **NULL** value, you must use the **NULL** predicate.</span></span> <span data-ttu-id="33d47-109">L'utilizzo del valore **null** in un predicato di confronto non è valido.</span><span class="sxs-lookup"><span data-stu-id="33d47-109">It is not valid to use the **NULL** value in a comparison predicate.</span></span> <span data-ttu-id="33d47-110">"WHERE column IS **null**" è corretto.</span><span class="sxs-lookup"><span data-stu-id="33d47-110">"WHERE column IS **NULL**" is correct.</span></span> <span data-ttu-id="33d47-111">"WHERE Column = **null**" non è valido.</span><span class="sxs-lookup"><span data-stu-id="33d47-111">"WHERE column = **NULL**" is not valid.</span></span>

 

## <a name="example"></a><span data-ttu-id="33d47-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="33d47-112">Example</span></span>

<span data-ttu-id="33d47-113">Nell'esempio seguente vengono restituiti i documenti privi di un valore System. video. Director.</span><span class="sxs-lookup"><span data-stu-id="33d47-113">The following example returns documents that do not have a System.Video.Director value.</span></span>


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a><span data-ttu-id="33d47-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33d47-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="33d47-115">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="33d47-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="33d47-116">Predicato LIKE</span><span class="sxs-lookup"><span data-stu-id="33d47-116">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="33d47-117">Confronto di valori letterali</span><span class="sxs-lookup"><span data-stu-id="33d47-117">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="33d47-118">Confronti multivalore (matrice)</span><span class="sxs-lookup"><span data-stu-id="33d47-118">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="33d47-119">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="33d47-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="33d47-120">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="33d47-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="33d47-121">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="33d47-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



