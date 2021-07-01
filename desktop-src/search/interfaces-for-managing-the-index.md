---
description: Informazioni su Windows Search consente di gestire l'indice Windows Search ricerca con Gestione ricerca, Gestione cataloghi e Gestione ambito ricerca per indicizzazione.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfacce per la gestione dell'indice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68360ec9c4a616f74392fd9dd34fc9f53b46114
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120016"
---
# <a name="interfaces-for-managing-the-index"></a><span data-ttu-id="7914d-103">Interfacce per la gestione dell'indice</span><span class="sxs-lookup"><span data-stu-id="7914d-103">Interfaces for Managing the Index</span></span>

<span data-ttu-id="7914d-104">Windows Search consente di gestire l'indice Windows Search con tre componenti principali: Gestione ricerca, Gestione catalogo e Gestione ambito ricerca per indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="7914d-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span> <span data-ttu-id="7914d-105">Alcune di queste interfacce di gestione possono essere usate con privilegi utente standard, ma quelle che modificano lo stato dell'indice richiedono privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="7914d-105">Some of these management interfaces can be used with standard user privileges, but those that change the state of the index require administrative privileges.</span></span>

## <a name="about-the-interfaces-for-managing-the-index"></a><span data-ttu-id="7914d-106">Informazioni sulle interfacce per la gestione dell'indice</span><span class="sxs-lookup"><span data-stu-id="7914d-106">About the Interfaces for Managing the Index</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7914d-107">Componente</span><span class="sxs-lookup"><span data-stu-id="7914d-107">Component</span></span></th>
<th><span data-ttu-id="7914d-108">Interfacce</span><span class="sxs-lookup"><span data-stu-id="7914d-108">Interfaces</span></span></th>
<th><span data-ttu-id="7914d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7914d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7914d-110">Gestione ricerca</span><span class="sxs-lookup"><span data-stu-id="7914d-110">Search Manager</span></span></td>
<td><span data-ttu-id="7914d-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span><span class="sxs-lookup"><span data-stu-id="7914d-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span></span></td>
<td><span data-ttu-id="7914d-112">Fornisce metodi per recuperare e impostare informazioni su Windows Search:</span><span class="sxs-lookup"><span data-stu-id="7914d-112">Provides methods to retrieve and set information about Windows Search:</span></span>
<ul>
<li><span data-ttu-id="7914d-113">Recupero di un'istanza di Gestione cataloghi per un catalogo specifico.</span><span class="sxs-lookup"><span data-stu-id="7914d-113">Getting an instance of the Catalog Manager for a specific catalog.</span></span></li>
<li><span data-ttu-id="7914d-114">Recupero o impostazione delle informazioni sul proxy.</span><span class="sxs-lookup"><span data-stu-id="7914d-114">Getting or setting proxy information.</span></span></li>
<li><span data-ttu-id="7914d-115">Recupero di informazioni sulla versione del Windows Search di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7914d-115">Getting version information about the Windows Search engine.</span></span></li>
</ul>
<span data-ttu-id="7914d-116">Per altre informazioni, vedere <a href="-search-3x-wds-mngidx-searchmanager.md">Uso di Gestione ricerca.</a></span><span class="sxs-lookup"><span data-stu-id="7914d-116">For more information, see <a href="-search-3x-wds-mngidx-searchmanager.md">Using the Search Manager</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7914d-117">Gestione cataloghi</span><span class="sxs-lookup"><span data-stu-id="7914d-117">Catalog Manager</span></span></td>
<td><span data-ttu-id="7914d-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span><span class="sxs-lookup"><span data-stu-id="7914d-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span></span><br/> <span data-ttu-id="7914d-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span><span class="sxs-lookup"><span data-stu-id="7914d-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span></span><br/></td>
<td><span data-ttu-id="7914d-120">Fornisce metodi per gestire un singolo catalogo di ricerca, ad esempio causando una nuova indicizzazione o l'impostazione di timeout.</span><span class="sxs-lookup"><span data-stu-id="7914d-120">Provides methods to manage an individual search catalog, such as causing a re-indexing or setting time-outs.</span></span> <span data-ttu-id="7914d-121">Questa interfaccia gestisce il catalogo in quattro aree:</span><span class="sxs-lookup"><span data-stu-id="7914d-121">This interface manages the catalog in four areas:</span></span>
<ul>
<li><span data-ttu-id="7914d-122">Contenuto del catalogo: assicura che i nuovi dati siano indicizzati e che altri componenti e applicazioni funzionino correttamente forzando una nuova indicizzazione di tutto o parte del catalogo o reimpostando l'intero catalogo.</span><span class="sxs-lookup"><span data-stu-id="7914d-122">Catalog contents - ensuring that new data is indexed and that other applications and components work properly by forcing a re-indexing of all or part of the catalog or by resetting the entire catalog.</span></span></li>
<li><span data-ttu-id="7914d-123">Proprietà del catalogo: impostazione delle proprietà che determinano il modo in cui il catalogo gestisce i timeout durante la connessione ai gestori di protocollo e il modo in cui i contrassegni diacritici vengono gestiti nelle ricerche.</span><span class="sxs-lookup"><span data-stu-id="7914d-123">Catalog properties - setting properties that determine how the catalog manages time-outs when connecting to protocol handlers and how diacritical marks are treated in searches.</span></span></li>
<li><span data-ttu-id="7914d-124">Stato del catalogo: recupero di informazioni sul catalogo, inclusi lo stato, le dimensioni e lo stato corrente dell'attività.</span><span class="sxs-lookup"><span data-stu-id="7914d-124">Catalog status - getting information about the catalog, including status, size, and current activity state.</span></span></li>
<li><span data-ttu-id="7914d-125">Accesso ad altre interfacce: recupero di altre interfacce correlate alla ricerca richieste dall'Gestione ambito ricerca per indicizzazione, dalle notifiche di modifica dei dati e <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>dall'interfaccia ISearchQueryHelper.</strong></a></span><span class="sxs-lookup"><span data-stu-id="7914d-125">Access to other interfaces - retrieving other search-related interfaces required by the Crawl Scope Manager, data change notifications, and the <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> interface.</span></span></li>
</ul>
<span data-ttu-id="7914d-126">Per altre informazioni, vedere <a href="-search-3x-wds-mngidx-catalog-manager.md">Uso di Gestione cataloghi.</a></span><span class="sxs-lookup"><span data-stu-id="7914d-126">For more information, see <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7914d-127">Gestione ambito ricerca per indicizzazione</span><span class="sxs-lookup"><span data-stu-id="7914d-127">Crawl Scope Manager</span></span></td>
<td><span data-ttu-id="7914d-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span><span class="sxs-lookup"><span data-stu-id="7914d-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span></span><br/> <span data-ttu-id="7914d-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span><span class="sxs-lookup"><span data-stu-id="7914d-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span></span><br/> <span data-ttu-id="7914d-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="7914d-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span></span><br/> <span data-ttu-id="7914d-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span><span class="sxs-lookup"><span data-stu-id="7914d-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span></span><br/> <span data-ttu-id="7914d-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="7914d-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span></span><br/> <span data-ttu-id="7914d-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span><span class="sxs-lookup"><span data-stu-id="7914d-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span></span><br/> <span data-ttu-id="7914d-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span><span class="sxs-lookup"><span data-stu-id="7914d-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span></span><br/></td>
<td><span data-ttu-id="7914d-135">Fornisce metodi per informare il motore di ricerca sui contenitori da ricercare o controllare e sugli elementi in tali contenitori da includere o escludere nell'indice.</span><span class="sxs-lookup"><span data-stu-id="7914d-135">Provides methods to inform the search engine about containers to crawl or watch, and items under those containers to include or exclude in the index.</span></span> <span data-ttu-id="7914d-136">È anche possibile eseguire una query sul Gestione ambito ricerca per indicizzazione per verificare se un URL specifico si trova nell'ambito della ricerca per indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="7914d-136">You can also query the Crawl Scope Manager to see if a particular URL is in the crawl scope.</span></span> <span data-ttu-id="7914d-137">Per altre informazioni, vedere <a href="-search-3x-wds-extidx-csm.md">Using the Gestione ambito ricerca per indicizzazione</a>.</span><span class="sxs-lookup"><span data-stu-id="7914d-137">For more information, see <a href="-search-3x-wds-extidx-csm.md">Using the Crawl Scope Manager</a>.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="7914d-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7914d-138">Related topics</span></span>

[<span data-ttu-id="7914d-139">Gestione dell'indice</span><span class="sxs-lookup"><span data-stu-id="7914d-139">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="7914d-140">Uso di Gestione ricerca</span><span class="sxs-lookup"><span data-stu-id="7914d-140">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)

[<span data-ttu-id="7914d-141">Uso di Gestione cataloghi</span><span class="sxs-lookup"><span data-stu-id="7914d-141">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="7914d-142">Uso del Gestione ambito ricerca per indicizzazione</span><span class="sxs-lookup"><span data-stu-id="7914d-142">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
