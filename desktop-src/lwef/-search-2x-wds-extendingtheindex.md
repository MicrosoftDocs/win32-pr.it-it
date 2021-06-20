---
title: Estensione dell'indice (funzionalità legacy dell'ambiente Windows)
description: Informazioni su come estendere l'indice in Windows Desktop Search 2.x. Per le versioni di Windows successive a Windows XP e Windows Server 2003, usare Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63408cfe1efeb8da4d6a4540cc57b99ea56ae935
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407354"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a><span data-ttu-id="eea30-104">Estensione dell'indice (funzionalità legacy dell'ambiente Windows)</span><span class="sxs-lookup"><span data-stu-id="eea30-104">Extending the Index (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="eea30-105">Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="eea30-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="eea30-106">Nelle versioni successive usare [invece Windows Search.](../search/-search-3x-wds-overview.md)</span><span class="sxs-lookup"><span data-stu-id="eea30-106">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="eea30-107">L'uso di e lo sviluppo per le versioni 2.x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato a favore [di Windows Search](../search/-search-3x-wds-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eea30-107">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged in favor of [Windows Search](../search/-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="eea30-108">WDS può essere esteso per indicizzare il contenuto di nuovi tipi di file e archivi dati.</span><span class="sxs-lookup"><span data-stu-id="eea30-108">WDS can be extended to index the contents of new file types and data stores.</span></span> <span data-ttu-id="eea30-109">Attualmente, WDS 2.x contiene filtri per oltre 200 tipi di elementi (inclusi elementi di testo non crittografato come HTML, XML e file di codice sorgente) e usa la stessa tecnologia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e gestore di protocollo di SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="eea30-109">Currently, WDS 2.x contains filters for over 200 types of items (including plaintext items such as HTML, XML, and source code files) and uses the same [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)and protocol handler technology as SharePoint Services.</span></span> <span data-ttu-id="eea30-110">Se sono già state installate implementazioni di filtro per i nuovi tipi di file, WDS può usare le interfacce di filtro esistenti per indicizzare questi dati.</span><span class="sxs-lookup"><span data-stu-id="eea30-110">If you already have filter implementations installed for your new file types, WDS can use the existing filter interfaces to index this data.</span></span>

