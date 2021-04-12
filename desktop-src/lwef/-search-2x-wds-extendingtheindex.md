---
title: Estensione dell'indice (funzionalità legacy dell'ambiente Windows)
description: L'utilizzo di e lo sviluppo per le versioni 2. x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato a favore di Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad766d6fa1c00649f7cbdc3118039ed50f13491
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118874"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a><span data-ttu-id="88e72-103">Estensione dell'indice (funzionalità legacy dell'ambiente Windows)</span><span class="sxs-lookup"><span data-stu-id="88e72-103">Extending the Index (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="88e72-104">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="88e72-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="88e72-105">Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="88e72-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="88e72-106">L'utilizzo di e lo sviluppo per le versioni 2. x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato a favore di [Windows Search](../search/-search-3x-wds-overview.md).</span><span class="sxs-lookup"><span data-stu-id="88e72-106">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged in favor of [Windows Search](../search/-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="88e72-107">WDS può essere esteso per indicizzare il contenuto dei nuovi tipi di file e degli archivi dati.</span><span class="sxs-lookup"><span data-stu-id="88e72-107">WDS can be extended to index the contents of new file types and data stores.</span></span> <span data-ttu-id="88e72-108">Attualmente, WDS 2. x contiene filtri per più di 200 tipi di elementi (inclusi elementi di testo non crittografato, ad esempio HTML, XML e file di codice sorgente) e utilizza lo stesso [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e la stessa tecnologia del gestore di protocollo di SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="88e72-108">Currently, WDS 2.x contains filters for over 200 types of items (including plaintext items such as HTML, XML, and source code files) and uses the same [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)and protocol handler technology as SharePoint Services.</span></span> <span data-ttu-id="88e72-109">Se si dispone già di implementazioni di filtro installate per i nuovi tipi di file, WDS può utilizzare le interfacce di filtro esistenti per indicizzare questi dati.</span><span class="sxs-lookup"><span data-stu-id="88e72-109">If you already have filter implementations installed for your new file types, WDS can use the existing filter interfaces to index this data.</span></span>

<span data-ttu-id="88e72-110">I componenti aggiuntivi di WDS 2. x consentono all'indice di attraversare e analizzare i nuovi dati e le strutture di dati per aggiungere informazioni al catalogo ricercabile.</span><span class="sxs-lookup"><span data-stu-id="88e72-110">WDS 2.x add-ins enable the index to traverse and parse new data and data structures for information to add to the searchable catalog.</span></span> <span data-ttu-id="88e72-111">Questi componenti aggiuntivi possono anche estendere la shell di Windows per associare icone e gestori di menu di scelta rapida con i nuovi tipi di file e gli archivi dati.</span><span class="sxs-lookup"><span data-stu-id="88e72-111">These add-ins can also extend the Windows Shell to associate icons and context-menu handlers with the new file types and data stores.</span></span> <span data-ttu-id="88e72-112">Per includere nuovi tipi di file nel catalogo WDS, un componente aggiuntivo deve implementare l'interfaccia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter).</span><span class="sxs-lookup"><span data-stu-id="88e72-112">To include new file types in the WDS catalog, an add-in must implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface.</span></span> <span data-ttu-id="88e72-113">Per includere nuovi archivi dati, un componente aggiuntivo deve essere un gestore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="88e72-113">To include new data stores, an add-in must be a protocol handler.</span></span> <span data-ttu-id="88e72-114">Se il nuovo archivio dati include file incorporati o nuovi tipi di file, sarà anche necessario scrivere un filtro appropriato.</span><span class="sxs-lookup"><span data-stu-id="88e72-114">If the new data store includes embedded files or new file types itself, you will also need to write an appropriate filter as well.</span></span>

> [!Note]
>
> <span data-ttu-id="88e72-115">I filtri e i gestori di protocollo devono essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni di CLR con il processo in cui vengono eseguiti tutti i componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="88e72-115">Filters and protocol handlers must be written in native code due to potential CLR versioning issues with the process all add-ins run in.</span></span>

 

## <a name="adding-file-types-to-the-index"></a><span data-ttu-id="88e72-116">Aggiunta di tipi di file all'indice</span><span class="sxs-lookup"><span data-stu-id="88e72-116">Adding File Types to the Index</span></span>

<span data-ttu-id="88e72-117">I componenti aggiuntivi possono estendere WDS per indicizzare i tipi di file nuovi o proprietari e associare ogni nuovo tipo di file a un'icona o a un menu di scelta rapida specifico per il file.</span><span class="sxs-lookup"><span data-stu-id="88e72-117">Add-ins can extend WDS to index new or proprietary file types and to associate each new file type with a file-specific icon or context menu.</span></span> <span data-ttu-id="88e72-118">A tale scopo, è possibile creare e registrare un componente aggiuntivo che:</span><span class="sxs-lookup"><span data-stu-id="88e72-118">To do this, you can build and register an add-in that:</span></span>

