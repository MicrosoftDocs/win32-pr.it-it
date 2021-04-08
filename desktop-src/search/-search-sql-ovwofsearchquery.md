---
description: Il Structured Query Language di Windows Search (SQL) è simile a una query SQL standard.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Panoramica della sintassi SQL di Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049385"
---
# <a name="overview-of-windows-search-sql-syntax"></a><span data-ttu-id="086bf-103">Panoramica della sintassi SQL di Windows Search</span><span class="sxs-lookup"><span data-stu-id="086bf-103">Overview of Windows Search SQL Syntax</span></span>

<span data-ttu-id="086bf-104">Il Structured Query Language di Windows Search (SQL) è simile a una query SQL standard.</span><span class="sxs-lookup"><span data-stu-id="086bf-104">The Windows Search Structured Query Language (SQL) is similar to a standard SQL query.</span></span> <span data-ttu-id="086bf-105">Viene illustrato nelle due sintassi seguenti:</span><span class="sxs-lookup"><span data-stu-id="086bf-105">It is shown in the following two syntaxes:</span></span>


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

<span data-ttu-id="086bf-106">Nell'esempio di query seguente vengono restituiti i valori conteggio pagine e Data creazione per tutti i documenti con più di 50 pagine, ordinate in ordine crescente di conteggio delle pagine.</span><span class="sxs-lookup"><span data-stu-id="086bf-106">In the following query example, the page count and date created values are returned for all documents which have more than 50 pages, sorted is ascending order of page count.</span></span>

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

<span data-ttu-id="086bf-107">La sintassi di query di Windows Search supporta molte opzioni, consentendo query più complesse.</span><span class="sxs-lookup"><span data-stu-id="086bf-107">The Windows Search query syntax supports many options, enabling more complicated queries.</span></span>

<span data-ttu-id="086bf-108">Nella tabella seguente viene descritta ogni clausola nelle istruzioni SELECT o GROUP ON e le funzionalità supportate.</span><span class="sxs-lookup"><span data-stu-id="086bf-108">The following table describes each clause in the SELECT or GROUP ON statements and the features supported.</span></span>

| <span data-ttu-id="086bf-109">Clausola</span><span class="sxs-lookup"><span data-stu-id="086bf-109">Clause</span></span>                                              | <span data-ttu-id="086bf-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="086bf-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="086bf-111">RAGGRUPPA IN... SOPRA...</span><span class="sxs-lookup"><span data-stu-id="086bf-111">GROUP ON...OVER...</span></span>](-search-sql-group-on-over.md) | <span data-ttu-id="086bf-112">Specifica come raggruppare i risultati restituiti dalla query.</span><span class="sxs-lookup"><span data-stu-id="086bf-112">Specifies how to group results returned by the query.</span></span> <span data-ttu-id="086bf-113">È possibile specificare gli intervalli in base ai quali raggruppare e specificare più di una colonna per il raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="086bf-113">You can specify the ranges by which to group and specify more than one column for grouping.</span></span> <span data-ttu-id="086bf-114">È possibile, ad esempio, raggruppare i risultati in base a un intervallo di dimensioni dei file (Size < 100, 100 <= size < 1000; 1000 <= size) e nidificare i raggruppamenti.</span><span class="sxs-lookup"><span data-stu-id="086bf-114">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size) and nest groupings.</span></span>                                                                                                       |
| [<span data-ttu-id="086bf-115">SELECT</span><span class="sxs-lookup"><span data-stu-id="086bf-115">SELECT</span></span>](-search-sql-select.md)                    | <span data-ttu-id="086bf-116">Specifica le colonne restituite dalla query.</span><span class="sxs-lookup"><span data-stu-id="086bf-116">Specifies the columns returned by the query.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="086bf-117">FROM</span><span class="sxs-lookup"><span data-stu-id="086bf-117">FROM</span></span>](-search-sql-from.md)                        | <span data-ttu-id="086bf-118">Specifica il computer e il catalogo in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="086bf-118">Specifies the machine and catalog to search.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="086bf-119">WHERE</span><span class="sxs-lookup"><span data-stu-id="086bf-119">WHERE</span></span>](-search-sql-where.md)                      | <span data-ttu-id="086bf-120">Specifica ciò che costituisce un documento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="086bf-120">Specifies what constitutes a matching document.</span></span> <span data-ttu-id="086bf-121">Questa clausola include molte opzioni, che consentono un controllo completo sulle condizioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="086bf-121">This clause has many options, enabling rich control over the search conditions.</span></span> <span data-ttu-id="086bf-122">Ad esempio, è possibile trovare una corrispondenza con parole, frasi, forme di Word flessori, stringhe, valori numerici e bit per bit e matrici multivalore.</span><span class="sxs-lookup"><span data-stu-id="086bf-122">For example, you can match against words, phrases, inflectional word forms, strings, numeric and bitwise values, and multi-valued arrays.</span></span> <span data-ttu-id="086bf-123">È anche possibile applicare pesi statistici alle condizioni di corrispondenza e combinare le condizioni di corrispondenza con gli operatori booleani.</span><span class="sxs-lookup"><span data-stu-id="086bf-123">You can also apply statistical weights to the matching conditions, and combine matching conditions with Boolean operators.</span></span> |
| [<span data-ttu-id="086bf-124">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="086bf-124">ORDER BY</span></span>](-search-sql-orderby.md)                 | <span data-ttu-id="086bf-125">Specifica l'ordinamento per i risultati restituiti dalla query.</span><span class="sxs-lookup"><span data-stu-id="086bf-125">Specifies the sort order for the results returned by the query.</span></span> <span data-ttu-id="086bf-126">È possibile specificare più di un campo in base al quale vengono ordinati i risultati ed è possibile utilizzare l'ordinamento crescente o decrescente.</span><span class="sxs-lookup"><span data-stu-id="086bf-126">You can specify more than one field on which the results are sorted, and you can use ascending or descending ordering.</span></span>                                                                                                                                                                                                               |

