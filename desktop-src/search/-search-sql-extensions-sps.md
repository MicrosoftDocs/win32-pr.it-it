---
description: Microsoft Windows Search, basato sugli standard SQL-92 e SQL-99, migliora le ricerche basate su documenti full-text nelle applicazioni di gestione dei documenti o di gestione delle informazioni.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: Estensioni SQL in Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525489"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a><span data-ttu-id="1edd2-103">Estensioni SQL in Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="1edd2-103">SQL Extensions in Microsoft Windows Search</span></span>

<span data-ttu-id="1edd2-104">Microsoft Windows Search, basato sugli standard SQL-92 e SQL-99, migliora le ricerche basate su documenti full-text nelle applicazioni di gestione dei documenti o di gestione delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="1edd2-104">Microsoft Windows Search, based on the SQL-92 and SQL-99 standards, improves full-text document-based searches in document-management or knowledge-management applications.</span></span> <span data-ttu-id="1edd2-105">I miglioramenti della ricerca di Windows sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1edd2-105">Windows Search improvements include the following:</span></span>

## <a name="128-character-identifier-names"></a><span data-ttu-id="1edd2-106">128-nomi di identificatori di caratteri</span><span class="sxs-lookup"><span data-stu-id="1edd2-106">128-Character Identifier Names</span></span>

<span data-ttu-id="1edd2-107">Mentre SQL-92 e SQL-99 limitano la colonna e altri identificatori a 18 caratteri, Windows Search supporta i nomi di colonna di 128 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1edd2-107">While SQL-92 and SQL-99 restrict column and other identifiers to 18 characters, Windows Search supports 128-character column names.</span></span> <span data-ttu-id="1edd2-108">Per altre informazioni, vedere [Identificatori](-search-sql-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="1edd2-108">For more information, see [Identifiers](-search-sql-identifiers.md).</span></span>

## <a name="grouping-results-by-columns"></a><span data-ttu-id="1edd2-109">Raggruppamento dei risultati per colonne</span><span class="sxs-lookup"><span data-stu-id="1edd2-109">Grouping Results by Columns</span></span>

<span data-ttu-id="1edd2-110">Nelle query è possibile specificare come raggruppare i risultati.</span><span class="sxs-lookup"><span data-stu-id="1edd2-110">Queries can specify how to group results.</span></span> <span data-ttu-id="1edd2-111">È possibile specificare gli intervalli in base ai quali raggruppare ed è possibile specificare più di una colonna per il raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="1edd2-111">You can specify the ranges by which to group, and you can specify more than one column for grouping.</span></span> <span data-ttu-id="1edd2-112">È ad esempio possibile raggruppare i risultati in base a un intervallo di dimensioni dei file (Size < 100, 100 <= size < 1000; 1000 <= size) ed è possibile annidare i raggruppamenti.</span><span class="sxs-lookup"><span data-stu-id="1edd2-112">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size), and you can nest groupings.</span></span> <span data-ttu-id="1edd2-113">Per ulteriori informazioni, vedere [Group on... SOPRA... Istruzione](-search-sql-group-on-over.md).</span><span class="sxs-lookup"><span data-stu-id="1edd2-113">For more information, see [GROUP ON ... OVER... Statement](-search-sql-group-on-over.md).</span></span>

## <a name="diacritic-insensitive-searching"></a><span data-ttu-id="1edd2-114">Ricerca Diacritic-Insensitive</span><span class="sxs-lookup"><span data-stu-id="1edd2-114">Diacritic-Insensitive Searching</span></span>

<span data-ttu-id="1edd2-115">Oltre alla ricerca senza distinzione tra maiuscole e minuscole, Windows Search supporta la ricerca non sensibile ai segni diacritici (contrassegni accentati).</span><span class="sxs-lookup"><span data-stu-id="1edd2-115">In addition to searching that is not case-sensitive, Windows Search supports searching that is not sensitive to diacritics (accent marks).</span></span> <span data-ttu-id="1edd2-116">Per altre informazioni, vedere [sensibilità dei segni diacritici nelle ricerche](-search-sql-accentinsensitivitysearches.md).</span><span class="sxs-lookup"><span data-stu-id="1edd2-116">For more information, see [Diacritic Sensitivity in Searches](-search-sql-accentinsensitivitysearches.md).</span></span>

## <a name="column-weighting"></a><span data-ttu-id="1edd2-117">Ponderazione delle colonne</span><span class="sxs-lookup"><span data-stu-id="1edd2-117">Column Weighting</span></span>

<span data-ttu-id="1edd2-118">Le query che cercano più di una colonna possono specificare l'importanza di ogni colonna.</span><span class="sxs-lookup"><span data-stu-id="1edd2-118">Queries that search more than one column can specify the importance of each column.</span></span> <span data-ttu-id="1edd2-119">I predicati [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) supportano entrambi la ponderazione delle colonne.</span><span class="sxs-lookup"><span data-stu-id="1edd2-119">The [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates both support column weighting.</span></span>

## <a name="null-predicate"></a><span data-ttu-id="1edd2-120">Predicato NULL</span><span class="sxs-lookup"><span data-stu-id="1edd2-120">NULL Predicate</span></span>

<span data-ttu-id="1edd2-121">Sebbene l'indicizzazione di contenuto full-text non disponga di un set di colonne definito, le query possono richiedere che i membri del set di risultati eseguano o non dispongano di colonne specificate.</span><span class="sxs-lookup"><span data-stu-id="1edd2-121">Although full-text content indexing has no defined set of columns, queries can require that members of the result set do or do not have specified columns.</span></span> <span data-ttu-id="1edd2-122">Non è possibile distinguere tra un documento e una proprietà specificata con il valore impostato su **null** e un documento che non dispone della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1edd2-122">It is not possible to differentiate between a document has a specified property with the value set to **NULL**, and a document that does not have the property at all.</span></span>

## <a name="rank-modification"></a><span data-ttu-id="1edd2-123">Modifica del rango</span><span class="sxs-lookup"><span data-stu-id="1edd2-123">Rank Modification</span></span>

<span data-ttu-id="1edd2-124">È possibile modificare la classificazione dei risultati della ricerca usando i [pesi](-search-sql-understandingrelevancevalues.md) sulle proprietà e sui gruppi di proprietà con alias.</span><span class="sxs-lookup"><span data-stu-id="1edd2-124">You can manipulate the search results ranking by using [weights](-search-sql-understandingrelevancevalues.md) on properties and on aliased groups of properties.</span></span> <span data-ttu-id="1edd2-125">La coercizione di rango supporta la manipolazione diretta della classificazione della pertinenza in base ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="1edd2-125">Rank coercion supports direct manipulation of the relevance ranking based on the criteria you specify.</span></span>

 

 



