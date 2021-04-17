---
description: Il linguaggio di query di ricerca di Microsoft Windows supporta sei predicati di ricerca non full-text. I predicati descritti in questa sezione sono elencati nella tabella seguente.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Predicati non full-text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306119"
---
# <a name="non-full-text-predicates"></a><span data-ttu-id="85110-104">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="85110-104">Non-Full-Text Predicates</span></span>

<span data-ttu-id="85110-105">Il linguaggio di query di ricerca di Microsoft Windows supporta sei predicati di ricerca non full-text.</span><span class="sxs-lookup"><span data-stu-id="85110-105">The Microsoft Windows Search query language supports six non-full-text search predicates.</span></span> <span data-ttu-id="85110-106">I predicati descritti in questa sezione sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="85110-106">The predicates described in this section are listed in the following table.</span></span>



| <span data-ttu-id="85110-107">Predicato non full-text</span><span class="sxs-lookup"><span data-stu-id="85110-107">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="85110-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85110-108">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85110-109">ALL bit per bit e SOME bit per bit</span><span class="sxs-lookup"><span data-stu-id="85110-109">ALL BITWISE and SOME BITWISE</span></span>](all-bitwise.md)                            | <span data-ttu-id="85110-110">È un set di parole chiave per il testing dei bit in un tipo integrale.</span><span class="sxs-lookup"><span data-stu-id="85110-110">Is a set of keywords that are about testing the bits in an integral type.</span></span>                                                                                                               |
| [<span data-ttu-id="85110-111">DATEADD (funzione)</span><span class="sxs-lookup"><span data-stu-id="85110-111">DATEADD Function</span></span>](-search-sql-dateadd.md)                                | <span data-ttu-id="85110-112">Esegue calcoli di data e ora per le proprietà corrispondenti con tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="85110-112">Performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="85110-113">Utilizzare la funzione DATEADD per ottenere le date e le ore in un intervallo di tempo specificato prima del presente.</span><span class="sxs-lookup"><span data-stu-id="85110-113">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>     |
| [<span data-ttu-id="85110-114">Predicato LIKE</span><span class="sxs-lookup"><span data-stu-id="85110-114">LIKE Predicate</span></span>](-search-sql-like.md)                                     | <span data-ttu-id="85110-115">Confronta i valori delle colonne usando semplici criteri di ricerca con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="85110-115">Compares column values using simple pattern matching with wildcard characters.</span></span>                                                                                                          |
| [<span data-ttu-id="85110-116">Confronto di valori letterali</span><span class="sxs-lookup"><span data-stu-id="85110-116">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="85110-117">Confronta i valori delle colonne con valori di stringa, data, timestamp, numerici e di altro valore letterale.</span><span class="sxs-lookup"><span data-stu-id="85110-117">Compares column values against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="85110-118">Questo predicato supporta le disuguaglianze quali maggiore di (' >') e minore di (' <').</span><span class="sxs-lookup"><span data-stu-id="85110-118">This predicate supports inequalities such as greater than ('>'), and less than ('<').</span></span> |
| [<span data-ttu-id="85110-119">Confronti multivalore (matrice)</span><span class="sxs-lookup"><span data-stu-id="85110-119">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="85110-120">Confronta le colonne multivalore con una matrice multivalore di valori letterali.</span><span class="sxs-lookup"><span data-stu-id="85110-120">Compares multivalued columns against a multivalued array of literals.</span></span>                                                                                                                   |
| [<span data-ttu-id="85110-121">Predicato NULL</span><span class="sxs-lookup"><span data-stu-id="85110-121">NULL Predicate</span></span>](-search-sql-null.md)                                     | <span data-ttu-id="85110-122">Rileva i valori di colonna che non sono definiti per il documento.</span><span class="sxs-lookup"><span data-stu-id="85110-122">Detects column values that are undefined for the document.</span></span>                                                                                                                              |



 

> [!IMPORTANT]
> <span data-ttu-id="85110-123">Le query di ricerca che usano il predicato **null** possono richiedere che Windows Search analizzi l'intero catalogo, che potrebbe rallentare le prestazioni della query.</span><span class="sxs-lookup"><span data-stu-id="85110-123">Search queries using the **NULL** predicate can require that Windows Search scan the entire catalog, which might slow down the query's performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="85110-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85110-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85110-125">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="85110-125">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