### <a name="code-samples"></a><span data-ttu-id="086bf-127">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="086bf-127">Code samples</span></span>

<span data-ttu-id="086bf-128">Nell'esempio di codice WSSQL viene illustrato come comunicare tra Microsoft OLE DB e Windows Search tramite SQL.</span><span class="sxs-lookup"><span data-stu-id="086bf-128">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="086bf-129">Nell'esempio di codice WSOleDB viene illustrato Active Template Library (ATL) OLE DB l'accesso alle applicazioni Windows Search e due metodi aggiuntivi per recuperare i risultati da Windows Search.</span><span class="sxs-lookup"><span data-stu-id="086bf-129">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="086bf-130">Entrambi gli esempi sono disponibili in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span><span class="sxs-lookup"><span data-stu-id="086bf-130">Both samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

## <a name="related-topics"></a><span data-ttu-id="086bf-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="086bf-131">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="086bf-132">Riferimento</span><span class="sxs-lookup"><span data-stu-id="086bf-132">Reference</span></span>

[<span data-ttu-id="086bf-133">Valori letterali</span><span class="sxs-lookup"><span data-stu-id="086bf-133">Literals</span></span>](-search-sql-literals.md)

[<span data-ttu-id="086bf-134">Uso di ricerche localizzate</span><span class="sxs-lookup"><span data-stu-id="086bf-134">Using Localized Searches</span></span>](-search-sql-usinglocsearches.md)

[<span data-ttu-id="086bf-135">Informazioni sui valori di pertinenza</span><span class="sxs-lookup"><span data-stu-id="086bf-135">Understanding Relevance Values</span></span>](-search-sql-understandingrelevancevalues.md)

[<span data-ttu-id="086bf-136">Mapping delle proprietà</span><span class="sxs-lookup"><span data-stu-id="086bf-136">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)

[<span data-ttu-id="086bf-137">Sintassi di ricerca avanzata</span><span class="sxs-lookup"><span data-stu-id="086bf-137">Advanced Query Syntax</span></span>](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a><span data-ttu-id="086bf-138">Informazioni concettuali</span><span class="sxs-lookup"><span data-stu-id="086bf-138">Conceptual</span></span>

[<span data-ttu-id="086bf-139">Estensioni SQL in Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="086bf-139">SQL Extensions in Microsoft Windows Search</span></span>](-search-sql-extensions-sps.md)

[<span data-ttu-id="086bf-140">Funzionalità SQL non disponibili in Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="086bf-140">SQL Features Unavailable in Microsoft Windows Search</span></span>](-search-sql-featuresunavailableinspssearch.md)

[<span data-ttu-id="086bf-141">Identificatori</span><span class="sxs-lookup"><span data-stu-id="086bf-141">Identifiers</span></span>](-search-sql-identifiers.md)

[<span data-ttu-id="086bf-142">Distinzione maiuscole/minuscole nelle ricerche</span><span class="sxs-lookup"><span data-stu-id="086bf-142">Case Sensitivity in Searches</span></span>](-search-sql-casesensitivityinsearches.md)

[<span data-ttu-id="086bf-143">Distinzione tra segni diacritici nelle ricerche</span><span class="sxs-lookup"><span data-stu-id="086bf-143">Diacritic Sensitivity in Searches</span></span>](-search-sql-accentinsensitivitysearches.md)

[<span data-ttu-id="086bf-144">Cast del tipo di dati di una colonna</span><span class="sxs-lookup"><span data-stu-id="086bf-144">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)

[<span data-ttu-id="086bf-145">Mapping dei tipi di dati</span><span class="sxs-lookup"><span data-stu-id="086bf-145">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