<span data-ttu-id="eea30-111">I componenti aggiuntivi WDS 2.x consentono all'indice di attraversare e analizzare nuovi dati e strutture di dati per ottenere informazioni da aggiungere al catalogo ricercabile.</span><span class="sxs-lookup"><span data-stu-id="eea30-111">WDS 2.x add-ins enable the index to traverse and parse new data and data structures for information to add to the searchable catalog.</span></span> <span data-ttu-id="eea30-112">Questi componenti aggiuntivi possono anche estendere la shell di Windows per associare icone e gestori di menu di scelta rapida ai nuovi tipi di file e archivi dati.</span><span class="sxs-lookup"><span data-stu-id="eea30-112">These add-ins can also extend the Windows Shell to associate icons and context-menu handlers with the new file types and data stores.</span></span> <span data-ttu-id="eea30-113">Per includere nuovi tipi di file nel catalogo di Servizi di distribuzione Windows, un componente aggiuntivo deve implementare [**l'interfaccia IFilter.**](/windows/desktop/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="eea30-113">To include new file types in the WDS catalog, an add-in must implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface.</span></span> <span data-ttu-id="eea30-114">Per includere nuovi archivi dati, un componente aggiuntivo deve essere un gestore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="eea30-114">To include new data stores, an add-in must be a protocol handler.</span></span> <span data-ttu-id="eea30-115">Se il nuovo archivio dati include file incorporati o nuovi tipi di file, sarà anche necessario scrivere un filtro appropriato.</span><span class="sxs-lookup"><span data-stu-id="eea30-115">If the new data store includes embedded files or new file types itself, you will also need to write an appropriate filter as well.</span></span>

> [!Note]
>
> <span data-ttu-id="eea30-116">I filtri e i gestori di protocollo devono essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni clr con il processo in cui vengono eseguiti tutti i componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="eea30-116">Filters and protocol handlers must be written in native code due to potential CLR versioning issues with the process all add-ins run in.</span></span>

 

## <a name="adding-file-types-to-the-index"></a><span data-ttu-id="eea30-117">Aggiunta di tipi di file all'indice</span><span class="sxs-lookup"><span data-stu-id="eea30-117">Adding File Types to the Index</span></span>

<span data-ttu-id="eea30-118">I componenti aggiuntivi possono estendere Servizi di distribuzione Windows per indicizzare tipi di file nuovi o proprietari e per associare ogni nuovo tipo di file a un'icona specifica del file o a un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="eea30-118">Add-ins can extend WDS to index new or proprietary file types and to associate each new file type with a file-specific icon or context menu.</span></span> <span data-ttu-id="eea30-119">A tale scopo, è possibile compilare e registrare un componente aggiuntivo che:</span><span class="sxs-lookup"><span data-stu-id="eea30-119">To do this, you can build and register an add-in that:</span></span>

1.  <span data-ttu-id="eea30-120">Implementa [**un'interfaccia IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)per ogni tipo di file in modo che WDS possa accedere e indicizzare il testo e i metadati del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="eea30-120">Implements an [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface for each file type so WDS can access and index the file type's text and metadata.</span></span>
2.  <span data-ttu-id="eea30-121">Implementa le **interfacce IExtractIcon** e **IContextMenu** per aggiungere icone e menu di scelta rapida per una maggiore integrazione e usabilità.</span><span class="sxs-lookup"><span data-stu-id="eea30-121">Implements the **IExtractIcon** and **IContextMenu** interfaces to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="eea30-122">Per informazioni sull'implementazione dei filtri, vedere Sviluppo di [componenti aggiuntivi IFilter.](-search-2x-wds-ifilteraddins.md)</span><span class="sxs-lookup"><span data-stu-id="eea30-122">For a discussion on implementing filters, see [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="adding-data-stores-to-the-index"></a><span data-ttu-id="eea30-123">Aggiunta di archivi dati all'indice</span><span class="sxs-lookup"><span data-stu-id="eea30-123">Adding Data Stores to the Index</span></span>

<span data-ttu-id="eea30-124">I componenti aggiuntivi possono estendere Servizi di distribuzione Windows per indicizzare nuovi archivi dati e associare file a un'icona o a un menu di scelta rapida specifico del file.</span><span class="sxs-lookup"><span data-stu-id="eea30-124">Add-ins can extend WDS to index new data stores and to associate files with a file-specific icon or context menu.</span></span> <span data-ttu-id="eea30-125">A tale scopo, è possibile compilare e registrare un gestore di protocollo che:</span><span class="sxs-lookup"><span data-stu-id="eea30-125">To do this, you can build and register a protocol handler that:</span></span>

1.  <span data-ttu-id="eea30-126">Implementa le **interfacce ISearchProtocol** e **IUrlAccessor** per elaborare e associare singoli elementi nell'origine contenuto.</span><span class="sxs-lookup"><span data-stu-id="eea30-126">Implements the **ISearchProtocol** and **IUrlAccessor** interfaces to process and bind individual items in the content source.</span></span> <span data-ttu-id="eea30-127">WDS usa gli URL per identificare in modo univoco gli elementi, se si trova nel file system, all'interno di un archivio simile a un database o sul Web.</span><span class="sxs-lookup"><span data-stu-id="eea30-127">WDS uses URLs to uniquely identify items, whether those items are in the file system, inside a database-like store, or on the Web.</span></span>
2.  <span data-ttu-id="eea30-128">Implementa **l'interfaccia IPersistFolder** e parti **dell'interfaccia IShellFolder** per aggiungere icone e menu di scelta rapida per una maggiore integrazione e usabilità.</span><span class="sxs-lookup"><span data-stu-id="eea30-128">Implements the **IPersistFolder** interface and portions of the **IShellFolder** interface to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="eea30-129">Per una discussione sull'implementazione di gestori di protocollo, vedere [Sviluppo di gestori di protocollo.](-search-2x-wds-phaddins.md)</span><span class="sxs-lookup"><span data-stu-id="eea30-129">For a discussion on implementing protocol handlers, see [Developing Protocol Handlers](-search-2x-wds-phaddins.md).</span></span>

## <a name="add-in-installer-guidelines"></a><span data-ttu-id="eea30-130">Linee guida per il programma di installazione dei componenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="eea30-130">Add-in Installer Guidelines</span></span>

<span data-ttu-id="eea30-131">L'installazione di un componente aggiuntivo deve seguire le linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="eea30-131">Installation of an add-in should follow the following guidelines:</span></span>

-   <span data-ttu-id="eea30-132">Il programma di installazione deve usare il programma di installazione EXE o MSI.</span><span class="sxs-lookup"><span data-stu-id="eea30-132">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="eea30-133">È necessario fornire le note sulla versione.</span><span class="sxs-lookup"><span data-stu-id="eea30-133">Release notes must be provided.</span></span>
-   <span data-ttu-id="eea30-134">È **necessario creare una voce Installazione** applicazioni per ogni componente aggiuntivo installato.</span><span class="sxs-lookup"><span data-stu-id="eea30-134">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="eea30-135">Il programma di installazione deve assumere tutte le impostazioni del Registro di sistema per il particolare tipo di file o archivio che il componente aggiuntivo corrente è in conoscenza.</span><span class="sxs-lookup"><span data-stu-id="eea30-135">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="eea30-136">Se viene sovrascritto un componente aggiuntivo precedente, il programma di installazione deve inviare una notifica all'utente.</span><span class="sxs-lookup"><span data-stu-id="eea30-136">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="eea30-137">Se un componente aggiuntivo più recente ha sovrascritto il componente aggiuntivo precedente, dovrebbe essere possibile ripristinare la funzionalità del componente aggiuntivo precedente e renderlo nuovamente il componente aggiuntivo predefinito per quel tipo di file o archivio.</span><span class="sxs-lookup"><span data-stu-id="eea30-137">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type or store again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eea30-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eea30-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="eea30-139">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="eea30-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eea30-140">Sviluppo di componenti aggiuntivi IFilter</span><span class="sxs-lookup"><span data-stu-id="eea30-140">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="eea30-141">Sviluppo di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="eea30-141">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

<span data-ttu-id="eea30-142">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="eea30-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="eea30-143">**Ifilter**</span><span class="sxs-lookup"><span data-stu-id="eea30-143">**IFilter**</span></span>](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
