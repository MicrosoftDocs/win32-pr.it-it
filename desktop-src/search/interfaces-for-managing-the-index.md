---
description: "Windows Search consente di gestire l'indice di ricerca di Windows con tre componenti principali: Search Manager, Catalog Manager e Crawl scope Manager."
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfacce per la gestione dell'indice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7191fbdb4e83c9e3f1460b96123901b5f277b41a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225945"
---
# <a name="interfaces-for-managing-the-index"></a><span data-ttu-id="1b0ba-103">Interfacce per la gestione dell'indice</span><span class="sxs-lookup"><span data-stu-id="1b0ba-103">Interfaces for Managing the Index</span></span>

<span data-ttu-id="1b0ba-104">Windows Search consente di gestire l'indice di ricerca di Windows con tre componenti principali: Search Manager, Catalog Manager e Crawl scope Manager.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span> <span data-ttu-id="1b0ba-105">Alcune di queste interfacce di gestione possono essere utilizzate con privilegi utente standard, ma quelle che modificano lo stato dell'indice richiedono privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-105">Some of these management interfaces can be used with standard user privileges, but those that change the state of the index require administrative privileges.</span></span>

## <a name="about-the-interfaces-for-managing-the-index"></a><span data-ttu-id="1b0ba-106">Informazioni sulle interfacce per la gestione dell'indice</span><span class="sxs-lookup"><span data-stu-id="1b0ba-106">About the Interfaces for Managing the Index</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b0ba-107">Componente</span><span class="sxs-lookup"><span data-stu-id="1b0ba-107">Component</span></span></th>
<th><span data-ttu-id="1b0ba-108">Interfacce</span><span class="sxs-lookup"><span data-stu-id="1b0ba-108">Interfaces</span></span></th>
<th><span data-ttu-id="1b0ba-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b0ba-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b0ba-110">Gestione ricerche</span><span class="sxs-lookup"><span data-stu-id="1b0ba-110">Search Manager</span></span></td>
<td><span data-ttu-id="1b0ba-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span><span class="sxs-lookup"><span data-stu-id="1b0ba-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span></span></td>
<td><span data-ttu-id="1b0ba-112">Fornisce metodi per recuperare e impostare informazioni su ricerca di Windows:</span><span class="sxs-lookup"><span data-stu-id="1b0ba-112">Provides methods to retrieve and set information about Windows Search:</span></span>
<ul>
<li><span data-ttu-id="1b0ba-113">Recupero di un'istanza di gestione catalogo per un catalogo specifico.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-113">Getting an instance of the Catalog Manager for a specific catalog.</span></span></li>
<li><span data-ttu-id="1b0ba-114">Recupero o impostazione delle informazioni sul proxy.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-114">Getting or setting proxy information.</span></span></li>
<li><span data-ttu-id="1b0ba-115">Recupero delle informazioni sulla versione del motore di ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-115">Getting version information about the Windows Search engine.</span></span></li>
</ul>
<span data-ttu-id="1b0ba-116">Per ulteriori informazioni, vedere <a href="-search-3x-wds-mngidx-searchmanager.md">utilizzo di Search Manager</a>.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-116">For more information, see <a href="-search-3x-wds-mngidx-searchmanager.md">Using the Search Manager</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b0ba-117">Gestione cataloghi</span><span class="sxs-lookup"><span data-stu-id="1b0ba-117">Catalog Manager</span></span></td>
<td><span data-ttu-id="1b0ba-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span><span class="sxs-lookup"><span data-stu-id="1b0ba-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span></span><br/> <span data-ttu-id="1b0ba-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span><span class="sxs-lookup"><span data-stu-id="1b0ba-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span></span><br/></td>
<td><span data-ttu-id="1b0ba-120">Fornisce metodi per la gestione di un singolo catalogo di ricerca, ad esempio la causa di una nuova indicizzazione o l'impostazione di timeout.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-120">Provides methods to manage an individual search catalog, such as causing a re-indexing or setting time-outs.</span></span> <span data-ttu-id="1b0ba-121">Questa interfaccia gestisce il catalogo in quattro aree:</span><span class="sxs-lookup"><span data-stu-id="1b0ba-121">This interface manages the catalog in four areas:</span></span>
<ul>
<li><span data-ttu-id="1b0ba-122">Contenuto del catalogo: garantire che i nuovi dati vengano indicizzati e che le applicazioni e i componenti funzionino correttamente forzando la reindicizzazione di tutto o parte del catalogo o reimpostando l'intero catalogo.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-122">Catalog contents - ensuring that new data is indexed and that other applications and components work properly by forcing a re-indexing of all or part of the catalog or by resetting the entire catalog.</span></span></li>
<li><span data-ttu-id="1b0ba-123">Proprietà catalogo-impostazione proprietà che determinano il modo in cui il catalogo gestisce i timeout quando ci si connette ai gestori di protocollo e come vengono trattati i segni diacritici nelle ricerche.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-123">Catalog properties - setting properties that determine how the catalog manages time-outs when connecting to protocol handlers and how diacritical marks are treated in searches.</span></span></li>
<li><span data-ttu-id="1b0ba-124">Stato del catalogo: ottenere informazioni sul catalogo, tra cui lo stato, le dimensioni e lo stato dell'attività corrente.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-124">Catalog status - getting information about the catalog, including status, size, and current activity state.</span></span></li>
<li><span data-ttu-id="1b0ba-125">Accesso ad altre interfacce: recupero di altre interfacce correlate alla ricerca richieste da gestione dell'ambito di ricerca per indicizzazione, notifiche delle modifiche dei dati e interfaccia <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1b0ba-125">Access to other interfaces - retrieving other search-related interfaces required by the Crawl Scope Manager, data change notifications, and the <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> interface.</span></span></li>
</ul>
<span data-ttu-id="1b0ba-126">Per ulteriori informazioni, vedere <a href="-search-3x-wds-mngidx-catalog-manager.md">utilizzo di gestione catalogo</a>.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-126">For more information, see <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b0ba-127">Gestione ambito ricerca per indicizzazione</span><span class="sxs-lookup"><span data-stu-id="1b0ba-127">Crawl Scope Manager</span></span></td>
<td><span data-ttu-id="1b0ba-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b0ba-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span></span><br/> <span data-ttu-id="1b0ba-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span><span class="sxs-lookup"><span data-stu-id="1b0ba-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span></span><br/> <span data-ttu-id="1b0ba-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b0ba-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span></span><br/> <span data-ttu-id="1b0ba-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span><span class="sxs-lookup"><span data-stu-id="1b0ba-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span></span><br/> <span data-ttu-id="1b0ba-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b0ba-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span></span><br/> <span data-ttu-id="1b0ba-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b0ba-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span></span><br/> <span data-ttu-id="1b0ba-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span><span class="sxs-lookup"><span data-stu-id="1b0ba-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span></span><br/></td>
<td><span data-ttu-id="1b0ba-135">Fornisce metodi per informare il motore di ricerca sui contenitori per eseguire la ricerca per indicizzazione o l'espressione di controllo e gli elementi in tali contenitori da includere o escludere nell'indice.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-135">Provides methods to inform the search engine about containers to crawl or watch, and items under those containers to include or exclude in the index.</span></span> <span data-ttu-id="1b0ba-136">È anche possibile eseguire una query su Gestione ambito ricerca per verificare se un particolare URL si trova nell'ambito della ricerca per indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-136">You can also query the Crawl Scope Manager to see if a particular URL is in the crawl scope.</span></span> <span data-ttu-id="1b0ba-137">Per ulteriori informazioni, vedere <a href="-search-3x-wds-extidx-csm.md">utilizzo di gestione ambito indicizzazione</a>.</span><span class="sxs-lookup"><span data-stu-id="1b0ba-137">For more information, see <a href="-search-3x-wds-extidx-csm.md">Using the Crawl Scope Manager</a>.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="1b0ba-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b0ba-138">Related topics</span></span>

[<span data-ttu-id="1b0ba-139">Gestione dell'indice</span><span class="sxs-lookup"><span data-stu-id="1b0ba-139">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="1b0ba-140">Utilizzo di gestione ricerche</span><span class="sxs-lookup"><span data-stu-id="1b0ba-140">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)

[<span data-ttu-id="1b0ba-141">Utilizzo di gestione cataloghi</span><span class="sxs-lookup"><span data-stu-id="1b0ba-141">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="1b0ba-142">Utilizzo di gestione ambito ricerca per indicizzazione</span><span class="sxs-lookup"><span data-stu-id="1b0ba-142">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
