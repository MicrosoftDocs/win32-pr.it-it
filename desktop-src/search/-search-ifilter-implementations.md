---
description: Microsoft fornisce diversi filtri standard con Windows Search. I client chiamano questi gestori di filtro (che sono implementazioni dell'interfaccia IFilter) per estrarre testo e proprietà da un documento.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Gestori di filtri forniti con Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128567"
---
# <a name="filter-handlers-that-ship-with-windows"></a><span data-ttu-id="d660c-104">Gestori di filtri forniti con Windows</span><span class="sxs-lookup"><span data-stu-id="d660c-104">Filter Handlers that Ship with Windows</span></span>

<span data-ttu-id="d660c-105">Microsoft fornisce diversi filtri standard con Windows Search.</span><span class="sxs-lookup"><span data-stu-id="d660c-105">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="d660c-106">I client chiamano questi gestori di filtro (che sono implementazioni dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) per estrarre testo e proprietà da un documento.</span><span class="sxs-lookup"><span data-stu-id="d660c-106">Clients call these filter handlers (which are implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) to extract text and properties from a document.</span></span>

<span data-ttu-id="d660c-107">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="d660c-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="d660c-108">Note sull'implementazione di Windows Search</span><span class="sxs-lookup"><span data-stu-id="d660c-108">Windows Search Implementation Notes</span></span>](#windows-search-implementation-notes)
  - [<span data-ttu-id="d660c-109">Implementazione di Windows 7 e 10</span><span class="sxs-lookup"><span data-stu-id="d660c-109">Windows 7 and 10 Implementation</span></span>](#windows-7-and-10-implementation)
  - [<span data-ttu-id="d660c-110">Implementazione di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d660c-110">Windows Vista Implementation</span></span>](#windows-vista-implementation)
  - [<span data-ttu-id="d660c-111">Implementazione legacy</span><span class="sxs-lookup"><span data-stu-id="d660c-111">Legacy Implementation</span></span>](#legacy-implementation)
- [<span data-ttu-id="d660c-112">Filtri di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="d660c-112">Windows Search Filters</span></span>](#filter-handlers-that-ship-with-windows)
  - [<span data-ttu-id="d660c-113">Gestore filtro MIME</span><span class="sxs-lookup"><span data-stu-id="d660c-113">MIME Filter Handler</span></span>](#mime-filter-handler)
  - [<span data-ttu-id="d660c-114">Gestore filtro HTML</span><span class="sxs-lookup"><span data-stu-id="d660c-114">HTML Filter Handler</span></span>](#html-filter-handler)
  - [<span data-ttu-id="d660c-115">Gestore filtro documenti</span><span class="sxs-lookup"><span data-stu-id="d660c-115">Document Filter Handler</span></span>](#document-filter-handler)
  - [<span data-ttu-id="d660c-116">Gestore filtro testo normale</span><span class="sxs-lookup"><span data-stu-id="d660c-116">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)
  - [<span data-ttu-id="d660c-117">Gestore di filtro binario o null</span><span class="sxs-lookup"><span data-stu-id="d660c-117">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler)
- [<span data-ttu-id="d660c-118">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="d660c-118">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="d660c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d660c-119">Related topics</span></span>](#related-topics)

## <a name="windows-search-implementation-notes"></a><span data-ttu-id="d660c-120">Note sull'implementazione di Windows Search</span><span class="sxs-lookup"><span data-stu-id="d660c-120">Windows Search Implementation Notes</span></span>

<span data-ttu-id="d660c-121">In Windows 7 e versioni successive, i filtri scritti nel codice gestito vengono bloccati in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="d660c-121">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="d660c-122">I filtri devono essere scritti in codice nativo a causa di potenziali problemi di controllo delle versioni di CLR con il processo di esecuzione di più componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="d660c-122">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="windows-7-and-10-implementation"></a><span data-ttu-id="d660c-123">Implementazione di Windows 7 e 10</span><span class="sxs-lookup"><span data-stu-id="d660c-123">Windows 7 and 10 Implementation</span></span>

<span data-ttu-id="d660c-124">In Windows 7 e versioni successive è presente un nuovo comportamento che si verifica quando si registra un gestore di filtro, un gestore di proprietà o una nuova estensione.</span><span class="sxs-lookup"><span data-stu-id="d660c-124">In Windows 7 and later, there is new behavior that occurs when registering a filter handler, property handler, or new extension.</span></span> <span data-ttu-id="d660c-125">Quando viene installato un nuovo gestore di proprietà e/o un gestore di filtro, i file con le estensioni corrispondenti vengono reindicizzati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d660c-125">When a new property handler and/or filter handler is installed, files with the corresponding extensions are automatically re-indexed.</span></span>

<span data-ttu-id="d660c-126">In Windows 7 e versioni successive, è consigliabile installare un gestore di filtri insieme ai gestori di proprietà corrispondenti e registrare il gestore di filtro prima del gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d660c-126">In Windows 7 and later, we recommend that you install a filter handler in conjunction with its corresponding property handlers, and that you register the filter handler before the property handler.</span></span> <span data-ttu-id="d660c-127">La registrazione del gestore delle proprietà avvia la reindicizzazione immediata dei file indicizzati in precedenza senza prima richiedere un riavvio e sfrutta tutti i gestori di filtro precedentemente registrati ai fini dell'indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="d660c-127">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a restart, and takes advantage of any previously registered filter handlers for the purpose of content indexing.</span></span>

<span data-ttu-id="d660c-128">Se solo un gestore di filtro viene installato senza un gestore di proprietà corrispondente, la reindicizzazione automatica viene eseguita dopo il riavvio del servizio di indicizzazione o il riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="d660c-128">If only a filter handler is installed without a corresponding property handler, then automatic re-indexing occurs either after a restart of the indexing service, or a restart of the system.</span></span>

<span data-ttu-id="d660c-129">Per i flag di descrizione della proprietà specifici di Windows 7, vedere gli argomenti di riferimento seguenti: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [tipo di PROPDESC \_ COLUMNINDEX \_ ](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) e [ \_ \_ flag PROPDESC SEARCHINFO](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span><span class="sxs-lookup"><span data-stu-id="d660c-129">For property description flags specific to Windows 7, see the following reference topics: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC\_COLUMNINDEX\_TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) and [PROPDESC\_SEARCHINFO\_FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span></span>

### <a name="windows-vista-implementation"></a><span data-ttu-id="d660c-130">Implementazione di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d660c-130">Windows Vista Implementation</span></span>

<span data-ttu-id="d660c-131">In Windows Vista e versioni precedenti, l'installazione di un gestore di proprietà o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) non avvia una reindicizzazione degli elementi esistenti a meno che un fornitore di software indipendente (ISV) non chiami in modo esplicito una ricompilazione o una reindicizzazione degli URL corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="d660c-131">In Windows Vista and earlier, installing an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or property handler does not initiate a re-indexing of existing items unless an independent software vendor (ISV) explicitly calls a rebuild or re-indexing of matching URLs.</span></span>

<span data-ttu-id="d660c-132">Esistono due principali differenze tra le applicazioni legacy, ad esempio il servizio di indicizzazione e le applicazioni più recenti, come Windows Search, di cui è necessario tenere conto quando si implementano i filtri:</span><span class="sxs-lookup"><span data-stu-id="d660c-132">There are two major differences between legacy applications like Indexing Service and newer applications like Windows Search that you should be aware of when implementing filters:</span></span>

- <span data-ttu-id="d660c-133">Utilizzo dell'interfaccia [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) .</span><span class="sxs-lookup"><span data-stu-id="d660c-133">Use of the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface.</span></span>
- <span data-ttu-id="d660c-134">Uso dei gestori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d660c-134">Use of property handlers.</span></span>

<span data-ttu-id="d660c-135">Per prima cosa, Windows Vista e Windows Search 3,0 e versioni successive richiedono l'uso di [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) per i motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d660c-135">First, Windows Vista and Windows Search 3.0 and later require you use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) for the following reasons:</span></span>

- <span data-ttu-id="d660c-136">Per garantire prestazioni e compatibilità futura.</span><span class="sxs-lookup"><span data-stu-id="d660c-136">To ensure performance and future compatibility.</span></span>
- <span data-ttu-id="d660c-137">Per aumentare la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d660c-137">To help increase security.</span></span> <span data-ttu-id="d660c-138">I filtri implementati con [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) sono più sicuri perché il contesto in cui viene eseguito il filtro non necessita dei diritti per aprire i file sul disco o sulla rete.</span><span class="sxs-lookup"><span data-stu-id="d660c-138">Filters implemented with [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) are more secure because the context in which the filter runs does not need the rights to open files on the disk or over the network.</span></span>

<span data-ttu-id="d660c-139">Mentre Windows Search USA solo [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), è anche possibile includere nell' [interfaccia IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) e/o nelle implementazioni dell' [interfaccia IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) nei filtri per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="d660c-139">While Windows Search uses only [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), you can also include [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and/or [IPersistStorage Interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) implementations in your filters for backward compatibility.</span></span>

<span data-ttu-id="d660c-140">La seconda differenza principale è che Windows Vista e Windows Search 3,0 e versioni successive dispongono di un nuovo [sistema di proprietà](../properties/building-property-handlers.md) che utilizza i gestori di proprietà per enumerare le proprietà degli elementi.</span><span class="sxs-lookup"><span data-stu-id="d660c-140">The second major difference is that Windows Vista and Windows Search 3.0 and later have a new [Property System](../properties/building-property-handlers.md) that uses property handlers to enumerate properties of items.</span></span>

<span data-ttu-id="d660c-141">Tuttavia, in alcuni casi è necessario implementare un filtro che gestisce il contenuto e le proprietà per:</span><span class="sxs-lookup"><span data-stu-id="d660c-141">However, there are times when you need to implement a filter that handles both content and properties in order to:</span></span>

- <span data-ttu-id="d660c-142">Supportano le implementazioni di MSSearch legacy.</span><span class="sxs-lookup"><span data-stu-id="d660c-142">Support legacy MSSearch implementations.</span></span>
- <span data-ttu-id="d660c-143">Attraversare i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="d660c-143">Traverse links.</span></span>
- <span data-ttu-id="d660c-144">Mantieni le informazioni sulla lingua.</span><span class="sxs-lookup"><span data-stu-id="d660c-144">Preserve language information.</span></span>
- <span data-ttu-id="d660c-145">Filtrare in modo ricorsivo gli elementi incorporati.</span><span class="sxs-lookup"><span data-stu-id="d660c-145">Recursively filter embedded items.</span></span>

<span data-ttu-id="d660c-146">In questi casi, è necessaria un'implementazione del filtro completo, incluso il metodo [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) per accedere ai valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d660c-146">In these situations, you need a full filter implementation, including the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method to access property values.</span></span>

### <a name="legacy-implementation"></a><span data-ttu-id="d660c-147">Implementazione legacy</span><span class="sxs-lookup"><span data-stu-id="d660c-147">Legacy Implementation</span></span>

<span data-ttu-id="d660c-148">Come accennato in precedenza, Windows Vista e Windows Search includono un nuovo sistema di proprietà che incapsula le proprietà di un elemento separate dal contenuto di un elemento.</span><span class="sxs-lookup"><span data-stu-id="d660c-148">As noted earlier, Windows Vista and Windows Search include a new property system that encapsulates an item's properties that is separate from an item's content.</span></span> <span data-ttu-id="d660c-149">Questo sistema di proprietà non esiste nelle versioni precedenti di Microsoft Windows Desktop Search (WDS) 2. x.</span><span class="sxs-lookup"><span data-stu-id="d660c-149">This property system does not exist in earlier versions of Microsoft Windows Desktop Search (WDS) 2.x.</span></span> <span data-ttu-id="d660c-150">Se il filtro deve supportare altre applicazioni, come descritto in precedenza, potrebbe essere necessario gestire sia il contenuto che le proprietà.</span><span class="sxs-lookup"><span data-stu-id="d660c-150">If your filter must support other applications as described above, it may need to handle both content and properties.</span></span>

<span data-ttu-id="d660c-151">Per ulteriori informazioni sullo sviluppo di un filtro compatibile, vedere gli argomenti seguenti, [IFilter (per le applicazioni legacy)](/windows/win32/api/filter/nn-filter-ifilter)e [sviluppo di componenti aggiuntivi di filtro (per le applicazioni legacy)](../lwef/-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="d660c-151">For more information on developing a compatible filter, see the following topics, [IFilter (for legacy applications)](/windows/win32/api/filter/nn-filter-ifilter), and [Developing Filter Add-ins (for legacy applications)](../lwef/-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="windows-search-filters"></a><span data-ttu-id="d660c-152">Filtri di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="d660c-152">Windows Search Filters</span></span>

<span data-ttu-id="d660c-153">Microsoft fornisce diversi filtri standard con Windows Search.</span><span class="sxs-lookup"><span data-stu-id="d660c-153">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="d660c-154">Il contenuto della dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  viene riepilogato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d660c-154">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  DLL contents are summarized in the following table.</span></span> <span data-ttu-id="d660c-155">Facendo clic sul nome di un gestore di filtro si passa alla descrizione dell'implementazione di **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="d660c-155">Clicking the name of a filter handler takes you to the description for that **IFilter** implementation.</span></span>

| <span data-ttu-id="d660c-156">Gestore filtro</span><span class="sxs-lookup"><span data-stu-id="d660c-156">Filter handler</span></span>                                                  | <span data-ttu-id="d660c-157">File filtrati</span><span class="sxs-lookup"><span data-stu-id="d660c-157">Files filtered</span></span>                              | <span data-ttu-id="d660c-158">DLL IFilter</span><span class="sxs-lookup"><span data-stu-id="d660c-158">IFilter DLL</span></span>  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [<span data-ttu-id="d660c-159">Gestore filtro MIME</span><span class="sxs-lookup"><span data-stu-id="d660c-159">MIME Filter Handler</span></span>](#mime-filter-handler)                     | <span data-ttu-id="d660c-160">Multipurpose Internet Mail Extension (MIME)</span><span class="sxs-lookup"><span data-stu-id="d660c-160">Multipurpose Internet Mail Extension (MIME)</span></span> | <span data-ttu-id="d660c-161">mimefilt.dll</span><span class="sxs-lookup"><span data-stu-id="d660c-161">mimefilt.dll</span></span> |
| [<span data-ttu-id="d660c-162">Gestore filtro HTML</span><span class="sxs-lookup"><span data-stu-id="d660c-162">HTML Filter Handler</span></span>](#html-filter-handler)                     | <span data-ttu-id="d660c-163">HTML 3,0 o versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="d660c-163">HTML 3.0 or earlier</span></span>                         | <span data-ttu-id="d660c-164">nlhtml.dll</span><span class="sxs-lookup"><span data-stu-id="d660c-164">nlhtml.dll</span></span>   |
| [<span data-ttu-id="d660c-165">Gestore filtro documenti</span><span class="sxs-lookup"><span data-stu-id="d660c-165">Document Filter Handler</span></span>](#document-filter-handler)             | <span data-ttu-id="d660c-166">Microsoft Word, Excel, PowerPoint</span><span class="sxs-lookup"><span data-stu-id="d660c-166">Microsoft Word, Excel, PowerPoint</span></span>           | <span data-ttu-id="d660c-167">offfilt.dll</span><span class="sxs-lookup"><span data-stu-id="d660c-167">offfilt.dll</span></span>  |
| [<span data-ttu-id="d660c-168">Gestore filtro testo normale</span><span class="sxs-lookup"><span data-stu-id="d660c-168">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)         | <span data-ttu-id="d660c-169">File di testo normale-IFilter predefinito</span><span class="sxs-lookup"><span data-stu-id="d660c-169">Plain text files - Default IFilter</span></span>          | <span data-ttu-id="d660c-170">query.dll</span><span class="sxs-lookup"><span data-stu-id="d660c-170">query.dll</span></span>    |
| [<span data-ttu-id="d660c-171">Gestore di filtro binario o null</span><span class="sxs-lookup"><span data-stu-id="d660c-171">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler) | <span data-ttu-id="d660c-172">File binari-IFilter null</span><span class="sxs-lookup"><span data-stu-id="d660c-172">Binary files - Null IFilter</span></span>                 | <span data-ttu-id="d660c-173">query.dll</span><span class="sxs-lookup"><span data-stu-id="d660c-173">query.dll</span></span>    |

### <a name="mime-filter-handler"></a><span data-ttu-id="d660c-174">Gestore filtro MIME</span><span class="sxs-lookup"><span data-stu-id="d660c-174">MIME Filter Handler</span></span>

<span data-ttu-id="d660c-175">Il gestore del filtro MIME (in mimefilt.dll) estrae le informazioni di testo e proprietà da file con estensioni. eml,. mht e. MHTML.</span><span class="sxs-lookup"><span data-stu-id="d660c-175">The MIME filter handler (in mimefilt.dll) extracts text and property information from files with the extensions .eml, .mht and .mhtml.</span></span>

### <a name="html-filter-handler"></a><span data-ttu-id="d660c-176">Gestore filtro HTML</span><span class="sxs-lookup"><span data-stu-id="d660c-176">HTML Filter Handler</span></span>

<span data-ttu-id="d660c-177">Il gestore del filtro HTML (in nlhtml.dll) estrae le informazioni di testo e proprietà dalla classe "HtmlFiles" in modo che possa essere indicizzata tramite la ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="d660c-177">The HTML filter handler (in nlhtml.dll) extracts text and property information from the class "htmlfiles" so that it can be indexed by Windows Search.</span></span> <span data-ttu-id="d660c-178">Per una descrizione dell'associazione tra [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e il tipo di file, vedere "ricerca della dll IFilter per un file" in [registrazione dei gestori di filtro](-search-ifilter-registering-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d660c-178">For a description of the association between [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and file type, see "Finding the IFilter DLL for a File" in [Registering Filter Handlers](-search-ifilter-registering-filters.md).</span></span>

<span data-ttu-id="d660c-179">È possibile usare la `META` funzionalità tag dei documenti HTML per inviare richieste di gestione speciali all' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)HTML.</span><span class="sxs-lookup"><span data-stu-id="d660c-179">You can use the `META` tag feature of HTML documents to convey special handling requests to the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter).</span></span> <span data-ttu-id="d660c-180">`META` i tag si verificano in prossimità dell'inizio di un file HTML all'interno dei `HEAD ... /HEAD` tag, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="d660c-180">`META` tags occur near the beginning of an html file within the `HEAD ... /HEAD` tags, as illustrated in the following example.</span></span>

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

<span data-ttu-id="d660c-181">Alcuni `META` tag HTML vengono automaticamente mappati a valori noti per set di proprietà e ID proprietà (PID), in modo che le query su queste proprietà effettuino ricerche nel contenuto mappato.</span><span class="sxs-lookup"><span data-stu-id="d660c-181">Some HTML `META` tags are automatically mapped to well known property set and property ID (property identifier (PID)) values so that queries on these properties will search the mapped contents.</span></span> <span data-ttu-id="d660c-182">Alcuni esempi sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d660c-182">Some examples are listed in the following table.</span></span> <span data-ttu-id="d660c-183">Per un elenco delle proprietà di sistema che è possibile usare per i formati di file, vedere [proprietà definite dal sistema per formati di file personalizzati](-shell-systemdefinedpropertiesforfileformats.md).</span><span class="sxs-lookup"><span data-stu-id="d660c-183">For a list of system properties that you can use for your file formats, see [System-Defined Properties for Custom File Formats](-shell-systemdefinedpropertiesforfileformats.md).</span></span>

| <span data-ttu-id="d660c-184">Esempio di proprietà</span><span class="sxs-lookup"><span data-stu-id="d660c-184">Property example</span></span>                              | <span data-ttu-id="d660c-185">Mapping a</span><span class="sxs-lookup"><span data-stu-id="d660c-185">Mapped to</span></span>                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d660c-186">meta Name = "Author" Content = "Ruth"</span><span class="sxs-lookup"><span data-stu-id="d660c-186">meta name="author" content="ruth"</span></span>             | <span data-ttu-id="d660c-187">Proprietà Author nel set di proprietà delle informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="d660c-187">The author property in the Summary Information property set.</span></span>            |
| <span data-ttu-id="d660c-188">meta Name = "Subject" Content = "elaborazione di testi"</span><span class="sxs-lookup"><span data-stu-id="d660c-188">meta name="subject" content="word processing"</span></span> | <span data-ttu-id="d660c-189">Proprietà Subject nel set di proprietà informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="d660c-189">The subject property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="d660c-190">meta Name = "keywords" Content = "Fonts, serif"</span><span class="sxs-lookup"><span data-stu-id="d660c-190">meta name="keywords" content="fonts, serif"</span></span>   | <span data-ttu-id="d660c-191">Proprietà della parola chiave nel set di proprietà delle informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="d660c-191">The keyword property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="d660c-192">meta Name = "ms. Category" Content = "fiction"</span><span class="sxs-lookup"><span data-stu-id="d660c-192">meta name="ms.category" content="fiction"</span></span>     | <span data-ttu-id="d660c-193">Proprietà Category nel set di proprietà informazioni di riepilogo del documento.</span><span class="sxs-lookup"><span data-stu-id="d660c-193">The category property in the document Summary Information property set.</span></span> |

<span data-ttu-id="d660c-194">Alcune funzionalità del [**IFILTER**](/windows/win32/api/filter/nn-filter-ifilter) HTML sono elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d660c-194">Some features of the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) are listed in the following table.</span></span>

[comment]: # (Questa tabella deve essere HTML per fare in modo che gli esempi vengano formattati correttamente)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d660c-196">Attività</span><span class="sxs-lookup"><span data-stu-id="d660c-196">Task</span></span></th>
<th><span data-ttu-id="d660c-197">Operazione</span><span class="sxs-lookup"><span data-stu-id="d660c-197">Action</span></span></th>
<th><span data-ttu-id="d660c-198">Esempio</span><span class="sxs-lookup"><span data-stu-id="d660c-198">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d660c-199">Creazione di abstract speciali da file</span><span class="sxs-lookup"><span data-stu-id="d660c-199">Creating special abstracts from files</span></span></td>
<td><span data-ttu-id="d660c-200">Usare il <code>META NAME=&quot;DESCRIPTION&quot;...</code> tag per indicare a <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> di usare la stringa che segue la <code>CONTENT</code> parola chiave come abstract del documento.</span><span class="sxs-lookup"><span data-stu-id="d660c-200">Use the <code>META NAME=&quot;DESCRIPTION&quot;...</code> tag to instruct the <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> to use the string following the <code>CONTENT</code> keyword as the document abstract.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d660c-201">Il processo di filtro può generare abstract per ogni file filtrato, che per impostazione predefinita è un set di caratteri all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="d660c-201">The filtering process can generate abstracts for each filtered file, which default to being a set of characters at the beginning of the file.</span></span>
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="d660c-202">Prevenzione del filtraggio di singoli file</span><span class="sxs-lookup"><span data-stu-id="d660c-202">Preventing individual files from being filtered</span></span></td>
<td><span data-ttu-id="d660c-203">Aggiungere un <code>meta name</code> tag al file.</span><span class="sxs-lookup"><span data-stu-id="d660c-203">Add a <code>meta name</code> tag to the file.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d660c-204">Impostazione del codice lingua per un file (per garantire che il sistema scelga i Word breaker e i file di parole non significative corretti)</span><span class="sxs-lookup"><span data-stu-id="d660c-204">Setting the language code for a file (to ensure the system chooses the correct language word breakers and noise word files)</span></span></td>
<td><span data-ttu-id="d660c-205">Aggiungere il <code>meta name</code> tag seguente al file, in cui il campo contenuto specifica il codice lingua appropriato (in caratteri o usando il valore delle impostazioni locali).</span><span class="sxs-lookup"><span data-stu-id="d660c-205">Add the following <code>meta name</code> tag to the file, where the content field specifies the appropriate language code (either in characters or by using the locale value).</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a><span data-ttu-id="d660c-206">Gestore filtro documenti</span><span class="sxs-lookup"><span data-stu-id="d660c-206">Document Filter Handler</span></span>

<span data-ttu-id="d660c-207">Il gestore del filtro del documento (in offilt.dll) filtra i file per alcune estensioni dei documenti Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d660c-207">The Document filter handler (in offilt.dll) filters files for some extensions of documents in Microsoft Office.</span></span> <span data-ttu-id="d660c-208">Sono inclusi i file con estensione doc, mdb, PPT e XLT, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="d660c-208">These include files with the extensions .doc, .mdb, .ppt, and .xlt, for example.</span></span>

### <a name="plain-text-filter-handler"></a><span data-ttu-id="d660c-209">Gestore filtro testo normale</span><span class="sxs-lookup"><span data-stu-id="d660c-209">Plain Text Filter Handler</span></span>

<span data-ttu-id="d660c-210">Per i file di testo normale, in Windows Search viene utilizzato il gestore del filtro del testo, che consente di filtrare le proprietà di sistema, ad esempio i nomi dei file, e il contenuto di un file.</span><span class="sxs-lookup"><span data-stu-id="d660c-210">For plain-text files, Windows Search uses the text filter handler, which filters both the system properties (such as file names) and the contents of a file.</span></span> <span data-ttu-id="d660c-211">Quando un tipo di file non dispone di un'associazione [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) nel registro di sistema, Windows Search indicizza solo le proprietà della Shell per il file.</span><span class="sxs-lookup"><span data-stu-id="d660c-211">When a file type does not have an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) association in the registry, Windows Search indexes only the Shell properties for the file.</span></span> <span data-ttu-id="d660c-212">Tuttavia, l'utente può utilizzare le **Opzioni avanzate** nel pannello di controllo **Opzioni di indicizzazione** per **indicizzare proprietà** o **proprietà di indice e contenuto del file**.</span><span class="sxs-lookup"><span data-stu-id="d660c-212">However the user can use the **Advanced Options** in the **Indexing Options** control panel to **Index Properties** or **Index Properties and File Contents**.</span></span>

![screenshot che mostra la finestra di dialogo Opzioni avanzate](images/ifilteradvancedoptions.png)

<span data-ttu-id="d660c-214">Se l'utente sceglie questa opzione per un tipo di file senza un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)associato, viene utilizzato il gestore del filtro del testo per estrarre il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="d660c-214">If the user chooses this option for a file type without an associated [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), the text filter handler is used to extract the content of the file.</span></span> <span data-ttu-id="d660c-215">Il gestore del filtro del testo non "comprende" qualsiasi formato di documento; Quando si filtra il contenuto di un file, il file viene considerato come una sequenza di caratteri.</span><span class="sxs-lookup"><span data-stu-id="d660c-215">The text filter handler does not "understand" any document format; when filtering the contents of a file, it treats the file as a sequence of characters.</span></span> <span data-ttu-id="d660c-216">Verifica il contrassegno Unicode per l'ordine dei byte all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="d660c-216">It does check for the Unicode byte-order mark at the beginning of the file.</span></span>

### <a name="binary-or-null-filter-handler"></a><span data-ttu-id="d660c-217">Gestore di filtro binario o null</span><span class="sxs-lookup"><span data-stu-id="d660c-217">Binary or Null Filter Handler</span></span>

<span data-ttu-id="d660c-218">Quando viene rilevato un file binario registrato, viene utilizzato il gestore di filtri null.</span><span class="sxs-lookup"><span data-stu-id="d660c-218">When a registered binary file is encountered, the null filter handler is used.</span></span> <span data-ttu-id="d660c-219">Il gestore di filtro null recupera solo le proprietà di sistema.</span><span class="sxs-lookup"><span data-stu-id="d660c-219">The null filter handler retrieves only the system properties.</span></span> <span data-ttu-id="d660c-220">Il contenuto di un file binario non viene filtrato.</span><span class="sxs-lookup"><span data-stu-id="d660c-220">The contents of a binary file are not filtered.</span></span> <span data-ttu-id="d660c-221">Esempi di proprietà di sistema sono **filename**, **LastWriteTime**, **Filesize** e **Attributes**.</span><span class="sxs-lookup"><span data-stu-id="d660c-221">Examples of system properties are **FileName**, **LastWriteTime**, **FileSize**, and **Attributes**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d660c-222">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="d660c-222">Additional Resources</span></span>

- <span data-ttu-id="d660c-223">Nell'esempio di codice [IFilterSample](-search-sample-ifiltersample.md) , disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="d660c-223">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="d660c-224">Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d660c-224">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="d660c-225">Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="d660c-225">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="d660c-226">Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d660c-226">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d660c-227">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d660c-227">Related topics</span></span>

[<span data-ttu-id="d660c-228">Sviluppo di gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="d660c-228">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="d660c-229">Informazioni sui gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="d660c-229">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="d660c-230">Procedure consigliate per la creazione di gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="d660c-230">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="d660c-231">Restituzione di proprietà da un gestore di filtro</span><span class="sxs-lookup"><span data-stu-id="d660c-231">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="d660c-232">Implementazione di gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="d660c-232">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="d660c-233">Registrazione di gestori di filtro</span><span class="sxs-lookup"><span data-stu-id="d660c-233">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)

[<span data-ttu-id="d660c-234">Test di gestori filtro</span><span class="sxs-lookup"><span data-stu-id="d660c-234">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
