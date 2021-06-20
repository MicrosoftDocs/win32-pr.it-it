---
description: Questo articolo illustra come inizializzare i gestori delle proprietà per l'uso con il sistema di proprietà di Windows.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Inizializzazione dei gestori di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d7626f92b3d81a6764e635c10302747f82a383
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406994"
---
# <a name="initializing-property-handlers"></a><span data-ttu-id="d44f9-103">Inizializzazione dei gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-103">Initializing Property Handlers</span></span>

<span data-ttu-id="d44f9-104">Questo argomento illustra come creare e registrare gestori di proprietà per l'uso con il sistema di proprietà di Windows.</span><span class="sxs-lookup"><span data-stu-id="d44f9-104">This topic explains how to create and register property handlers to work with the Windows property system.</span></span>

<span data-ttu-id="d44f9-105">Questo argomento è organizzato come segue:</span><span class="sxs-lookup"><span data-stu-id="d44f9-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="d44f9-106">Gestori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-106">Property Handlers</span></span>](#property-handlers)
-   [<span data-ttu-id="d44f9-107">Prima di iniziare</span><span class="sxs-lookup"><span data-stu-id="d44f9-107">Before You Begin</span></span>](#before-you-begin)
-   [<span data-ttu-id="d44f9-108">Inizializzazione dei gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-108">Initializing Property Handlers</span></span>](#initializing-property-handlers)
-   [<span data-ttu-id="d44f9-109">In memoria Archivio proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-109">In-Memory Property Store</span></span>](#in-memory-property-store)
-   [<span data-ttu-id="d44f9-110">Gestione dei PROPVARIANT-Based predefiniti</span><span class="sxs-lookup"><span data-stu-id="d44f9-110">Dealing with PROPVARIANT-Based Values</span></span>](#dealing-with-propvariant-based-values)
-   [<span data-ttu-id="d44f9-111">Supporto dei metadati aperti</span><span class="sxs-lookup"><span data-stu-id="d44f9-111">Supporting Open Metadata</span></span>](#supporting-open-metadata)
-   [<span data-ttu-id="d44f9-112">Contenuto full-text</span><span class="sxs-lookup"><span data-stu-id="d44f9-112">Full-Text Contents</span></span>](#full-text-contents)
-   [<span data-ttu-id="d44f9-113">Fornire valori per le proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-113">Providing Values for Properties</span></span>](#providing-values-for-properties)
-   [<span data-ttu-id="d44f9-114">Scrittura di valori</span><span class="sxs-lookup"><span data-stu-id="d44f9-114">Writing Back Values</span></span>](#writing-back-values)
-   [<span data-ttu-id="d44f9-115">Implementazione di IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="d44f9-115">Implementing IPropertyStoreCapabilities</span></span>](#implementing-ipropertystorecapabilities)
-   [<span data-ttu-id="d44f9-116">Registrazione e distribuzione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-116">Registering and Distributing Property Handlers</span></span>](#registering-and-distributing-property-handlers)
-   [<span data-ttu-id="d44f9-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d44f9-117">Related topics</span></span>](#related-topics)

## <a name="property-handlers"></a><span data-ttu-id="d44f9-118">Gestori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-118">Property Handlers</span></span>

<span data-ttu-id="d44f9-119">I gestori delle proprietà sono una parte fondamentale del sistema di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-119">Property handlers are a crucial part of the property system.</span></span> <span data-ttu-id="d44f9-120">Vengono richiamati in-process dall'indicizzatore per leggere e indicizzare i valori delle proprietà e vengono richiamati anche da Esplora risorse in-process per leggere e scrivere i valori delle proprietà direttamente nei file.</span><span class="sxs-lookup"><span data-stu-id="d44f9-120">They are invoked in-process by the indexer to read and index property values, and are also invoked by Windows Explorer in-process to read and write property values directly in the files.</span></span> <span data-ttu-id="d44f9-121">Questi gestori devono essere scritti e testati con attenzione per evitare prestazioni ridotte o la perdita di dati nei file interessati.</span><span class="sxs-lookup"><span data-stu-id="d44f9-121">These handlers need to be carefully written and tested to prevent degraded performance or the loss of data in the affected files.</span></span> <span data-ttu-id="d44f9-122">Per altre informazioni sulle considerazioni specifiche dell'indicizzatore che influiscono sull'implementazione del gestore delle proprietà, vedere Sviluppo di gestori di proprietà [per Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span><span class="sxs-lookup"><span data-stu-id="d44f9-122">For more information on indexer-specific considerations that affect property handler implementation, see [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span></span>

<span data-ttu-id="d44f9-123">Questo argomento illustra un formato di file basato su XML di esempio che descrive una ricetta con estensione recipe.</span><span class="sxs-lookup"><span data-stu-id="d44f9-123">This topic discusses a sample XML-based file format that describes a recipe with a .recipe file name extension.</span></span> <span data-ttu-id="d44f9-124">L'estensione di file con estensione recipe viene registrata come formato di file distinto anziché basarsi sul formato di file .xml più generico, il cui gestore usa un flusso secondario per archiviare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-124">The .recipe file name extension is registered as its own distinct file format rather than relying on the more generic .xml file format, whose handler uses a secondary stream to store properties.</span></span> <span data-ttu-id="d44f9-125">È consigliabile registrare estensioni di file univoche per i tipi di file.</span><span class="sxs-lookup"><span data-stu-id="d44f9-125">We recommend that you register unique file name extensions for your file types.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="d44f9-126">Prima di iniziare</span><span class="sxs-lookup"><span data-stu-id="d44f9-126">Before You Begin</span></span>

<span data-ttu-id="d44f9-127">I gestori di proprietà sono oggetti COM che creano [**l'astrazione IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per un formato di file specifico.</span><span class="sxs-lookup"><span data-stu-id="d44f9-127">Property handlers are COM objects that create the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) abstraction for a specific file format.</span></span> <span data-ttu-id="d44f9-128">Leggono (analizzano) e scrivono questo formato di file in modo conforme alle specifiche.</span><span class="sxs-lookup"><span data-stu-id="d44f9-128">They read (parse) and write this file format in a manner that conforms to its specification.</span></span> <span data-ttu-id="d44f9-129">Alcuni gestori di proprietà esereranno il proprio lavoro in base alle API che astrarranno l'accesso a un formato di file specifico.</span><span class="sxs-lookup"><span data-stu-id="d44f9-129">Some property handlers do their work based on APIs that abstract access to a specific file format.</span></span> <span data-ttu-id="d44f9-130">Prima di sviluppare un gestore delle proprietà per il formato di file, è necessario comprendere in che modo il formato di file archivia le proprietà e come tali proprietà (nomi e valori) vengono mappate nell'astrazione dell'archivio proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-130">Before you develop a property handler for your file format, you need to understand how your file format stores properties, and how those properties (names and values) are mapped into the property store abstraction.</span></span>

<span data-ttu-id="d44f9-131">Quando si pianifica l'implementazione, tenere presente che i gestori delle proprietà sono componenti di basso livello caricati nel contesto di processi come Esplora risorse, l'indicizzatore Windows Search e applicazioni di terze parti che usano il modello di programmazione dell'elemento Shell.</span><span class="sxs-lookup"><span data-stu-id="d44f9-131">When planning your implementation, remember that property handlers are low-level components that are loaded in the context of processes like Windows Explorer, the Windows Search indexer, and third-party applications that use the Shell item programming model.</span></span> <span data-ttu-id="d44f9-132">Di conseguenza, i gestori di proprietà non possono essere implementati nel codice gestito e devono essere implementati in C++.</span><span class="sxs-lookup"><span data-stu-id="d44f9-132">As a result, property handlers cannot be implemented in managed code, and should be implemented in C++.</span></span> <span data-ttu-id="d44f9-133">Se il gestore usa api o servizi per eseguire il proprio lavoro, è necessario assicurarsi che tali servizi possano funzionare correttamente negli ambienti in cui viene caricato il gestore delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-133">If your handler uses any APIs or services to do its work, you must ensure that those services can function properly in the environment(s) in which your property handler is loaded.</span></span>

> [!Note]  
> <span data-ttu-id="d44f9-134">I gestori di proprietà sono sempre associati a tipi di file specifici. Pertanto, se il formato di file contiene proprietà che richiedono un gestore delle proprietà personalizzate, è necessario registrare sempre un'estensione di file univoca per ogni formato di file.</span><span class="sxs-lookup"><span data-stu-id="d44f9-134">Property handlers are always associated with specific file types; thus, if your file format contains properties that require a custom property handler, you should always register a unique file name extension for each file format.</span></span>

 

## <a name="initializing-property-handlers"></a><span data-ttu-id="d44f9-135">Inizializzazione dei gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-135">Initializing Property Handlers</span></span>

<span data-ttu-id="d44f9-136">Prima che una proprietà venga usata dal sistema, viene inizializzata chiamando un'implementazione di [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span><span class="sxs-lookup"><span data-stu-id="d44f9-136">Before a property is used by the system, it is initialized by calling an implementation of [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span></span> <span data-ttu-id="d44f9-137">Il gestore della proprietà deve essere inizializzato facendo in modo che il sistema gli assegni un flusso anziché lasciare tale assegnazione all'implementazione del gestore.</span><span class="sxs-lookup"><span data-stu-id="d44f9-137">The property handler should be initialized by having the system assign it a stream rather than leaving that assignment to the handler implementation.</span></span> <span data-ttu-id="d44f9-138">Questo metodo di inizializzazione garantisce quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d44f9-138">This method of initialization ensures the following things:</span></span>

-   <span data-ttu-id="d44f9-139">Il gestore delle proprietà può essere eseguito in un processo con restrizioni (una funzionalità di sicurezza importante) senza avere diritti di accesso per leggere o scrivere direttamente i file, anziché accedere al contenuto tramite il flusso.</span><span class="sxs-lookup"><span data-stu-id="d44f9-139">The property handler can run in a restricted process (an important security feature) without having access rights to directly read or write files, rather accessing their content through the stream.</span></span>
-   <span data-ttu-id="d44f9-140">Il sistema può essere considerato attendibile per gestire correttamente gli oplock dei file, che è una misura di affidabilità importante.</span><span class="sxs-lookup"><span data-stu-id="d44f9-140">The system can be trusted to handle the file oplocks correctly, which is an important reliability measure.</span></span>
-   <span data-ttu-id="d44f9-141">Il sistema di proprietà fornisce un servizio di salvataggio sicuro automatico senza alcuna funzionalità aggiuntiva richiesta dall'implementazione del gestore delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-141">The property system provides an automatic safe saving service without any extra functionality required from the property handler implementation.</span></span> <span data-ttu-id="d44f9-142">Per altre [informazioni sui flussi,](#writing-back-values) vedere la sezione Writing Back Values (Scrittura di valori).</span><span class="sxs-lookup"><span data-stu-id="d44f9-142">See the [Writing Back Values](#writing-back-values) section for more information about streams.</span></span>
-   <span data-ttu-id="d44f9-143">L'uso di [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) astrae l'implementazione file system dettagli.</span><span class="sxs-lookup"><span data-stu-id="d44f9-143">Use of the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstracts your implementation from file system details.</span></span> <span data-ttu-id="d44f9-144">In questo modo il gestore può supportare l'inizializzazione tramite archivi alternativi, ad esempio una cartella File Transfer Protocol (FTP) o un file compresso con un'estensione .zip file.</span><span class="sxs-lookup"><span data-stu-id="d44f9-144">This enables the handler to support initialization through alternative storages such as a File Transfer Protocol (FTP) folder or a compressed file with a .zip file name extension.</span></span>

<span data-ttu-id="d44f9-145">In alcuni casi l'inizializzazione con i flussi non è possibile.</span><span class="sxs-lookup"><span data-stu-id="d44f9-145">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="d44f9-146">In queste situazioni, sono disponibili altre due interfacce che i gestori delle proprietà possono implementare: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) e [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span><span class="sxs-lookup"><span data-stu-id="d44f9-146">In those situations, there are two further interfaces that property handlers can implement: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) and [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span></span> <span data-ttu-id="d44f9-147">Se un gestore delle proprietà non implementa [**IInitializeWithStream,**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)deve rifiutare esplicitamente l'esecuzione nel processo isolato in cui l'indicizzatore di sistema lo insererebbe per impostazione predefinita in caso di modifica al flusso.</span><span class="sxs-lookup"><span data-stu-id="d44f9-147">If a property handler does not implement the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process into which the system indexer would place it by default if there were a change to the stream.</span></span> <span data-ttu-id="d44f9-148">Per rifiutare esplicitamente questa funzionalità, impostare il valore del Registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="d44f9-148">To opt out of this feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

<span data-ttu-id="d44f9-149">Tuttavia, è molto meglio implementare [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) ed eseguire un'inizializzazione basata su flusso.</span><span class="sxs-lookup"><span data-stu-id="d44f9-149">However, it is far better to implement [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization.</span></span> <span data-ttu-id="d44f9-150">Di conseguenza, il gestore della proprietà sarà più sicuro e affidabile.</span><span class="sxs-lookup"><span data-stu-id="d44f9-150">Your property handler will be safer and more reliable as a result.</span></span> <span data-ttu-id="d44f9-151">La disabilitazione dell'isolamento dei processi è in genere destinata solo ai gestori di proprietà legacy e deve essere evitata in modo faticoso da qualsiasi nuovo codice.</span><span class="sxs-lookup"><span data-stu-id="d44f9-151">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

<span data-ttu-id="d44f9-152">Per esaminare in dettaglio l'implementazione di un gestore di proprietà, esaminare l'esempio di codice seguente, ovvero un'implementazione di [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span><span class="sxs-lookup"><span data-stu-id="d44f9-152">To examine the implementation of a property handler in detail, look at the following code example, which is an implementation of [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span> <span data-ttu-id="d44f9-153">Il gestore viene inizializzato caricando un documento recipe basato su XML tramite un puntatore all'istanza [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) associata del documento.</span><span class="sxs-lookup"><span data-stu-id="d44f9-153">The handler is initialized by loading an XML-based recipe document through a pointer to that document's associated [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) instance.</span></span> <span data-ttu-id="d44f9-154">La **\_ variabile spDocEle** usata vicino alla fine dell'esempio di codice è definita in precedenza nell'esempio come MSXML2::IXMLDOMElementPtr.</span><span class="sxs-lookup"><span data-stu-id="d44f9-154">The **\_spDocEle** variable used near the end of the code example is defined earlier in the sample as an MSXML2::IXMLDOMElementPtr.</span></span>

> [!Note]  
> <span data-ttu-id="d44f9-155">Gli esempi di codice seguenti e di tutti i successivi sono tratto dall'esempio di gestore di ricette incluso nel Windows Software Development Kit (Windows SDK) (SDK).</span><span class="sxs-lookup"><span data-stu-id="d44f9-155">The following and all subsequent code examples are taken from the recipe handler sample included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d44f9-156">.</span><span class="sxs-lookup"><span data-stu-id="d44f9-156">.</span></span>

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



<span data-ttu-id="d44f9-157">Â</span><span class="sxs-lookup"><span data-stu-id="d44f9-157">Â</span></span> 

<span data-ttu-id="d44f9-158">Dopo il caricamento del documento stesso, le proprietà da visualizzare nel Esplora risorse vengono caricate chiamando il metodo **\_ LoadProperties** protetto, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="d44f9-158">After the document itself is loaded, the properties to be displayed in Windows Explorer are loaded by calling the protected **\_LoadProperties** method, as illustrated in the following code example.</span></span> <span data-ttu-id="d44f9-159">Questo processo viene esaminato in dettaglio nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="d44f9-159">This process is examined in detail in the next section.</span></span>


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



<span data-ttu-id="d44f9-160">Se il flusso è di sola lettura ma il *parametro grfMode* contiene il flag STGM READWRITE, l'inizializzazione avrà esito negativo e restituirà \_ STG \_ E \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="d44f9-160">If the stream is read-only but the *grfMode* parameter contains the STGM\_READWRITE flag, the initialization should fail and return STG\_E\_ACCESSDENIED.</span></span> <span data-ttu-id="d44f9-161">Senza questo controllo, Esplora risorse i valori delle proprietà come scrivibili anche se non lo sono, con un'esperienza utente finale confusa.</span><span class="sxs-lookup"><span data-stu-id="d44f9-161">Without this check, Windows Explorer shows the property values as writable even though they are not, leading to a confusing end-user experience.</span></span>

<span data-ttu-id="d44f9-162">Il gestore della proprietà viene inizializzato una sola volta nella relativa durata.</span><span class="sxs-lookup"><span data-stu-id="d44f9-162">The property handler is initialized only once in its lifetime.</span></span> <span data-ttu-id="d44f9-163">Se viene richiesta una seconda inizializzazione, il gestore deve restituire `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .</span><span class="sxs-lookup"><span data-stu-id="d44f9-163">If a second initialization is requested, the handler should return `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)`.</span></span>

## <a name="in-memory-property-store"></a><span data-ttu-id="d44f9-164">In-Memory Archivio proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-164">In-Memory Property Store</span></span>

<span data-ttu-id="d44f9-165">Prima di vedere l'implementazione di **\_ LoadProperties,** è necessario comprendere la matrice **PropertyMap** usata nell'esempio per eseguire il mapping delle proprietà nel documento XML alle proprietà esistenti nel sistema di proprietà tramite i relativi valori PKEY.</span><span class="sxs-lookup"><span data-stu-id="d44f9-165">Before looking at the implementation of **\_LoadProperties**, you should understand the **PropertyMap** array used in the sample to map properties in the XML document to existing properties in the property system through their PKEY values.</span></span>

<span data-ttu-id="d44f9-166">Non esporre ogni elemento e attributo nel file XML come proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-166">You should not expose every element and attribute in the XML file as a property.</span></span> <span data-ttu-id="d44f9-167">Selezionare invece solo quelli che si ritiene siano utili per gli utenti finali nell'organizzazione dei documenti (in questo caso, le ricette).</span><span class="sxs-lookup"><span data-stu-id="d44f9-167">Instead, select only those that you believe will be useful to end users in the organization of their documents (in this case, recipes).</span></span> <span data-ttu-id="d44f9-168">Si tratta di un concetto importante da tenere presente quando si sviluppano i gestori delle proprietà: la differenza tra le informazioni realmente utili per gli scenari aziendali e le informazioni che appartengono ai dettagli del file e possono essere visualizzate aprendo il file stesso.</span><span class="sxs-lookup"><span data-stu-id="d44f9-168">This is an important concept to keep in mind as you develop your property handlers: the difference between information that is truly useful for organizational scenarios, and information that belongs to the details of your file and can be seen by opening the file itself.</span></span> <span data-ttu-id="d44f9-169">Le proprietà non devono essere una duplicazione completa di un file XML.</span><span class="sxs-lookup"><span data-stu-id="d44f9-169">Properties are not intended to be a full duplication of an XML file.</span></span>


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



<span data-ttu-id="d44f9-170">Ecco l'implementazione completa **\_ del metodo LoadProperties** chiamato da [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span><span class="sxs-lookup"><span data-stu-id="d44f9-170">Here is the full implementation of the **\_LoadProperties** method called by [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



<span data-ttu-id="d44f9-171">Il **\_ metodo LoadProperties** chiama la funzione helper Shell [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) per creare un archivio delle proprietà in memoria (cache) per le proprietà gestite.</span><span class="sxs-lookup"><span data-stu-id="d44f9-171">The **\_LoadProperties** method calls the Shell helper function [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create an in-memory property store (cache) for the handled properties.</span></span> <span data-ttu-id="d44f9-172">Usando una cache, le modifiche vengono rilevate per l'utente.</span><span class="sxs-lookup"><span data-stu-id="d44f9-172">By using a cache, changes are tracked for you.</span></span> <span data-ttu-id="d44f9-173">In questo modo è possibile verificare se un valore di proprietà è stato modificato nella cache ma non è stato ancora salvato nell'archiviazione persistente.</span><span class="sxs-lookup"><span data-stu-id="d44f9-173">This frees you from tracking whether a property value has been changed in the cache but not yet saved to persisted storage.</span></span> <span data-ttu-id="d44f9-174">Consente inoltre di rendere inutili persistenti i valori delle proprietà che non sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="d44f9-174">It also frees you from needlessly persisting property values that have not changed.</span></span>

<span data-ttu-id="d44f9-175">Il **\_ metodo LoadProperties** chiama anche **\_ LoadProperty** la cui implementazione è illustrata nel codice seguente) una volta per ogni proprietà mappata.</span><span class="sxs-lookup"><span data-stu-id="d44f9-175">The **\_LoadProperties** method also calls **\_LoadProperty** whose implementation is illustrated in the following code) once for each mapped property.</span></span> <span data-ttu-id="d44f9-176">**\_ LoadProperty** ottiene il valore della proprietà come specificato nell'elemento **PropertyMap** nel flusso XML e lo assegna alla cache in memoria tramite una chiamata a [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span><span class="sxs-lookup"><span data-stu-id="d44f9-176">**\_LoadProperty** gets the value of the property as specified in the **PropertyMap** element in the XML stream and assigns it to the in-memory cache through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span></span> <span data-ttu-id="d44f9-177">Il flag PSC NORMAL nella chiamata \_ a **IPropertyStoreCache::SetValueAndState** indica che il valore della proprietà non è stato modificato dopo l'immissione nella cache.</span><span class="sxs-lookup"><span data-stu-id="d44f9-177">The PSC\_NORMAL flag in the call to **IPropertyStoreCache::SetValueAndState** indicates that the property value has not been altered since the time it entered the cache.</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a><span data-ttu-id="d44f9-178">Gestione dei PROPVARIANT-Based predefiniti</span><span class="sxs-lookup"><span data-stu-id="d44f9-178">Dealing with PROPVARIANT-Based Values</span></span>

<span data-ttu-id="d44f9-179">Nell'implementazione **\_ di LoadProperty** viene fornito un valore della proprietà sotto forma di [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="d44f9-179">In the implementation of **\_LoadProperty**, a property value is provided in the form of a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="d44f9-180">Viene fornito un set di API nel Software Development Kit (SDK) per la conversione da tipi primitivi come **PWSTR** o **int** a o da tipi **PROPVARIANT.**</span><span class="sxs-lookup"><span data-stu-id="d44f9-180">A set of APIs in the software development kit (SDK) is provided to convert from primitive types such as **PWSTR** or **int** to or from **PROPVARIANT** types.</span></span> <span data-ttu-id="d44f9-181">Queste API sono disponibili in Propvarutil.h.</span><span class="sxs-lookup"><span data-stu-id="d44f9-181">These APIs are found in Propvarutil.h.</span></span>

<span data-ttu-id="d44f9-182">Ad esempio, per convertire [**un oggetto PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in una stringa, è possibile usare [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d44f9-182">For example, to convert a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to a string, you can use [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) as illustrated here.</span></span>


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



<span data-ttu-id="d44f9-183">Per inizializzare un oggetto PROPVARIANT da una stringa, è possibile usare [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span><span class="sxs-lookup"><span data-stu-id="d44f9-183">To initialize a PROPVARIANT from a string, you can use [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span></span>


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



<span data-ttu-id="d44f9-184">Come si può vedere in uno dei file di ricette inclusi nell'esempio, può essere presente più di una parola chiave in ogni file.</span><span class="sxs-lookup"><span data-stu-id="d44f9-184">As you can see in any of the recipe files included in the sample, there can be more than one keyword in each file.</span></span> <span data-ttu-id="d44f9-185">A tale scopo, il sistema di proprietà supporta stringhe multivalore rappresentate come vettore di stringhe ,ad esempio "VT \_ VECTOR \| VT \_ LPWSTR".</span><span class="sxs-lookup"><span data-stu-id="d44f9-185">To account for this, the property system supports multi-valued strings represented as a vector of strings (for instance "VT\_VECTOR \| VT\_LPWSTR").</span></span> <span data-ttu-id="d44f9-186">Il **\_ metodo LoadVectorProperty** nell'esempio usa valori basati su vettori.</span><span class="sxs-lookup"><span data-stu-id="d44f9-186">The **\_LoadVectorProperty** method in the example uses vector-based values.</span></span>


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



<span data-ttu-id="d44f9-187">Se non esiste un valore nel file, non restituire un errore.</span><span class="sxs-lookup"><span data-stu-id="d44f9-187">If a value does not exist in the file, do not return an error.</span></span> <span data-ttu-id="d44f9-188">Impostare invece il valore su VT \_ EMPTY e restituire S **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d44f9-188">Instead, set the value to VT\_EMPTY and return **S\_OK**.</span></span> <span data-ttu-id="d44f9-189">VT \_ EMPTY indica che il valore della proprietà non esiste.</span><span class="sxs-lookup"><span data-stu-id="d44f9-189">VT\_EMPTY indicates that the property value does not exist.</span></span>

## <a name="supporting-open-metadata"></a><span data-ttu-id="d44f9-190">Supporto dei metadati aperti</span><span class="sxs-lookup"><span data-stu-id="d44f9-190">Supporting Open Metadata</span></span>

<span data-ttu-id="d44f9-191">In questo esempio viene utilizzato un formato di file basato su XML.</span><span class="sxs-lookup"><span data-stu-id="d44f9-191">This example uses an XML-based file format.</span></span> <span data-ttu-id="d44f9-192">Il relativo schema può essere esteso per supportare le proprietà che non sono state pensate durante lo sviluppo, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="d44f9-192">Its schema can be extended to support properties that were not thought of during developmet, for example.</span></span> <span data-ttu-id="d44f9-193">Questo sistema è noto come metadati aperti.</span><span class="sxs-lookup"><span data-stu-id="d44f9-193">This system is known as open metadata.</span></span> <span data-ttu-id="d44f9-194">Questo esempio estende il sistema di proprietà creando un nodo nell'elemento **Recipe** denominato **ExtendedProperties**, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="d44f9-194">This example extends the property system by creating a node under the **Recipe** element called **ExtendedProperties**, as illustrated in the following code example.</span></span>


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



<span data-ttu-id="d44f9-195">Per caricare le proprietà estese persistenti durante l'inizializzazione, implementare il **\_ metodo LoadExtendedProperties,** come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="d44f9-195">To load persisted extended properties during initialization, implement the **\_LoadExtendedProperties** method, as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



<span data-ttu-id="d44f9-196">Le API di serializzazione dichiarate in Propsys.h vengono usate per serializzare e deserializzare i tipi [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in BLOB di dati e quindi viene usata la codifica Base64 per serializzare tali BLOB in stringhe che possono essere salvate nel codice XML.</span><span class="sxs-lookup"><span data-stu-id="d44f9-196">Serialization APIs declared in Propsys.h are used to serialize and deserialize [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types into blobs of data, and then Base64 encoding is used to serialize those blobs into strings that can be saved in the XML.</span></span> <span data-ttu-id="d44f9-197">Queste stringhe vengono archiviate **nell'attributo EncodedValue** dell'elemento **ExtendedProperties.**</span><span class="sxs-lookup"><span data-stu-id="d44f9-197">These strings are stored in the **EncodedValue** attribute of the **ExtendedProperties** element.</span></span> <span data-ttu-id="d44f9-198">Il metodo di utilità seguente, implementato nel file Util.cpp dell'esempio, esegue la serializzazione.</span><span class="sxs-lookup"><span data-stu-id="d44f9-198">The following utility method, implemented in the sample's Util.cpp file, performs the serialization.</span></span> <span data-ttu-id="d44f9-199">Inizia con una chiamata alla [**funzione StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) per eseguire la serializzazione binaria, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="d44f9-199">It begins with a call to the [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) function to perform the binary serialization, as illustrated in the following code example.</span></span>


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



<span data-ttu-id="d44f9-200">Successivamente, la [**funzione CryptBinaryToString,**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)dichiarata in Wincrypt.h, esegue la conversione Base64.</span><span class="sxs-lookup"><span data-stu-id="d44f9-200">Next, the [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â function, declared in Wincrypt.h, performs the Base64 conversion.</span></span>


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



<span data-ttu-id="d44f9-201">La **funzione DeserializePropVariantFromString,** disponibile anche in Util.cpp, inverte l'operazione, deserializzando i valori dal file XML.</span><span class="sxs-lookup"><span data-stu-id="d44f9-201">The **DeserializePropVariantFromString** function, also found in Util.cpp, reverses the operation, deserializing values from the XML file.</span></span>

<span data-ttu-id="d44f9-202">Per informazioni sul supporto per i metadati aperti, vedere "Tipi di file che supportano metadati aperti" in [Tipi di file.](../shell/fa-file-types.md)</span><span class="sxs-lookup"><span data-stu-id="d44f9-202">For information about support for open metadata, see "File Types that Support Open Metadata" in [File Types](../shell/fa-file-types.md).</span></span>

## <a name="full-text-contents"></a><span data-ttu-id="d44f9-203">Full-Text contenuto</span><span class="sxs-lookup"><span data-stu-id="d44f9-203">Full-Text Contents</span></span>

<span data-ttu-id="d44f9-204">I gestori di proprietà possono anche semplificare una ricerca full-text del contenuto del file e sono un modo semplice per fornire tale funzionalità se il formato di file non è troppo complicato.</span><span class="sxs-lookup"><span data-stu-id="d44f9-204">Property handlers can also facilitate a full-text search of the file contents, and they are an easy way to provide that functionality if the file format is not overly complicated.</span></span> <span data-ttu-id="d44f9-205">Esiste un modo alternativo e più potente per fornire il testo completo del file tramite [**l'implementazione dell'interfaccia IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="d44f9-205">There is an alternative, more powerful way to provide the full text of the file through the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface implementation.</span></span>

<span data-ttu-id="d44f9-206">La tabella seguente riepiloga i vantaggi di ogni approccio usando [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) o [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)</span><span class="sxs-lookup"><span data-stu-id="d44f9-206">The following table summarizes the benefits of each approach using either [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>



| <span data-ttu-id="d44f9-207">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="d44f9-207">Capability</span></span>                                   | <span data-ttu-id="d44f9-208">Ifilter</span><span class="sxs-lookup"><span data-stu-id="d44f9-208">IFilter</span></span>                      | <span data-ttu-id="d44f9-209">Ipropertystore</span><span class="sxs-lookup"><span data-stu-id="d44f9-209">IPropertyStore</span></span> |
|----------------------------------------------|------------------------------|----------------|
| <span data-ttu-id="d44f9-210">Consente il write back nei file?</span><span class="sxs-lookup"><span data-stu-id="d44f9-210">Allows write back to files?</span></span>                  | <span data-ttu-id="d44f9-211">No</span><span class="sxs-lookup"><span data-stu-id="d44f9-211">No</span></span>                           | <span data-ttu-id="d44f9-212">Sì</span><span class="sxs-lookup"><span data-stu-id="d44f9-212">Yes</span></span>            |
| <span data-ttu-id="d44f9-213">Fornisce una combinazione di contenuto e proprietà?</span><span class="sxs-lookup"><span data-stu-id="d44f9-213">Provides mix of content and properties?</span></span>      | <span data-ttu-id="d44f9-214">Sì</span><span class="sxs-lookup"><span data-stu-id="d44f9-214">Yes</span></span>                          | <span data-ttu-id="d44f9-215">Sì</span><span class="sxs-lookup"><span data-stu-id="d44f9-215">Yes</span></span>            |
| <span data-ttu-id="d44f9-216">Multilingue?</span><span class="sxs-lookup"><span data-stu-id="d44f9-216">Multilingual?</span></span>                                | <span data-ttu-id="d44f9-217">Sì</span><span class="sxs-lookup"><span data-stu-id="d44f9-217">Yes</span></span>                          | <span data-ttu-id="d44f9-218">No</span><span class="sxs-lookup"><span data-stu-id="d44f9-218">No</span></span>             |
| <span data-ttu-id="d44f9-219">MIME/Embedded?</span><span class="sxs-lookup"><span data-stu-id="d44f9-219">MIME/Embedded?</span></span>                               | <span data-ttu-id="d44f9-220">Sì</span><span class="sxs-lookup"><span data-stu-id="d44f9-220">Yes</span></span>                          | <span data-ttu-id="d44f9-221">No</span><span class="sxs-lookup"><span data-stu-id="d44f9-221">No</span></span>             |
| <span data-ttu-id="d44f9-222">Limiti di testo?</span><span class="sxs-lookup"><span data-stu-id="d44f9-222">Text boundaries?</span></span>                             | <span data-ttu-id="d44f9-223">Frase, paragrafo, capitolo</span><span class="sxs-lookup"><span data-stu-id="d44f9-223">Sentence, paragraph, chapter</span></span> | <span data-ttu-id="d44f9-224">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d44f9-224">None</span></span>           |
| <span data-ttu-id="d44f9-225">Implementazione supportata per SPS/SQL Server?</span><span class="sxs-lookup"><span data-stu-id="d44f9-225">Implementation supported for SPS/SQL Server?</span></span> | <span data-ttu-id="d44f9-226">Sì</span><span class="sxs-lookup"><span data-stu-id="d44f9-226">Yes</span></span>                          | <span data-ttu-id="d44f9-227">No</span><span class="sxs-lookup"><span data-stu-id="d44f9-227">No</span></span>             |
| <span data-ttu-id="d44f9-228">Implementazione</span><span class="sxs-lookup"><span data-stu-id="d44f9-228">Implementation</span></span>                               | <span data-ttu-id="d44f9-229">Complex</span><span class="sxs-lookup"><span data-stu-id="d44f9-229">Complex</span></span>                      | <span data-ttu-id="d44f9-230">Semplice</span><span class="sxs-lookup"><span data-stu-id="d44f9-230">Simple</span></span>         |



 

<span data-ttu-id="d44f9-231">Nell'esempio del gestore di recipe il formato del file recipe non presenta requisiti complessi, quindi è stato implementato solo [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per il supporto full-text.</span><span class="sxs-lookup"><span data-stu-id="d44f9-231">In the recipe handler sample, the recipe file format does not have any complex requirements, so only [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) has been implemented for full-text support.</span></span> <span data-ttu-id="d44f9-232">La ricerca full-text viene implementata per i nodi XML denominati nella matrice seguente.</span><span class="sxs-lookup"><span data-stu-id="d44f9-232">Full-text search is implemented for the XML nodes named in the following array.</span></span>


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



<span data-ttu-id="d44f9-233">Il sistema di proprietà contiene la proprietà (PKEY Search Contents), creata per fornire `System.Search.Contents` \_ contenuto \_ full-text all'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="d44f9-233">The property system contains the `System.Search.Contents` (PKEY\_Search\_Contents) property, which was created to provide full-text content to the indexer.</span></span> <span data-ttu-id="d44f9-234">Il valore di questa proprietà non viene mai visualizzato direttamente nell'interfaccia utente. Il testo di tutti i nodi XML denominati nella matrice precedente viene concatenato in un'unica stringa.</span><span class="sxs-lookup"><span data-stu-id="d44f9-234">This property's value is never displayed directly in the UI; the text from all of the XML nodes named in the array above are concatenated into a single string.</span></span> <span data-ttu-id="d44f9-235">Tale stringa viene quindi fornita all'indicizzatore come contenuto full-text del file recipe tramite una chiamata a [**IPropertyStoreCache::SetValueAndState,**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="d44f9-235">That string is then provided to the indexer as the full-text content of the recipe file through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a><span data-ttu-id="d44f9-236">Specifica di valori per le proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-236">Providing Values for Properties</span></span>

<span data-ttu-id="d44f9-237">Quando vengono usati per leggere i valori, i gestori delle proprietà vengono in genere richiamati per uno dei motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d44f9-237">When used to read values, property handlers are usually invoked for one of the following reasons:</span></span>

-   <span data-ttu-id="d44f9-238">Per enumerare tutti i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-238">To enumerate all property values.</span></span>
-   <span data-ttu-id="d44f9-239">Per ottenere il valore di una proprietà specifica.</span><span class="sxs-lookup"><span data-stu-id="d44f9-239">To get the value of a specific property.</span></span>

<span data-ttu-id="d44f9-240">Per l'enumerazione, a un gestore delle proprietà viene richiesto di enumerarne le proprietà durante l'indicizzazione o quando la finestra di dialogo delle proprietà richiede la visualizzazione delle proprietà nel **gruppo Altro** .</span><span class="sxs-lookup"><span data-stu-id="d44f9-240">For enumeration, a property handler is asked to enumerate its properties either during indexing or when the properties dialog box asks for properties to display in the **Other** group.</span></span> <span data-ttu-id="d44f9-241">L'indicizzazione continua come operazione in background.</span><span class="sxs-lookup"><span data-stu-id="d44f9-241">Indexing goes on constantly as a background operation.</span></span> <span data-ttu-id="d44f9-242">Ogni volta che un file viene modificato, l'indicizzatore viene informato e indicizza nuovamente il file richiedendo al gestore delle proprietà di enumerarne le proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-242">Whenever a file changes, the indexer is notified, and it re-indexes the file by asking the property handler to enumerate its properties.</span></span> <span data-ttu-id="d44f9-243">È quindi fondamentale che i gestori delle proprietà siano implementati in modo efficiente e restituiranno i valori delle proprietà il più rapidamente possibile.</span><span class="sxs-lookup"><span data-stu-id="d44f9-243">Therefore, it is critical that property handlers are implemented efficiently and return property values as quickly as possible.</span></span> <span data-ttu-id="d44f9-244">Enumerare tutte le proprietà per le quali si dispone di valori, come si farebbe per qualsiasi raccolta, ma non enumerare le proprietà che comportano calcoli a elevato utilizzo di memoria o richieste di rete che potrebbero renderle lente per il recupero.</span><span class="sxs-lookup"><span data-stu-id="d44f9-244">Enumerate all the properties for which you have values, just as you would for any collection, but do not enumerate properties that involve memory-intensive calculations or network requests that could make them slow to retrieve.</span></span>

<span data-ttu-id="d44f9-245">Quando si scrive un gestore di proprietà, in genere è necessario considerare i due set di proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="d44f9-245">When writing a property handler, you usually need to consider the following two sets of properties.</span></span>

-   <span data-ttu-id="d44f9-246">Proprietà primarie: proprietà supportate dal tipo di file in modo nativo.</span><span class="sxs-lookup"><span data-stu-id="d44f9-246">Primary properties: Properties that your file type supports natively.</span></span> <span data-ttu-id="d44f9-247">Ad esempio, un gestore della proprietà photo per i metadati EXIF (Exchangeable Image File) supporta in modo nativo `System.Photo.FNumber` .</span><span class="sxs-lookup"><span data-stu-id="d44f9-247">For example, a photo property handler for Exchangeable Image File (EXIF) metadata natively supports `System.Photo.FNumber`.</span></span>
-   <span data-ttu-id="d44f9-248">Proprietà estese: proprietà supportate dal tipo di file come parte dei metadati aperti.</span><span class="sxs-lookup"><span data-stu-id="d44f9-248">Extended properties: Properties that your file type supports as part of open metadata.</span></span>

<span data-ttu-id="d44f9-249">Poiché l'esempio usa la cache in memoria, l'implementazione dei metodi [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) è solo una questione di delega a tale cache, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="d44f9-249">Because the sample uses in-memory cache, implementing [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods is just a matter of delegating to that cache, as illustrated in the following code example.</span></span>


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



<span data-ttu-id="d44f9-250">Se si sceglie di non delegare alla cache in memoria, è necessario implementare i metodi> il comportamento previsto seguente:</span><span class="sxs-lookup"><span data-stu-id="d44f9-250">If you choose not to delegate to the in-memory cache, you must implement your methods to provide> the following expected behavior:</span></span>

-   <span data-ttu-id="d44f9-251">[**IPropertyStore::GetCount:**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85))se non sono presenti proprietà, questo metodo restituisce **S \_ OK.**</span><span class="sxs-lookup"><span data-stu-id="d44f9-251">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): If there are no properties, this method returns **S\_OK**.</span></span>
-   <span data-ttu-id="d44f9-252">[**IPropertyStore::GetAt:**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85))se *iProp* è maggiore o uguale a *cProps,* questo metodo restituisce E INVALIDARG e la struttura a cui punta il parametro pkey viene riempita con \_ zeri. </span><span class="sxs-lookup"><span data-stu-id="d44f9-252">[**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): If *iProp* is greater than or equal to *cProps*, this method returns E\_INVALIDARG and the structure pointed to by the *pkey* parameter is filled with zeroes.</span></span>
-   <span data-ttu-id="d44f9-253">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) riflettono lo stato corrente del gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-253">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) and [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflect the current state of the property handler.</span></span> <span data-ttu-id="d44f9-254">Se [**propertyKEY viene**](/windows/win32/api/wtypes/ns-wtypes-propertykey) aggiunto o rimosso dal file tramite [**IPropertyStore::SetValue,**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))questi due metodi devono riflettere tale modifica alla successiva chiamata.</span><span class="sxs-lookup"><span data-stu-id="d44f9-254">If a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) is added to or removed from the file through [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), these two methods must reflect that change the next time they are called.</span></span>
-   <span data-ttu-id="d44f9-255">[**IPropertyStore::GetValue:**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85))se a questo metodo viene richiesto un valore che non esiste, restituisce **S \_ OK** con il valore segnalato come VT \_ EMPTY.</span><span class="sxs-lookup"><span data-stu-id="d44f9-255">[**IPropertyStore::GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): If this method is asked for a value that does not exist, it returns **S\_OK** with the value reported as VT\_EMPTY.</span></span>

## <a name="writing-back-values"></a><span data-ttu-id="d44f9-256">Scrittura di valori</span><span class="sxs-lookup"><span data-stu-id="d44f9-256">Writing Back Values</span></span>

<span data-ttu-id="d44f9-257">Quando il gestore delle proprietà scrive il valore di una proprietà usando [**IPropertyStore::SetValue,**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))non scrive il valore nel file fino a quando non viene chiamato [**IPropertyStore::Commit.**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d44f9-257">When the property handler writes the value of a property using [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), it does not write the value to the file until [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) is called.</span></span> <span data-ttu-id="d44f9-258">La cache in memoria può essere utile per implementare questo schema.</span><span class="sxs-lookup"><span data-stu-id="d44f9-258">The in-memory cache can be useful in implementing this scheme.</span></span> <span data-ttu-id="d44f9-259">Nel codice di esempio l'implementazione **di IPropertyStore::SetValue** imposta semplicemente il nuovo valore nella cache in memoria e imposta lo stato di tale proprietà su PSC \_ DIRTY.</span><span class="sxs-lookup"><span data-stu-id="d44f9-259">In the sample code the **IPropertyStore::SetValue** implementation simply sets the new value in the in-memory cache and sets the state of that property to PSC\_DIRTY.</span></span>


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



<span data-ttu-id="d44f9-260">In qualsiasi [**implementazione di IPropertyStore,**](/windows/win32/api/propsys/nn-propsys-ipropertystore) da [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))è previsto il comportamento seguente:</span><span class="sxs-lookup"><span data-stu-id="d44f9-260">In any [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, the following behavior is expected from [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):</span></span>

-   <span data-ttu-id="d44f9-261">Se la proprietà esiste già, viene impostato il valore della proprietà .</span><span class="sxs-lookup"><span data-stu-id="d44f9-261">If the property already exists, the value of the property is set.</span></span>
-   <span data-ttu-id="d44f9-262">Se la proprietà non esiste, viene aggiunta la nuova proprietà e ne viene impostato il valore.</span><span class="sxs-lookup"><span data-stu-id="d44f9-262">If the property does not exist, the new property is added and its value set.</span></span>
-   <span data-ttu-id="d44f9-263">Se il valore della proprietà non può essere reso persistente con la stessa accuratezza specificata (ad esempio, il troncamento a causa di limitazioni delle dimensioni nel formato di file), il valore viene impostato per quanto possibile e viene restituito INPLACE \_ S \_ TRUNCATED.</span><span class="sxs-lookup"><span data-stu-id="d44f9-263">If the property value cannot be persisted at the same accuracy as given (for instance, truncation due to size limitations in the file format), the value is set as far as possible and INPLACE\_S\_TRUNCATED is returned.</span></span>
-   <span data-ttu-id="d44f9-264">Se la proprietà non è supportata dal gestore della proprietà, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` viene restituito .</span><span class="sxs-lookup"><span data-stu-id="d44f9-264">If the property is not supported by the property handler, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` is returned.</span></span>
-   <span data-ttu-id="d44f9-265">Se esiste un altro motivo per cui non è possibile impostare il valore della proprietà, ad esempio il file bloccato o la mancanza di diritti di modifica tramite elenchi di controllo di accesso (ACL), viene restituito STG \_ E \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="d44f9-265">If there is another reason that the property value cannot be set, such as the file being locked or lack of rights to edit through access control lists (ACLs), then STG\_E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="d44f9-266">Uno dei principali vantaggi dell'uso dei flussi, come nell'esempio, è l'affidabilità.</span><span class="sxs-lookup"><span data-stu-id="d44f9-266">One major advantage of using streams, as the sample, is reliability.</span></span> <span data-ttu-id="d44f9-267">I gestori di proprietà devono sempre considerare che non possono lasciare un file in uno stato incoerente in caso di errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="d44f9-267">Property handlers must always consider that they cannot leave a file in an inconsistent state in the case of a catastrophic failure.</span></span> <span data-ttu-id="d44f9-268">È ovviamente consigliabile evitare di danneggiare i file di un utente e il modo migliore per eseguire questa operazione è con un meccanismo di copia su scrittura.</span><span class="sxs-lookup"><span data-stu-id="d44f9-268">Corrupting a user's files obviously should be avoided, and the best way to do this is with a "copy-on-write" mechanism.</span></span> <span data-ttu-id="d44f9-269">Se il gestore delle proprietà usa un flusso per accedere a un file, si ottiene automaticamente questo comportamento. il sistema scrive tutte le modifiche nel flusso, sostituendo il file con la nuova copia solo durante l'operazione di commit.</span><span class="sxs-lookup"><span data-stu-id="d44f9-269">If your property handler uses a stream to access a file, you get this behavior automatically; the system writes any changes to the stream, replacing the file with the new copy only during the commit operation.</span></span>

<span data-ttu-id="d44f9-270">Per eseguire l'override di questo comportamento e controllare manualmente il processo di salvataggio dei file, è possibile rifiutare esplicitamente il comportamento di salvataggio sicuro impostando il valore ManualSafeSave nella voce del Registro di sistema del gestore, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d44f9-270">To override this behavior and control the file saving process manually, you can opt out of the safe save behavior by setting the ManualSafeSave value in your handler's registry entry as illustrated here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

<span data-ttu-id="d44f9-271">Quando un gestore specifica il valore ManualSafeSave, il flusso con cui viene inizializzato non è un flusso transazionato (STGM \_ TRANSACTED).</span><span class="sxs-lookup"><span data-stu-id="d44f9-271">When a handler specifies the ManualSafeSave value, the stream with which it is initialized is not a transacted stream (STGM\_TRANSACTED).</span></span> <span data-ttu-id="d44f9-272">Il gestore stesso deve implementare la funzione di salvataggio sicuro per garantire che il file non sia danneggiato se l'operazione di salvataggio viene interrotta.</span><span class="sxs-lookup"><span data-stu-id="d44f9-272">The handler itself must implement the safe save function to ensure that the file is not corrupted if the save operation is interrupted.</span></span> <span data-ttu-id="d44f9-273">Se il gestore implementa la scrittura sul posto, scriverà nel flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="d44f9-273">If the handler implements in-place writing, it will write to the stream that it is given.</span></span> <span data-ttu-id="d44f9-274">Se il gestore non supporta questa funzionalità, deve recuperare un flusso con cui scrivere la copia aggiornata del file usando [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span><span class="sxs-lookup"><span data-stu-id="d44f9-274">If the handler does not support this feature, then it must retrieve a stream with which to write the updated copy of the file using [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span></span> <span data-ttu-id="d44f9-275">Al termine della scrittura, il gestore deve chiamare [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) nel flusso originale per completare l'operazione e sostituire il contenuto del flusso originale con la nuova copia del file.</span><span class="sxs-lookup"><span data-stu-id="d44f9-275">After the handler is done writing, it should call [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) on the original stream to complete the operation, and replace the contents of the original stream with the new copy of the file.</span></span>

<span data-ttu-id="d44f9-276">ManualSafeSave è anche la situazione predefinita se non si inizializza il gestore con un flusso.</span><span class="sxs-lookup"><span data-stu-id="d44f9-276">ManualSafeSave is also the default situation if you do not initialize your handler with a stream.</span></span> <span data-ttu-id="d44f9-277">Senza un flusso originale per ricevere il contenuto del flusso temporaneo, è necessario usare [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) per eseguire una sostituzione atomica del file di origine.</span><span class="sxs-lookup"><span data-stu-id="d44f9-277">Without an original stream to receive the contents of the temporary stream, you must use [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) to perform an atomic replacement of the source file.</span></span>

<span data-ttu-id="d44f9-278">I formati di file di grandi dimensioni che verranno usati in modo da produrre file superiori a 1 MB devono implementare il supporto per la scrittura di proprietà sul posto; In caso contrario, il comportamento delle prestazioni non soddisfa le aspettative dei client del sistema di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-278">Large file formats that will be used in a way that produces files greater than 1 MB should implement support for in-place property writing; otherwise, the performance behavior does not meet the expectations of clients of the property system.</span></span> <span data-ttu-id="d44f9-279">In questo scenario, il tempo necessario per scrivere le proprietà non deve essere influenzato dalle dimensioni del file.</span><span class="sxs-lookup"><span data-stu-id="d44f9-279">In this scenario, the time required to write properties should not be affected by the file size.</span></span>

<span data-ttu-id="d44f9-280">Per i file di dimensioni molto grandi, ad esempio un file video di almeno 1 GB, è necessaria una soluzione diversa.</span><span class="sxs-lookup"><span data-stu-id="d44f9-280">For very large files, for example a video file of 1 GB or more, a different solution is required.</span></span> <span data-ttu-id="d44f9-281">Se lo spazio nel file non è sufficiente per eseguire la scrittura sul posto, il gestore potrebbe non riuscire a eseguire l'aggiornamento della proprietà se la quantità di spazio riservata per la scrittura delle proprietà sul posto è stata esaurita.</span><span class="sxs-lookup"><span data-stu-id="d44f9-281">If there is not enough space in the file to perform in-place writing, the handler may fail the property update if the amount of space reserved for in-place property writing has been exhausted.</span></span> <span data-ttu-id="d44f9-282">Questo errore si verifica per evitare prestazioni scarse derivanti da 2 GB di I/O (da 1 a lettura, 1 da scrivere).</span><span class="sxs-lookup"><span data-stu-id="d44f9-282">This failure occurs to avoid poor performance arising from 2 GB of IO (1 to read, 1 to write).</span></span> <span data-ttu-id="d44f9-283">A causa di questo potenziale errore, questi formati di file devono riservare spazio sufficiente per la scrittura delle proprietà sul posto.</span><span class="sxs-lookup"><span data-stu-id="d44f9-283">Because of this potential failure, these file formats should reserve enough space for in-place property writing.</span></span>

<span data-ttu-id="d44f9-284">Se il file ha spazio sufficiente nell'intestazione per scrivere i metadati e se la scrittura di questi metadati non causa l'aumentare o la riduzione del file, potrebbe essere sicuro scrivere sul posto.</span><span class="sxs-lookup"><span data-stu-id="d44f9-284">If the file has enough space in its header to write metadata, and if the writing of that metadata does not cause the file to grow or shrink, it might be safe to write in-place.</span></span> <span data-ttu-id="d44f9-285">Come punto di partenza è consigliabile usare 64 KB.</span><span class="sxs-lookup"><span data-stu-id="d44f9-285">We recommend 64 KB as a starting point.</span></span> <span data-ttu-id="d44f9-286">La scrittura sul posto equivale al gestore che richiede ManualSafeSave e chiama [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) nell'implementazione di [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))e ha prestazioni molto migliori rispetto alla copia in scrittura.</span><span class="sxs-lookup"><span data-stu-id="d44f9-286">Writing in-place is equivalent to the handler asking for ManualSafeSave and calling [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) in the implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), and has much better performance than copy-on-write.</span></span> <span data-ttu-id="d44f9-287">Se le dimensioni del file cambiano a causa di modifiche al valore della proprietà, non è consigliabile eseguire la scrittura sul posto a causa del potenziale danneggiamento di un file in caso di terminazione anomala.</span><span class="sxs-lookup"><span data-stu-id="d44f9-287">If the file size changes due to property value changes, writing in-place should not be attempted because of the potential for a corrupted file in the event of an abnormal termination.</span></span>

> [!Note]  
> <span data-ttu-id="d44f9-288">Per motivi di prestazioni, è consigliabile usare l'opzione ManualSafeSave con gestori di proprietà che funzionano con file di dimensioni maggiori o superiori a 100 KB.</span><span class="sxs-lookup"><span data-stu-id="d44f9-288">For performance reasons we recommend that the ManualSafeSave option be used with property handlers working with files that are 100 KB or larger.</span></span>

 

<span data-ttu-id="d44f9-289">Come illustrato nell'implementazione di esempio seguente di [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), il gestore per ManualSafeSave viene registrato per illustrare l'opzione di salvataggio sicuro manuale.</span><span class="sxs-lookup"><span data-stu-id="d44f9-289">As illustrated in the following sample implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), the handler for ManualSafeSave is registered to illustrate the manual safe save option.</span></span> <span data-ttu-id="d44f9-290">Il **\_ metodo SaveCacheToDom** scrive i valori delle proprietà archiviati nella cache in memoria nell'oggetto XMLdocument.</span><span class="sxs-lookup"><span data-stu-id="d44f9-290">The **\_SaveCacheToDom** method writes the property values stored in the in-memory cache to the XMLdocument object.</span></span>


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



<span data-ttu-id="d44f9-291">Chiedere quindi se il pecified supporta [**IDestinationStreamFactory.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory)</span><span class="sxs-lookup"><span data-stu-id="d44f9-291">Next, ask whether the pecified supports [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).</span></span>


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



<span data-ttu-id="d44f9-292">Eseguire quindi il commit del flusso originale, che scrive di nuovo i dati nel file originale in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="d44f9-292">Next, commit the original stream, which writes the data back to the original file in a safe manner.</span></span>


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



<span data-ttu-id="d44f9-293">Esaminare quindi **\_ l'implementazione di SaveCacheToDom.**</span><span class="sxs-lookup"><span data-stu-id="d44f9-293">Then examine the **\_SaveCacheToDom** implementation.</span></span>


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



<span data-ttu-id="d44f9-294">Ottenere quindi il numero di proprietà archiviate nella cache in memoria.</span><span class="sxs-lookup"><span data-stu-id="d44f9-294">Next, get the number of properties stored in the in-memory cache.</span></span>


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



<span data-ttu-id="d44f9-295">Scorrere ora le proprietà per determinare se il valore di una proprietà è stato modificato dopo il caricamento in memoria.</span><span class="sxs-lookup"><span data-stu-id="d44f9-295">Now iterate through the properties to determine whether the value of a property has been changed since it was loaded into memory.</span></span>


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



<span data-ttu-id="d44f9-296">Il [**metodo IPropertyStoreCache::GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) ottiene lo stato della proprietà nella cache.</span><span class="sxs-lookup"><span data-stu-id="d44f9-296">The [**IPropertyStoreCache::GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) method gets the state of the property in the cache.</span></span> <span data-ttu-id="d44f9-297">Il flag DIRTY di PSC, impostato nell'implementazione \_ di [**IPropertyStore::SetValue,**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) contrassegna una proprietà come modificata.</span><span class="sxs-lookup"><span data-stu-id="d44f9-297">The PSC\_DIRTY flag, which was set in the [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) implementation, marks a property as changed.</span></span>


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



<span data-ttu-id="d44f9-298">Eseguire il mapping della proprietà al nodo XML come specificato nella **matrice \_ rgPropertyMap.**</span><span class="sxs-lookup"><span data-stu-id="d44f9-298">Map the property to the XML node as specified in the **eg\_rgPropertyMap** array.</span></span>


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



<span data-ttu-id="d44f9-299">Se una proprietà non è presente nella mappa, è una nuova proprietà impostata da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="d44f9-299">If a property is not in the map, it is a new property that was set by Windows Explorer.</span></span> <span data-ttu-id="d44f9-300">Poiché i metadati aperti sono supportati, salvare la nuova proprietà nella **sezione ExtendedProperties** del codice XML.</span><span class="sxs-lookup"><span data-stu-id="d44f9-300">Because open metadata is supported, save the new property in the **ExtendedProperties** section of the XML.</span></span>


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a><span data-ttu-id="d44f9-301">Implementazione di IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="d44f9-301">Implementing IPropertyStoreCapabilities</span></span>

<span data-ttu-id="d44f9-302">[**IPropertyStoreCapabilities informa**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) l'interfaccia utente della shell se una determinata proprietà può essere modificata nell'interfaccia utente della shell.</span><span class="sxs-lookup"><span data-stu-id="d44f9-302">[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informs the Shell UI whether a particular property can be edited in the Shell UI.</span></span> <span data-ttu-id="d44f9-303">È importante notare che ciò riguarda solo la possibilità di modificare la proprietà nell'interfaccia utente, non se è possibile chiamare [**correttamente IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) sulla proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-303">It is important to note that this relates only to the ability to edit the property in the UI, not whether you can successfully call [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) on the property.</span></span> <span data-ttu-id="d44f9-304">Una proprietà che provoca un valore restituito S FALSE da \_ [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) potrebbe comunque essere impostata tramite un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d44f9-304">A property that provokes a return value of S\_FALSE from [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) might still be capable of being set through an application.</span></span>


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



<span data-ttu-id="d44f9-305">[**IsPropertyWritable restituisce**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) **S \_ OK** per indicare che agli utenti finali deve essere consentito modificare direttamente la proprietà. S \_ FALSE indica che non dovrebbero.</span><span class="sxs-lookup"><span data-stu-id="d44f9-305">[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) returns **S\_OK** to indicate that end users should be allowed to edit the property directly; S\_FALSE indicates that they should not.</span></span> <span data-ttu-id="d44f9-306">S \_ FALSE può significare che le applicazioni sono responsabili della scrittura della proprietà, non degli utenti.</span><span class="sxs-lookup"><span data-stu-id="d44f9-306">S\_FALSE can mean that applications are responsible for writing the property, not users.</span></span> <span data-ttu-id="d44f9-307">Shell disabilita la modifica dei controlli in base ai risultati delle chiamate a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d44f9-307">The Shell disables editing controls as appropriate based on the results of calls to this method.</span></span> <span data-ttu-id="d44f9-308">Si presuppone che un gestore che non [**implementa IPropertyStoreCapabilities supporti**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) i metadati aperti tramite il supporto per la scrittura di qualsiasi proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-308">A handler that does not implement [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) is assumed to support open metadata through support for the writing of any property.</span></span>

<span data-ttu-id="d44f9-309">Se si compila un gestore che gestisce solo proprietà di sola lettura, è necessario implementare il metodo **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)o [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) in modo che restituisca STG E ACCESSDENIED quando viene chiamato con il \_ flag \_ STGM \_ READWRITE.</span><span class="sxs-lookup"><span data-stu-id="d44f9-309">If you are building a handler that handles only read-only properties, then you should implement your **Initialize** method ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem), or [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) so that it returns STG\_E\_ACCESSDENIED when called with the STGM\_READWRITE flag.</span></span>

<span data-ttu-id="d44f9-310">Per alcune proprietà [l'attributo isInnate](./propdesc-schema-typeinfo.md) è impostato su **true.**</span><span class="sxs-lookup"><span data-stu-id="d44f9-310">Some properties have their [isInnate](./propdesc-schema-typeinfo.md) attribute set to **true**.</span></span> <span data-ttu-id="d44f9-311">Le proprietà innate hanno le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="d44f9-311">Innate properties have the following characteristics:</span></span>

-   <span data-ttu-id="d44f9-312">La proprietà viene in genere calcolata in qualche modo.</span><span class="sxs-lookup"><span data-stu-id="d44f9-312">The property is usually calculated in some way.</span></span> <span data-ttu-id="d44f9-313">Ad esempio, `System.Image.BitDepth` viene calcolato dall'immagine stessa.</span><span class="sxs-lookup"><span data-stu-id="d44f9-313">For instance, `System.Image.BitDepth` is calculated from the image itself.</span></span>
-   <span data-ttu-id="d44f9-314">La modifica della proprietà non avrebbe senso senza modificare il file.</span><span class="sxs-lookup"><span data-stu-id="d44f9-314">Changing the property would not make sense without changing the file.</span></span> <span data-ttu-id="d44f9-315">Ad esempio, la modifica non ridimensiona l'immagine, quindi non ha senso consentire `System.Image.Dimensions` all'utente di modificarla.</span><span class="sxs-lookup"><span data-stu-id="d44f9-315">For instance, changing `System.Image.Dimensions` would not resize the image, so it does not make sense to allow the user to change it.</span></span>
-   <span data-ttu-id="d44f9-316">In alcuni casi, queste proprietà vengono fornite automaticamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d44f9-316">In some cases, these properties are provided automatically by the system.</span></span> <span data-ttu-id="d44f9-317">Ad esempio, , fornito dal file system, e , che si basa sull'utente con cui `System.DateModified` `System.SharedWith` condivide il file.</span><span class="sxs-lookup"><span data-stu-id="d44f9-317">Examples include `System.DateModified`, which is provided by the file system, and `System.SharedWith`, which is based on who the user is sharing the file with.</span></span>

<span data-ttu-id="d44f9-318">A causa di queste caratteristiche, le proprietà contrassegnate come *IsInnate* vengono fornite all'utente nell'interfaccia utente della shell solo come proprietà di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d44f9-318">Due to these characteristics, properties marked as *IsInnate* are provided to the user in the Shell UI only as read-only properties.</span></span> <span data-ttu-id="d44f9-319">Se una proprietà è contrassegnata come *IsInnate,* il sistema di proprietà non archivia tale proprietà nel gestore delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d44f9-319">If a property is marked as *IsInnate*, the property system does not store that property in the property handler.</span></span> <span data-ttu-id="d44f9-320">Pertanto, i gestori delle proprietà non necessitano di codice speciale per la gestione di queste proprietà nelle rispettive implementazioni.</span><span class="sxs-lookup"><span data-stu-id="d44f9-320">Therefore, property handlers do not need special code to account for these properties in their implementations.</span></span> <span data-ttu-id="d44f9-321">Se il valore *dell'attributo IsInnate* non viene dichiarato in modo esplicito per una determinata proprietà, il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d44f9-321">If the value of the *IsInnate* attribute is not explicitly stated for a particular property, the default value is **false**.</span></span>

## <a name="registering-and-distributing-property-handlers"></a><span data-ttu-id="d44f9-322">Registrazione e distribuzione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-322">Registering and Distributing Property Handlers</span></span>

<span data-ttu-id="d44f9-323">Con il gestore della proprietà implementato, deve essere registrato e la relativa estensione di file associata al gestore.</span><span class="sxs-lookup"><span data-stu-id="d44f9-323">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="d44f9-324">Per altre informazioni, vedere [Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md).</span><span class="sxs-lookup"><span data-stu-id="d44f9-324">For more information, see [Registering and Distributing Property Handlers](./prophand-reg-dist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d44f9-325">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d44f9-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d44f9-326">Informazioni sui gestori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-326">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="d44f9-327">Uso dei nomi dei tipi</span><span class="sxs-lookup"><span data-stu-id="d44f9-327">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="d44f9-328">Uso degli elenchi di proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-328">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="d44f9-329">Registrazione e distribuzione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-329">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="d44f9-330">Procedure consigliate e domande frequenti sul gestore delle proprietà</span><span class="sxs-lookup"><span data-stu-id="d44f9-330">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
