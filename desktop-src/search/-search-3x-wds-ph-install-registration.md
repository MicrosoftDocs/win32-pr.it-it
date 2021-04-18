---
description: L'installazione di un gestore di protocollo comporta la copia delle DLL in una posizione appropriata nella directory programmi e quindi la registrazione del gestore del protocollo tramite il registro di sistema.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Installazione e registrazione di gestori di protocollo (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306180"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a><span data-ttu-id="e73ec-103">Installazione e registrazione di gestori di protocollo (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="e73ec-103">Installing and Registering Protocol Handlers (Windows Search)</span></span>

<span data-ttu-id="e73ec-104">L'installazione di un gestore di protocollo comporta la copia delle DLL in una posizione appropriata nella directory programmi e quindi la registrazione del gestore del protocollo tramite il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e73ec-104">Installing a protocol handler involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the protocol handler through the registry.</span></span> <span data-ttu-id="e73ec-105">L'applicazione di installazione può anche aggiungere una radice di ricerca e regole di ambito per definire un ambito di ricerca per indicizzazione predefinito per l'origine dati della shell.</span><span class="sxs-lookup"><span data-stu-id="e73ec-105">The installation application can also add a search root and scope rules to define a default crawl scope for the Shell data source.</span></span>

<span data-ttu-id="e73ec-106">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="e73ec-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e73ec-107">Informazioni sugli URL</span><span class="sxs-lookup"><span data-stu-id="e73ec-107">About URLs</span></span>](#about-urls)
-   [<span data-ttu-id="e73ec-108">Implementazione delle interfacce del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-108">Implementing Protocol Handler Interfaces</span></span>](#implementing-protocol-handler-interfaces)
    -   [<span data-ttu-id="e73ec-109">ISearchProtocol e ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="e73ec-109">ISearchProtocol and ISearchProtocol2</span></span>](#isearchprotocol-and-isearchprotocol2)
    -   [<span data-ttu-id="e73ec-110">IUrlAccessor, IUrlAccessor2, IUrlAccessor3 e IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="e73ec-110">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [<span data-ttu-id="e73ec-111">IProtocolHandlerSite</span><span class="sxs-lookup"><span data-stu-id="e73ec-111">IProtocolHandlerSite</span></span>](#iprotocolhandlersite)
-   [<span data-ttu-id="e73ec-112">Implementazione di gestori di filtri per i contenitori</span><span class="sxs-lookup"><span data-stu-id="e73ec-112">Implementing Filter Handlers for Containers</span></span>](#implementing-filter-handlers-for-containers)
-   [<span data-ttu-id="e73ec-113">Installazione e registrazione di un gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-113">Installing and Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="e73ec-114">Linee guida per la registrazione di un gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-114">Guidelines for Registering a Protocol Handler</span></span>](#guidelines-for-registering-a-protocol-handler)
    -   [<span data-ttu-id="e73ec-115">Registrazione di un gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-115">Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="e73ec-116">Registrazione del gestore del tipo di file del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-116">Registering the Protocol Handler's File Type Handler</span></span>](#registering-the-protocol-handlers-file-type-handler)
-   [<span data-ttu-id="e73ec-117">Verifica dell'indicizzazione degli elementi</span><span class="sxs-lookup"><span data-stu-id="e73ec-117">Ensuring that Your Items are Indexed</span></span>](#ensuring-that-your-items-are-indexed)
-   [<span data-ttu-id="e73ec-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e73ec-118">Related topics</span></span>](#related-topics)

## <a name="about-urls"></a><span data-ttu-id="e73ec-119">Informazioni sugli URL</span><span class="sxs-lookup"><span data-stu-id="e73ec-119">About URLs</span></span>

<span data-ttu-id="e73ec-120">Windows Search USA gli URL per identificare in modo univoco gli elementi nella gerarchia dell'origine dati della shell.</span><span class="sxs-lookup"><span data-stu-id="e73ec-120">Windows Search uses URLs to uniquely identify items in the hierarchy of your Shell data source.</span></span> <span data-ttu-id="e73ec-121">L'URL che rappresenta il primo nodo della gerarchia è denominato radice di [ricerca](-search-3x-wds-extidx-csm-searchroots.md); Windows Search inizierà l'indicizzazione alla radice di ricerca, richiedendo che il gestore di protocollo enumera i collegamenti figlio per ogni URL.</span><span class="sxs-lookup"><span data-stu-id="e73ec-121">The URL that is the first node in the hierarchy is called the [search root](-search-3x-wds-extidx-csm-searchroots.md); Windows Search will begin indexing at the search root, requesting that the protocol handler enumerate child links for each URL.</span></span>

<span data-ttu-id="e73ec-122">La struttura di URL tipica è la seguente:</span><span class="sxs-lookup"><span data-stu-id="e73ec-122">The typical URL structure is:</span></span>


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



<span data-ttu-id="e73ec-123">La sintassi dell'URL è descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e73ec-123">The URL syntax is described in the following table.</span></span>



| <span data-ttu-id="e73ec-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e73ec-124">Syntax</span></span>           | <span data-ttu-id="e73ec-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e73ec-125">Description</span></span>                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | <span data-ttu-id="e73ec-126">Identifica il gestore di protocollo da richiamare per l'URL.</span><span class="sxs-lookup"><span data-stu-id="e73ec-126">Identifies which protocol handler to invoke for the URL.</span></span>                                                                                                                                                           |
| <span data-ttu-id="e73ec-127">{SID utente}</span><span class="sxs-lookup"><span data-stu-id="e73ec-127">{user SID}</span></span>       | <span data-ttu-id="e73ec-128">Identifica il contesto di sicurezza dell'utente in cui viene chiamato il gestore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="e73ec-128">Identifies the user security context under which the protocol handler is called.</span></span> <span data-ttu-id="e73ec-129">Se non viene identificato alcun ID di sicurezza utente (SID), il gestore di protocollo viene chiamato nel contesto di sicurezza del servizio di sistema.</span><span class="sxs-lookup"><span data-stu-id="e73ec-129">If no user security identifier (SID) is identified, the protocol handler is called in the security context of the system service.</span></span> |
| <path>     | <span data-ttu-id="e73ec-130">Definisce la gerarchia dell'archivio in cui ogni barra ('/') è un separatore tra i nomi delle cartelle.</span><span class="sxs-lookup"><span data-stu-id="e73ec-130">Defines the hierarchy of the store, where each forward slash ('/') is a separator between folder names.</span></span>                                                                                                            |
| <ItemID>   | <span data-ttu-id="e73ec-131">Rappresenta una stringa univoca che identifica l'elemento figlio, ad esempio il nome del file.</span><span class="sxs-lookup"><span data-stu-id="e73ec-131">Represents a unique string that identifies the child item (for example, the file name).</span></span>                                                                                                                            |



 

<span data-ttu-id="e73ec-132">L'indicizzatore di ricerca di Windows taglia la barra finale dagli URL.</span><span class="sxs-lookup"><span data-stu-id="e73ec-132">The Windows Search Indexer trims the final slash from URLs.</span></span> <span data-ttu-id="e73ec-133">Di conseguenza, non è possibile fare affidamento sulla presenza di una barra finale per identificare una directory rispetto a un elemento.</span><span class="sxs-lookup"><span data-stu-id="e73ec-133">As a result you cannot rely on the existence of a final slash to identify a directory versus an item.</span></span> <span data-ttu-id="e73ec-134">Il gestore di protocollo deve essere in grado di gestire questa sintassi dell'URL.</span><span class="sxs-lookup"><span data-stu-id="e73ec-134">Your protocol handler must be able to handle this URL syntax.</span></span> <span data-ttu-id="e73ec-135">Verificare che il nome del protocollo selezionato per identificare l'origine dati della shell non sia in conflitto con quelli correnti.</span><span class="sxs-lookup"><span data-stu-id="e73ec-135">Ensure that the protocol name that you select to identify your Shell data source does not conflict with current ones.</span></span> <span data-ttu-id="e73ec-136">Questa convenzione di denominazione è consigliata: `companyName.scheme` .</span><span class="sxs-lookup"><span data-stu-id="e73ec-136">We recommend this naming convention: `companyName.scheme`.</span></span>

<span data-ttu-id="e73ec-137">Per ulteriori informazioni sulla creazione di un'origine dati della shell, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e73ec-137">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

## <a name="implementing-protocol-handler-interfaces"></a><span data-ttu-id="e73ec-138">Implementazione delle interfacce del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-138">Implementing Protocol Handler Interfaces</span></span>

<span data-ttu-id="e73ec-139">Per la creazione di un gestore di protocollo è necessaria l'implementazione delle tre interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="e73ec-139">Creating a protocol handler requires the implementation of the following three interfaces:</span></span>

-   <span data-ttu-id="e73ec-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) per la gestione di oggetti UrlAccessor.</span><span class="sxs-lookup"><span data-stu-id="e73ec-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects.</span></span>
-   <span data-ttu-id="e73ec-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) per esporre le proprietà e identificare i filtri appropriati per gli elementi nell'origine dati della shell.</span><span class="sxs-lookup"><span data-stu-id="e73ec-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) to expose properties and identify appropriate filters for items in the Shell data source.</span></span>
-   <span data-ttu-id="e73ec-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) per filtrare i file proprietari o per enumerare e filtrare i file archiviati in modo gerarchico.</span><span class="sxs-lookup"><span data-stu-id="e73ec-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span>

<span data-ttu-id="e73ec-143">Oltre alle tre interfacce obbligatorie elencate, le altre interfacce sono facoltative ed è possibile implementare qualsiasi interfaccia facoltativa più appropriata per l'attività.</span><span class="sxs-lookup"><span data-stu-id="e73ec-143">Other than the three mandatory interfaces listed, the other interfaces are optional, and you are at liberty to implement whichever optional interfaces are most appropriate for the task at hand.</span></span>

### <a name="isearchprotocol-and-isearchprotocol2"></a><span data-ttu-id="e73ec-144">ISearchProtocol e ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="e73ec-144">ISearchProtocol and ISearchProtocol2</span></span>

<span data-ttu-id="e73ec-145">Le interfacce SearchProtocol inizializzano e gestiscono gli oggetti UrlAccessor del gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="e73ec-145">The SearchProtocol interfaces initialize and manage your protocol handler UrlAccessor objects.</span></span> <span data-ttu-id="e73ec-146">L'interfaccia [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) è un'estensione facoltativa di [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)e include un metodo aggiuntivo per specificare altre informazioni sull'utente e sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="e73ec-146">The [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) interface is an optional extension of [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol), and includes an extra method to specify more information about the user and the item.</span></span>

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a><span data-ttu-id="e73ec-147">IUrlAccessor, IUrlAccessor2, IUrlAccessor3 e IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="e73ec-147">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>

<span data-ttu-id="e73ec-148">Le interfacce [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) sono descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e73ec-148">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces are described in the following table.</span></span>



| <span data-ttu-id="e73ec-149">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="e73ec-149">Interface</span></span>                                                 | <span data-ttu-id="e73ec-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e73ec-150">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e73ec-151">**IUrlAccessor**</span><span class="sxs-lookup"><span data-stu-id="e73ec-151">**IUrlAccessor**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | <span data-ttu-id="e73ec-152">Per un URL specificato, l'interfaccia [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) fornisce l'accesso alle proprietà dell'elemento esposto nell'URL.</span><span class="sxs-lookup"><span data-stu-id="e73ec-152">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interface provides access to the properties of the item that is exposed in the URL.</span></span> <span data-ttu-id="e73ec-153">Può inoltre associare tali proprietà a un filtro specifico del gestore di protocollo, ovvero un filtro diverso da quello associato al nome del file.</span><span class="sxs-lookup"><span data-stu-id="e73ec-153">It can also bind those properties to a protocol handler-specific filter (that is, a filter other than the one associated with the file name).</span></span> |
| <span data-ttu-id="e73ec-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="e73ec-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (optional)</span></span> | <span data-ttu-id="e73ec-155">L'interfaccia [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) estende [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) con metodi che ottengono una tabella codici per le proprietà dell'elemento e il relativo URL di visualizzazione e che ottengono il tipo di elemento nell'URL (documento o directory).</span><span class="sxs-lookup"><span data-stu-id="e73ec-155">The [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) interface extends [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) with methods that get a code page for the item's properties and its display URL, and that get the type of item in the URL (document or directory).</span></span>                                    |
| <span data-ttu-id="e73ec-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="e73ec-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (optional)</span></span> | <span data-ttu-id="e73ec-157">L'interfaccia [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) estende [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) con un metodo che ottiene una matrice di SID utente, consentendo all'host del protocollo di ricerca di rappresentare questi utenti per indicizzare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="e73ec-157">The [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface extends [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) with a method that gets an array of user SIDs, enabling the search protocol host to impersonate these users to index the item.</span></span>                                                      |
| <span data-ttu-id="e73ec-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="e73ec-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (optional)</span></span> | <span data-ttu-id="e73ec-159">L'interfaccia [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) estende la funzionalità dell'interfaccia [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) con un metodo che identifica se il contenuto dell'elemento deve essere indicizzato.</span><span class="sxs-lookup"><span data-stu-id="e73ec-159">The [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) interface extends the functionality of the [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface with a method that identifies whether the content of the item should be indexed.</span></span>                                                                 |



 

<span data-ttu-id="e73ec-160">Viene creata un'istanza dell'oggetto UrlAccessor che viene inizializzato da un oggetto SearchProtocol.</span><span class="sxs-lookup"><span data-stu-id="e73ec-160">The UrlAccessor object is instantiated and initialized by a SearchProtocol object.</span></span> <span data-ttu-id="e73ec-161">Le interfacce [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) forniscono l'accesso a informazioni importanti tramite i metodi descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e73ec-161">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces provide access to important pieces of information through the methods described in the following table.</span></span>



| <span data-ttu-id="e73ec-162">Metodo</span><span class="sxs-lookup"><span data-stu-id="e73ec-162">Method</span></span>                                                                                        | <span data-ttu-id="e73ec-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e73ec-163">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e73ec-164">**IUrlAccessor:: GetLastModified**</span><span class="sxs-lookup"><span data-stu-id="e73ec-164">**IUrlAccessor::GetLastModified**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | <span data-ttu-id="e73ec-165">Restituisce l'ora dell'Ultima modifica apportata all'URL.</span><span class="sxs-lookup"><span data-stu-id="e73ec-165">Returns the time that the URL was last modified.</span></span> <span data-ttu-id="e73ec-166">Se questa volta è più recente dell'ultima volta in cui l'indicizzatore ha elaborato questo URL, vengono chiamati i gestori di filtro (implementazioni dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) per estrarre i dati modificati (possibilmente) per tale elemento.</span><span class="sxs-lookup"><span data-stu-id="e73ec-166">If this time is more recent than the last time the indexer processed this URL, filter handlers (implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) are called to extract the (possibly) changed data for that item.</span></span> <span data-ttu-id="e73ec-167">Gli orari modificati per le directory vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="e73ec-167">Modified times for directories are ignored.</span></span> |
| [<span data-ttu-id="e73ec-168">**IUrlAccessor:: directory**</span><span class="sxs-lookup"><span data-stu-id="e73ec-168">**IUrlAccessor::IsDirectory**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | <span data-ttu-id="e73ec-169">Indica se l'URL rappresenta una cartella contenente un URL figlio.</span><span class="sxs-lookup"><span data-stu-id="e73ec-169">Identifies whether the URL represents a folder containing a child URLs.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="e73ec-170">**IUrlAccessor::BindToStream**</span><span class="sxs-lookup"><span data-stu-id="e73ec-170">**IUrlAccessor::BindToStream**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | <span data-ttu-id="e73ec-171">Esegue l'associazione a un' [interfaccia IStream](/windows/win32/api/objidl/nn-objidl-istream) che rappresenta i dati di un file in un archivio dati personalizzato.</span><span class="sxs-lookup"><span data-stu-id="e73ec-171">Binds to an [IStream interface](/windows/win32/api/objidl/nn-objidl-istream) that represents the data of a file in a custom data store.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="e73ec-172">**IUrlAccessor::BindToFilter**</span><span class="sxs-lookup"><span data-stu-id="e73ec-172">**IUrlAccessor::BindToFilter**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | <span data-ttu-id="e73ec-173">Esegue l'associazione a un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)specifico del gestore di protocollo, che può esporre le proprietà per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="e73ec-173">Binds to a protocol handler-specific [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), which can expose properties for the item.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="e73ec-174">**IUrlAccessor4::ShouldIndexItemContent**</span><span class="sxs-lookup"><span data-stu-id="e73ec-174">**IUrlAccessor4::ShouldIndexItemContent**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | <span data-ttu-id="e73ec-175">Indica se il contenuto dell'elemento deve essere indicizzato.</span><span class="sxs-lookup"><span data-stu-id="e73ec-175">Identifies whether the content of the item should be indexed.</span></span>                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a><span data-ttu-id="e73ec-176">IProtocolHandlerSite</span><span class="sxs-lookup"><span data-stu-id="e73ec-176">IProtocolHandlerSite</span></span>

<span data-ttu-id="e73ec-177">L'interfaccia [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) viene utilizzata per creare un'istanza di un gestore di filtro, che è ospitato in un processo isolato.</span><span class="sxs-lookup"><span data-stu-id="e73ec-177">The [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) interface is used to instantiate a filter handler, which is hosted in an isolated process.</span></span> <span data-ttu-id="e73ec-178">Il gestore di filtri appropriato viene ottenuto per un identificatore di classe persistente (CLSID), una classe di archiviazione di documenti o un'estensione di file specificati.</span><span class="sxs-lookup"><span data-stu-id="e73ec-178">The appropriate filter handler is obtained for a specified persistent class identifier (CLSID), document storage class, or file name extension.</span></span> <span data-ttu-id="e73ec-179">Il vantaggio di chiedere al processo host di eseguire l'associazione a [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è che il processo host è in grado di gestire il processo di individuazione di un gestore di filtri appropriato e di controllare la sicurezza richiesta per la chiamata al gestore.</span><span class="sxs-lookup"><span data-stu-id="e73ec-179">The benefit of asking the host process to bind to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is that the host process can manage the process of locating an appropriate filter handler, and control the security involved in calling the handler.</span></span>

## <a name="implementing-filter-handlers-for-containers"></a><span data-ttu-id="e73ec-180">Implementazione di gestori di filtri per i contenitori</span><span class="sxs-lookup"><span data-stu-id="e73ec-180">Implementing Filter Handlers for Containers</span></span>

<span data-ttu-id="e73ec-181">Se si implementa un gestore di protocollo gerarchico, è necessario implementare un gestore di filtri per un contenitore che enumera gli URL figlio.</span><span class="sxs-lookup"><span data-stu-id="e73ec-181">If you are implementing a hierarchical protocol handler, then you must implement a filter handler for a container that enumerates child URLs.</span></span> <span data-ttu-id="e73ec-182">Un gestore di filtro è un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="e73ec-182">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span> <span data-ttu-id="e73ec-183">Il processo di enumerazione è un ciclo attraverso i metodi [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) e [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) dell'interfaccia **IFilter** . ogni URL figlio viene esposto come valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e73ec-183">The enumeration process is a loop through the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) and [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) methods of the **IFilter** interface; each child URL is exposed as the value of the property.</span></span>

<span data-ttu-id="e73ec-184">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) restituisce le proprietà del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e73ec-184">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns the properties of the container.</span></span> <span data-ttu-id="e73ec-185">Per enumerare gli URL figlio, **IFilter:: GetChunk** restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e73ec-185">To enumerate child URLs, **IFilter::GetChunk** returns either of the following:</span></span>

-   <span data-ttu-id="e73ec-186">[Pkey \_ \_UrlToIndex di ricerca](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="e73ec-186">[PKEY\_Search\_UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span></span>

    <span data-ttu-id="e73ec-187">URL dell'elemento senza l'ora dell'Ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="e73ec-187">The URL to the item without the last modified time.</span></span> <span data-ttu-id="e73ec-188">[**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) restituisce un PROPVARIANT contenente l'URL figlio.</span><span class="sxs-lookup"><span data-stu-id="e73ec-188">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing the child URL.</span></span>

-   <span data-ttu-id="e73ec-189">[Pkey \_ \_UrlToIndexWithModificationTime di ricerca](../properties/props-system-search-urltoindexwithmodificationtime.md):</span><span class="sxs-lookup"><span data-stu-id="e73ec-189">[PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):</span></span>

    <span data-ttu-id="e73ec-190">L'URL e l'ora dell'Ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="e73ec-190">The URL and the last modified time.</span></span> <span data-ttu-id="e73ec-191">[**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) restituisce un PROPVARIANT contenente un vettore dell'URL figlio e l'ora dell'Ultima modifica.</span><span class="sxs-lookup"><span data-stu-id="e73ec-191">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing a vector of the child URL and the last modified time.</span></span>

<span data-ttu-id="e73ec-192">La restituzione di [pkey \_ Search \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) è più efficiente perché l'indicizzatore può determinare immediatamente se l'elemento deve essere indicizzato senza chiamare i metodi [**ISearchProtocol:: CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) e [**IUrlAccessor:: GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) .</span><span class="sxs-lookup"><span data-stu-id="e73ec-192">Returning [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the [**ISearchProtocol::CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) and [**IUrlAccessor::GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) methods.</span></span>

<span data-ttu-id="e73ec-193">Nell'esempio di codice seguente viene illustrato come restituire la proprietà [ \_ \_ UrlToIndexWithModificationTime di ricerca pkey](../properties/props-system-search-urltoindexwithmodificationtime.md) .</span><span class="sxs-lookup"><span data-stu-id="e73ec-193">The following example code demonstrates how to return the [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) property.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e73ec-194">Copyright (c) Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="e73ec-194">Copyright (c) Microsoft Corporation.</span></span> <span data-ttu-id="e73ec-195">Tutti i diritti sono riservati.</span><span class="sxs-lookup"><span data-stu-id="e73ec-195">All rights reserved.</span></span>

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> <span data-ttu-id="e73ec-196">Un componente [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) del contenitore deve sempre enumerare tutti gli URL figlio anche se gli URL figlio non sono stati modificati, perché l'indicizzatore rileva le eliminazioni tramite il processo di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e73ec-196">A container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) component should always enumerate all child URLs even if the child URLs have not changed, because the indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="e73ec-197">Se l'output della data in [un \_ \_ UrlToIndexWithModificationTime di ricerca pkey](../properties/props-system-search-urltoindexwithmodificationtime.md) indica che i dati non sono stati modificati, l'indicizzatore non aggiorna i dati per tale URL.</span><span class="sxs-lookup"><span data-stu-id="e73ec-197">If the date output in a [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

## <a name="installing-and-registering-a-protocol-handler"></a><span data-ttu-id="e73ec-198">Installazione e registrazione di un gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-198">Installing and Registering a Protocol Handler</span></span>

<span data-ttu-id="e73ec-199">L'installazione dei gestori di protocollo comporta la copia delle DLL in un percorso appropriato nella directory programmi e la successiva registrazione delle DLL.</span><span class="sxs-lookup"><span data-stu-id="e73ec-199">Installing protocol handlers involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the DLL(s).</span></span> <span data-ttu-id="e73ec-200">I gestori di protocollo devono implementare la registrazione automatica per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e73ec-200">Protocol handlers should implement self-registration for installation.</span></span> <span data-ttu-id="e73ec-201">L'applicazione di installazione può anche aggiungere una radice di ricerca e regole di ambito per definire un ambito di ricerca per indicizzazione predefinito per l'origine dati della shell, che viene illustrato in [assicurandosi che gli elementi siano indicizzati](#ensuring-that-your-items-are-indexed) alla fine di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="e73ec-201">The installation application can also add a search root, and scope rules to define a default crawl scope for the Shell data source, which is discussed in [Ensuring that Your Items are Indexed](#ensuring-that-your-items-are-indexed) at the end of this topic.</span></span>

### <a name="guidelines-for-registering-a-protocol-handler"></a><span data-ttu-id="e73ec-202">Linee guida per la registrazione di un gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-202">Guidelines for Registering a Protocol Handler</span></span>

<span data-ttu-id="e73ec-203">Quando si registra un gestore di protocollo, attenersi alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="e73ec-203">You should follow these guidelines when registering a protocol handler:</span></span>

-   <span data-ttu-id="e73ec-204">Il programma di installazione deve usare il programma di installazione EXE o MSI.</span><span class="sxs-lookup"><span data-stu-id="e73ec-204">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="e73ec-205">È necessario fornire le note sulla versione.</span><span class="sxs-lookup"><span data-stu-id="e73ec-205">Release notes must be provided.</span></span>
-   <span data-ttu-id="e73ec-206">È necessario creare una voce di installazione applicazioni per ogni componente aggiuntivo installato.</span><span class="sxs-lookup"><span data-stu-id="e73ec-206">An Add/Remove Programs entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="e73ec-207">Il programma di installazione deve assumere tutte le impostazioni del registro di sistema per il tipo di file o l'archivio specifico che il componente aggiuntivo corrente riconosce.</span><span class="sxs-lookup"><span data-stu-id="e73ec-207">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="e73ec-208">Se un componente aggiuntivo precedente viene sovrascritto, il programma di installazione deve inviare una notifica all'utente.</span><span class="sxs-lookup"><span data-stu-id="e73ec-208">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="e73ec-209">Se un componente aggiuntivo più recente ha sovrascritto il componente aggiuntivo precedente, dovrebbe essere possibile ripristinare la funzionalità del componente aggiuntivo precedente e impostarlo di nuovo come componente aggiuntivo predefinito per quel tipo di file.</span><span class="sxs-lookup"><span data-stu-id="e73ec-209">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>
-   <span data-ttu-id="e73ec-210">Il programma di installazione deve definire un ambito di ricerca per indicizzazione predefinito per l'indicizzatore mediante l'aggiunta di una radice di ricerca e le regole dell'ambito mediante Gestione ambito ricerca per indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="e73ec-210">The installer should define a default crawl scope for the indexer by adding a search root, and scope rules using the Crawl Scope Manager (CSM).</span></span>

### <a name="registering-a-protocol-handler"></a><span data-ttu-id="e73ec-211">Registrazione di un gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-211">Registering a Protocol Handler</span></span>

<span data-ttu-id="e73ec-212">È necessario creare quattordici voci nel registro di sistema per registrare il componente gestore di protocollo, dove:</span><span class="sxs-lookup"><span data-stu-id="e73ec-212">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="e73ec-213">*Ver \_ IND \_ ProgID* è il ProgID indipendente dalla versione dell'implementazione del gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="e73ec-213">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="e73ec-214">*Ver \_ DEP \_ ProgID* è il ProgID dipendente dalla versione dell'implementazione del gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="e73ec-214">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="e73ec-215">*CLSID \_ 1* è il CLSID dell'implementazione del gestore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="e73ec-215">*CLSID\_1* is the CLSID of the protocol handler implementation.</span></span>

<span data-ttu-id="e73ec-216">**Per registrare un gestore di protocollo:**</span><span class="sxs-lookup"><span data-stu-id="e73ec-216">**To register a protocol handler:**</span></span>

1.  <span data-ttu-id="e73ec-217">Registrare la versione Independent ProgID con le chiavi e i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e73ec-217">Register the version independent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  <span data-ttu-id="e73ec-218">Registrare il ProgID dipendente dalla versione con le chiavi e i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e73ec-218">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="e73ec-219">Registrare il CLSID del gestore di protocollo con le chiavi e i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e73ec-219">Register the protocol handler's CLSID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  <span data-ttu-id="e73ec-220">Registrare il gestore di protocollo con Windows Search.</span><span class="sxs-lookup"><span data-stu-id="e73ec-220">Register the protocol handler with Windows Search.</span></span> <span data-ttu-id="e73ec-221">Nell'esempio seguente <Protocol Name> è il nome del protocollo stesso, ad esempio file, MAPI e così via:</span><span class="sxs-lookup"><span data-stu-id="e73ec-221">In the following example, <Protocol Name> is the name of the protocol itself, such as file, mapi, and so forth:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    <span data-ttu-id="e73ec-222">Prima di Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="e73ec-222">Prior to Windows Vista:</span></span>

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a><span data-ttu-id="e73ec-223">Registrazione del gestore del tipo di file del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-223">Registering the Protocol Handler's File Type Handler</span></span>

<span data-ttu-id="e73ec-224">È necessario creare due voci nel registro di sistema per registrare il gestore del tipo di file del gestore di protocollo (noto anche come estensione della Shell).</span><span class="sxs-lookup"><span data-stu-id="e73ec-224">You need to make two entries in the registry to register the protocol handler's file type handler (which is also known as a Shell extension).</span></span>

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a><span data-ttu-id="e73ec-225">Verifica dell'indicizzazione degli elementi</span><span class="sxs-lookup"><span data-stu-id="e73ec-225">Ensuring that Your Items are Indexed</span></span>

<span data-ttu-id="e73ec-226">Dopo aver implementato il gestore di protocollo, è necessario specificare gli elementi della shell da indicizzare nel gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="e73ec-226">After you have implemented your protocol handler, you must specify which Shell items your protocol handler is to index.</span></span> <span data-ttu-id="e73ec-227">È possibile utilizzare Gestione catalogo per avviare la reindicizzazione (per ulteriori informazioni, vedere Utilizzo di [gestione catalogo](-search-3x-wds-mngidx-catalog-manager.md)).</span><span class="sxs-lookup"><span data-stu-id="e73ec-227">You can use the Catalog Manager to initiate re-indexing (for more information, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md)).</span></span> <span data-ttu-id="e73ec-228">In alternativa, è possibile usare anche il gestore della ricerca per indicizzazione (CSM) per configurare le regole predefinite che indicano gli URL di cui l'indicizzatore vuole eseguire la ricerca per indicizzazione. per ulteriori informazioni, vedere [utilizzo di gestione ambito indicizzazione](-search-3x-wds-extidx-csm.md) e [gestione delle regole dell'ambito](-search-3x-wds-extidx-csm-scoperules.md).</span><span class="sxs-lookup"><span data-stu-id="e73ec-228">Or you can also use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl (for more information, see [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md) and [Managing Scope Rules](-search-3x-wds-extidx-csm-scoperules.md)).</span></span> <span data-ttu-id="e73ec-229">È anche possibile aggiungere una radice di ricerca (per altre informazioni, vedere [Managing Search Roots](-search-3x-wds-extidx-csm-searchroots.md)).</span><span class="sxs-lookup"><span data-stu-id="e73ec-229">You can also add a search root (for more information, see [Managing Search Roots](-search-3x-wds-extidx-csm-searchroots.md)).</span></span> <span data-ttu-id="e73ec-230">Un'altra opzione disponibile per l'utente consiste nel seguire la procedura descritta nell'esempio REINDEX negli [esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="e73ec-230">Another option available to you is to follow the procedure in the ReIndex sample in [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="e73ec-231">L'interfaccia [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) fornisce metodi che inviano una notifica al motore di ricerca dei contenitori per eseguire la ricerca per indicizzazione e/o guardare e gli elementi sottoposti a tali contenitori da includere o escludere durante la ricerca per indicizzazione</span><span class="sxs-lookup"><span data-stu-id="e73ec-231">The [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.</span></span> <span data-ttu-id="e73ec-232">In Windows 7 e versioni successive, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) estende **ISearchCrawlScopeManager** con il metodo [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) che ottiene la versione, che informa i client se lo stato del CSM è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="e73ec-232">In Windows 7 and later, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extends **ISearchCrawlScopeManager** with the [**ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) method that gets the version, which informs clients whether the state of the CSM has changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e73ec-233">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e73ec-233">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e73ec-234">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e73ec-234">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e73ec-235">Informazioni sui gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-235">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="e73ec-236">Sviluppo di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-236">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="e73ec-237">Notifica dell'indice delle modifiche</span><span class="sxs-lookup"><span data-stu-id="e73ec-237">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="e73ec-238">Aggiunta di icone e menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="e73ec-238">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="e73ec-239">Esempio di codice: estensioni della Shell per i gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-239">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="e73ec-240">Creazione di un connettore di ricerca per un gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-240">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="e73ec-241">Debug di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="e73ec-241">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
