---
description: Windows Search fornisce funzionalità di ricerca e ricerca per indicizzazione del contenuto che supportano la ricerca full-text. Il linguaggio di query utilizzato da ricerca di Windows estende la sintassi delle query di database standard SQL-92 e SQL-99 per migliorarne l'utilità con le ricerche basate su testo.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484412"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a><span data-ttu-id="78f49-104">Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="78f49-104">Querying the Index with Windows Search SQL Syntax</span></span>

<span data-ttu-id="78f49-105">Windows Search fornisce funzionalità di ricerca e ricerca per indicizzazione del contenuto che supportano la ricerca full-text.</span><span class="sxs-lookup"><span data-stu-id="78f49-105">Windows Search provides content crawling and search features that support full-text searching.</span></span> <span data-ttu-id="78f49-106">Il linguaggio di query utilizzato da ricerca di Windows estende la sintassi delle query di database standard SQL-92 e SQL-99 per migliorarne l'utilità con le ricerche basate su testo.</span><span class="sxs-lookup"><span data-stu-id="78f49-106">The query language used by Windows Search extends the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span>

<span data-ttu-id="78f49-107">Tutte le funzionalità di Windows Search Structured Query Language (SQL) sono compatibili con Windows Search in Windows Vista e versioni successive, incluse tutte le versioni di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="78f49-107">All features of Windows Search Structured Query Language (SQL) are compatible with Windows Search on Windows Vista, and later, including all versions of Windows 10.</span></span>

<span data-ttu-id="78f49-108">In questa sezione viene fornita una panoramica della sintassi SQL in Windows Search e sono inclusi gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="78f49-108">This section provides an overview of SQL syntax in Windows Search, and includes the following topics:</span></span>

- [<span data-ttu-id="78f49-109">Panoramica della sintassi SQL di Windows Search</span><span class="sxs-lookup"><span data-stu-id="78f49-109">Overview of Windows Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
- [<span data-ttu-id="78f49-110">Informazioni generali sul linguaggio di query</span><span class="sxs-lookup"><span data-stu-id="78f49-110">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)
- [<span data-ttu-id="78f49-111">RAGGRUPPA IN... SOPRA... Istruzione</span><span class="sxs-lookup"><span data-stu-id="78f49-111">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
- [<span data-ttu-id="78f49-112">SELECT (istruzione)</span><span class="sxs-lookup"><span data-stu-id="78f49-112">SELECT Statement</span></span>](-search-sql-select.md)
- [<span data-ttu-id="78f49-113">Clausola FROM</span><span class="sxs-lookup"><span data-stu-id="78f49-113">FROM Clause</span></span>](-search-sql-from.md)
- [<span data-ttu-id="78f49-114">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="78f49-114">WHERE Clause</span></span>](-search-sql-where.md)
- [<span data-ttu-id="78f49-115">Clausola ORDER BY</span><span class="sxs-lookup"><span data-stu-id="78f49-115">ORDER BY Clause</span></span>](-search-sql-orderby.md)
- [<span data-ttu-id="78f49-116">RANGO per clausola</span><span class="sxs-lookup"><span data-stu-id="78f49-116">RANK BY Clause</span></span>](-search-sql-rankby.md)
- [<span data-ttu-id="78f49-117">Istruzione SET</span><span class="sxs-lookup"><span data-stu-id="78f49-117">SET Statement</span></span>](-search-sql-set.md)
- [<span data-ttu-id="78f49-118">Proprietà del set di righe</span><span class="sxs-lookup"><span data-stu-id="78f49-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)

<span data-ttu-id="78f49-119">In questa documentazione si presuppone una certa familiarità con il collegamento a oggetti e il database di incorporamento (OLE DB) e SQL.</span><span class="sxs-lookup"><span data-stu-id="78f49-119">This documentation assumes familiarity with Object Linking and Embedding Database (OLE DB), and SQL.</span></span>

## <a name="code-samples"></a><span data-ttu-id="78f49-120">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="78f49-120">Code samples</span></span>

<span data-ttu-id="78f49-121">Nell'esempio di codice WSSQL viene illustrato come comunicare tra Microsoft OLE DB e Windows Search tramite SQL.</span><span class="sxs-lookup"><span data-stu-id="78f49-121">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="78f49-122">Nell'esempio di codice WSOleDB viene illustrato Active Template Library (ATL) OLE DB l'accesso alle applicazioni Windows Search e due metodi aggiuntivi per recuperare i risultati da Windows Search.</span><span class="sxs-lookup"><span data-stu-id="78f49-122">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="78f49-123">Entrambi gli esempi sono disponibili negli [esempi di Windows Search](-search-samples-ovw.md) e [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="78f49-123">Both samples are available in the [Windows Search Samples](-search-samples-ovw.md) and the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>

## <a name="related-topics"></a><span data-ttu-id="78f49-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="78f49-124">Related topics</span></span>

[<span data-ttu-id="78f49-125">Esecuzione di query sull'indice a livello di codice</span><span class="sxs-lookup"><span data-stu-id="78f49-125">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="78f49-126">Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice</span><span class="sxs-lookup"><span data-stu-id="78f49-126">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="78f49-127">Esecuzione di query sull'indice con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="78f49-127">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)

[<span data-ttu-id="78f49-128">Esecuzione di query sull'indice con il protocollo search-ms</span><span class="sxs-lookup"><span data-stu-id="78f49-128">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)

[<span data-ttu-id="78f49-129">Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="78f49-129">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="78f49-130">Uso della sintassi avanzata delle query a livello di codice</span><span class="sxs-lookup"><span data-stu-id="78f49-130">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
