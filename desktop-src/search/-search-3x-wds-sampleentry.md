---
description: In questo argomento vengono descritte le tecnologie correlate a Windows Search.
ms.assetid: 76b39ea6-2aaf-40e0-aa56-2165e188244d
title: Tecnologie di ricerca correlate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f8a03738958e19712ff8cc4566e4b7f7396ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128587"
---
# <a name="related-search-technologies"></a><span data-ttu-id="bdb13-103">Tecnologie di ricerca correlate</span><span class="sxs-lookup"><span data-stu-id="bdb13-103">Related Search Technologies</span></span>

<span data-ttu-id="bdb13-104">In questo argomento vengono descritte le tecnologie correlate a [Windows Search](-search-3x-wds-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bdb13-104">This topic describes technologies that are related to [Windows Search](-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="bdb13-105">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="bdb13-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="bdb13-106">Ricerca Enterprise</span><span class="sxs-lookup"><span data-stu-id="bdb13-106">Enterprise Search</span></span>](#enterprise-search)
    -   [<span data-ttu-id="bdb13-107">Ricerca di SharePoint Enterprise</span><span class="sxs-lookup"><span data-stu-id="bdb13-107">SharePoint Enterprise Search</span></span>](#sharepoint-enterprise-search)
-   [<span data-ttu-id="bdb13-108">Windows Desktop Search 2. x</span><span class="sxs-lookup"><span data-stu-id="bdb13-108">Windows Desktop Search 2.x</span></span>](#windows-desktop-search-2x)
-   [<span data-ttu-id="bdb13-109">Platform SDK: servizio di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="bdb13-109">Platform SDK: Indexing Service</span></span>](#platform-sdk-indexing-service)
-   [<span data-ttu-id="bdb13-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bdb13-110">Related topics</span></span>](#related-topics)

## <a name="enterprise-search"></a><span data-ttu-id="bdb13-111">Ricerca Enterprise</span><span class="sxs-lookup"><span data-stu-id="bdb13-111">Enterprise Search</span></span>

<span data-ttu-id="bdb13-112">Per una panoramica delle risorse tecniche per la [ricerca Enterprise da Microsoft](https://www.microsoft.com/enterprisesearch/en/us/default.aspx), vedere:</span><span class="sxs-lookup"><span data-stu-id="bdb13-112">For an overview of technical resources for [Enterprise Search from Microsoft](https://www.microsoft.com/enterprisesearch/en/us/default.aspx), see:</span></span>

-   [<span data-ttu-id="bdb13-113">Centro risorse di ricerca Enterprise</span><span class="sxs-lookup"><span data-stu-id="bdb13-113">Enterprise Search Resource Center</span></span>](https://developer.microsoft.com/office/docs)
-   [<span data-ttu-id="bdb13-114">Blog di Microsoft Enterprise Search</span><span class="sxs-lookup"><span data-stu-id="bdb13-114">Microsoft Enterprise Search Blog</span></span>](https://blogs.msdn.com/b/enterprisesearch/rss.aspx)

### <a name="sharepoint-enterprise-search"></a><span data-ttu-id="bdb13-115">Ricerca di SharePoint Enterprise</span><span class="sxs-lookup"><span data-stu-id="bdb13-115">SharePoint Enterprise Search</span></span>

<span data-ttu-id="bdb13-116">SharePoint Foundation 2010 fornisce l' [esecuzione di query dal codice sul lato server](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) e l' [esecuzione di query dal codice sul lato client](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14)).</span><span class="sxs-lookup"><span data-stu-id="bdb13-116">SharePoint Foundation 2010 provides [querying from server-side code](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) and [querying from client-side code](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14)).</span></span> <span data-ttu-id="bdb13-117">Per altre informazioni sull'esecuzione di query, sulla ricerca di nuovi contenuti e sul miglioramento della pertinenza con la ricerca Enterprise di SharePoint Server 2010, vedere la pagina relativa alle [nozioni di base sulle ricerche aziendali](/previous-versions/office/ee554857(v=office.14)).</span><span class="sxs-lookup"><span data-stu-id="bdb13-117">For more information on querying, searching for new content, and improving relevance with Sharepoint Server 2010 Enterprise Search, see [Enterprise Search Fundamentals](/previous-versions/office/ee554857(v=office.14)).</span></span>

<span data-ttu-id="bdb13-118">Windows 7 Search supporta la Federazione di ricerca negli archivi dati remoti usando le tecnologie OpenSearch, che consentono agli utenti di accedere ai dati remoti e interagire con essi da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="bdb13-118">Windows 7 Search supports search federation to remote data stores by using OpenSearch technologies, which enable users to access and interact with their remote data from within Windows Explorer.</span></span> <span data-ttu-id="bdb13-119">SharePoint Search Server 2008 e MOSS 2007 SP2 supportano anche la ricerca federata di server remoti con OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="bdb13-119">SharePoint Search Server 2008 and MOSS 2007 SP2 also support federated search of remote servers using OpenSearch.</span></span> <span data-ttu-id="bdb13-120">Per informazioni sulla distribuzione di Search Server 2008 con Office SharePoint Server 2007, vedere la pagina relativa alla ricerca di ricerca [federata nel \[ server \] 2008](/previous-versions/office/bb931109(v=office.14)).</span><span class="sxs-lookup"><span data-stu-id="bdb13-120">For information about Search Server 2008 deployment with Office SharePoint Server 2007, see [Federated Search \[Search Server 2008\]](/previous-versions/office/bb931109(v=office.14)).</span></span> <span data-ttu-id="bdb13-121">Per informazioni sulla ricerca con facet MOSS, in cui i risultati della ricerca vengono ritrovati per categoria, vedere [codeplex](https://www.codeplex.com/FacetedSearch).</span><span class="sxs-lookup"><span data-stu-id="bdb13-121">For information on MOSS Faceted Search, in which search results are refinded by category, see [Codeplex](https://www.codeplex.com/FacetedSearch).</span></span>

<span data-ttu-id="bdb13-122">I gestori del protocollo di ricerca di Windows utilizzano specifiche di progettazione simili a quelle di SharePoint Server e spesso possono essere utilizzati in modo interscambiabile.</span><span class="sxs-lookup"><span data-stu-id="bdb13-122">Windows Search protocol handlers use design specifications similar to SharePoint Server, and they can often be used interchangeably.</span></span> <span data-ttu-id="bdb13-123">Di conseguenza, quando gli utenti devono eseguire la ricerca in database legacy, archivi di posta elettronica o altre strutture di dati non supportate da Windows Search, è necessario innanzitutto determinare se un gestore di protocollo esiste già per tale archivio dati, ad esempio per l'uso con un'altra applicazione, ad esempio SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="bdb13-123">Hence, when users need to search legacy databases, email stores or other data structures that are not supported by Windows Search, you should first determine whether a protocol handler already exists for that data store, perhaps for use with another application such as SharePoint Server.</span></span> <span data-ttu-id="bdb13-124">In tal caso, è possibile installare il gestore di protocollo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="bdb13-124">If so, you can install that protocol handler on the system.</span></span>

## <a name="windows-desktop-search-2x"></a><span data-ttu-id="bdb13-125">Windows Desktop Search 2. x</span><span class="sxs-lookup"><span data-stu-id="bdb13-125">Windows Desktop Search 2.x</span></span>

<span data-ttu-id="bdb13-126">L'utilizzo di e dello sviluppo per le versioni 2. x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato.</span><span class="sxs-lookup"><span data-stu-id="bdb13-126">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged.</span></span> <span data-ttu-id="bdb13-127">Anziché utilizzare [Windows Desktop Search 2. x](../lwef/-search-2x-wds-overview.md), utilizzare la [ricerca di Windows](-search-3x-wds-overview.md) e l' [API di Windows Search](-search-reference-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="bdb13-127">Instead of using [Windows Desktop Search 2.x](../lwef/-search-2x-wds-overview.md), use [Windows Search](-search-3x-wds-overview.md) and [Windows Search API](-search-reference-entry-page.md).</span></span>

## <a name="platform-sdk-indexing-service"></a><span data-ttu-id="bdb13-128">Platform SDK: servizio di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="bdb13-128">Platform SDK: Indexing Service</span></span>

<span data-ttu-id="bdb13-129">[Platform SDK: il servizio di indicizzazione](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) è obsoleto a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bdb13-129">[Platform SDK: Indexing Service](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) is obsolete as of Windows XP.</span></span> <span data-ttu-id="bdb13-130">Usare invece [Windows Search](-search-3x-wds-overview.md) e l' [API di ricerca di Windows](-search-reference-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="bdb13-130">Instead, use [Windows Search](-search-3x-wds-overview.md) and [Windows Search API](-search-reference-entry-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdb13-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bdb13-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdb13-132">Panoramica di Windows Search</span><span class="sxs-lookup"><span data-stu-id="bdb13-132">Windows Search Overview</span></span>](-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="bdb13-133">Guida per gli sviluppatori di Windows Search</span><span class="sxs-lookup"><span data-stu-id="bdb13-133">Windows Search Developer's Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="bdb13-134">Informazioni di riferimento su Windows Search</span><span class="sxs-lookup"><span data-stu-id="bdb13-134">Windows Search Reference</span></span>](-search-reference-entry-page.md)
</dt> <dt>

[<span data-ttu-id="bdb13-135">Esempi di codice di Windows Search</span><span class="sxs-lookup"><span data-stu-id="bdb13-135">Windows Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

[<span data-ttu-id="bdb13-136">Ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="bdb13-136">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="bdb13-137">Glossario di Windows Search</span><span class="sxs-lookup"><span data-stu-id="bdb13-137">Windows Search Glossary</span></span>](search-glossary.md)
</dt> </dl>

 

 