1.  <span data-ttu-id="88e72-119">Implementa un'interfaccia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)per ogni tipo di file, in modo che WDS possa accedere e indicizzare il testo e i metadati del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="88e72-119">Implements an [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface for each file type so WDS can access and index the file type's text and metadata.</span></span>
2.  <span data-ttu-id="88e72-120">Implementa le interfacce **IExtractIcon** e **IContextMenu** per aggiungere icone e menu di scelta rapida per una maggiore integrazione e usabilità.</span><span class="sxs-lookup"><span data-stu-id="88e72-120">Implements the **IExtractIcon** and **IContextMenu** interfaces to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="88e72-121">Per informazioni sull'implementazione di filtri, vedere [sviluppo di componenti aggiuntivi IFilter](-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="88e72-121">For a discussion on implementing filters, see [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="adding-data-stores-to-the-index"></a><span data-ttu-id="88e72-122">Aggiunta di archivi dati all'indice</span><span class="sxs-lookup"><span data-stu-id="88e72-122">Adding Data Stores to the Index</span></span>

<span data-ttu-id="88e72-123">I componenti aggiuntivi possono estendere WDS per indicizzare nuovi archivi dati e associare i file a un'icona specifica del file o a un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="88e72-123">Add-ins can extend WDS to index new data stores and to associate files with a file-specific icon or context menu.</span></span> <span data-ttu-id="88e72-124">A tale scopo, è possibile creare e registrare un gestore di protocollo che:</span><span class="sxs-lookup"><span data-stu-id="88e72-124">To do this, you can build and register a protocol handler that:</span></span>

1.  <span data-ttu-id="88e72-125">Implementa le interfacce **ISearchProtocol** e **IUrlAccessor** per elaborare e associare singoli elementi nell'origine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="88e72-125">Implements the **ISearchProtocol** and **IUrlAccessor** interfaces to process and bind individual items in the content source.</span></span> <span data-ttu-id="88e72-126">WDS usa gli URL per identificare in modo univoco gli elementi, sia che si trovino nel file system, all'interno di un archivio simile a un database o sul Web.</span><span class="sxs-lookup"><span data-stu-id="88e72-126">WDS uses URLs to uniquely identify items, whether those items are in the file system, inside a database-like store, or on the Web.</span></span>
2.  <span data-ttu-id="88e72-127">Implementa l'interfaccia **IPersistFolder** e le parti dell'interfaccia **IShellFolder** per aggiungere icone e menu di scelta rapida per una maggiore integrazione e usabilità.</span><span class="sxs-lookup"><span data-stu-id="88e72-127">Implements the **IPersistFolder** interface and portions of the **IShellFolder** interface to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="88e72-128">Per informazioni sull'implementazione dei gestori di protocollo, vedere [sviluppo di gestori di protocollo](-search-2x-wds-phaddins.md).</span><span class="sxs-lookup"><span data-stu-id="88e72-128">For a discussion on implementing protocol handlers, see [Developing Protocol Handlers](-search-2x-wds-phaddins.md).</span></span>

## <a name="add-in-installer-guidelines"></a><span data-ttu-id="88e72-129">Linee guida del programma di installazione del componente aggiuntivo</span><span class="sxs-lookup"><span data-stu-id="88e72-129">Add-in Installer Guidelines</span></span>

<span data-ttu-id="88e72-130">L'installazione di un componente aggiuntivo deve attenersi alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="88e72-130">Installation of an add-in should follow the following guidelines:</span></span>

-   <span data-ttu-id="88e72-131">Il programma di installazione deve usare il programma di installazione EXE o MSI.</span><span class="sxs-lookup"><span data-stu-id="88e72-131">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="88e72-132">È necessario fornire le note sulla versione.</span><span class="sxs-lookup"><span data-stu-id="88e72-132">Release notes must be provided.</span></span>
-   <span data-ttu-id="88e72-133">È necessario creare una voce di installazione **applicazioni** per ogni componente aggiuntivo installato.</span><span class="sxs-lookup"><span data-stu-id="88e72-133">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="88e72-134">Il programma di installazione deve assumere tutte le impostazioni del registro di sistema per il tipo di file o l'archivio specifico che il componente aggiuntivo corrente riconosce.</span><span class="sxs-lookup"><span data-stu-id="88e72-134">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="88e72-135">Se un componente aggiuntivo precedente viene sovrascritto, il programma di installazione deve inviare una notifica all'utente.</span><span class="sxs-lookup"><span data-stu-id="88e72-135">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="88e72-136">Se un componente aggiuntivo più recente ha sovrascritto il componente aggiuntivo precedente, dovrebbe essere possibile ripristinare la funzionalità del componente aggiuntivo precedente e renderlo di nuovo il componente aggiuntivo predefinito per il tipo di file o l'archivio.</span><span class="sxs-lookup"><span data-stu-id="88e72-136">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type or store again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88e72-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88e72-137">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="88e72-138">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="88e72-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="88e72-139">Sviluppo di componenti aggiuntivi IFilter</span><span class="sxs-lookup"><span data-stu-id="88e72-139">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="88e72-140">Sviluppo di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="88e72-140">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

<span data-ttu-id="88e72-141">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="88e72-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="88e72-142">**IFilter**</span><span class="sxs-lookup"><span data-stu-id="88e72-142">**IFilter**</span></span>](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
