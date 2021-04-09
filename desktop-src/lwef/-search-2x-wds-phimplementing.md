---
title: Implementazione di un gestore di protocollo per WDS
description: La creazione di un gestore di protocollo comporta l'implementazione di ISearchProtocol per la gestione di oggetti UrlAccessor, IUrlAccessor per la generazione di metadati relativi e per identificare i filtri appropriati per gli elementi nell'archivio dati, IProtocolHandlerSite per creare un'istanza di un oggetto SearchProtocol e identificare i filtri appropriati e IFilterto filtrare i file proprietari o enumerare e filtrare i file archiviati gerarchicamente.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117647"
---
# <a name="implementing-a-protocol-handler-for-wds"></a><span data-ttu-id="f00a6-103">Implementazione di un gestore di protocollo per WDS</span><span class="sxs-lookup"><span data-stu-id="f00a6-103">Implementing a Protocol Handler for WDS</span></span>

> [!NOTE]
> <span data-ttu-id="f00a6-104">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f00a6-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="f00a6-105">Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="f00a6-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="f00a6-106">La creazione di un gestore di protocollo comporta l'implementazione di [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) per la gestione di oggetti UrlAccessor, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) per la generazione di metadati relativi e per identificare i filtri appropriati per gli elementi nell'archivio dati, IProtocolHandlerSite per creare un'istanza di un oggetto SearchProtocol e identificare i filtri appropriati e [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)per filtrare i file proprietari o per enumerare e filtrare i file archiviati gerarchicamente.</span><span class="sxs-lookup"><span data-stu-id="f00a6-106">Creating a protocol handler involves implementing [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) to generate metadata about and to identify appropriate filters for items in the data store, IProtocolHandlerSite to instantiate a SearchProtocol object and identify appropriate filters, and [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span> <span data-ttu-id="f00a6-107">Il gestore di protocollo deve essere multithreading.</span><span class="sxs-lookup"><span data-stu-id="f00a6-107">The protocol handler must be multithreaded.</span></span>

<span data-ttu-id="f00a6-108">In questa sezione sono inclusi gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f00a6-108">This sections contains the following topics:</span></span>

-   [<span data-ttu-id="f00a6-109">Nota sugli URL</span><span class="sxs-lookup"><span data-stu-id="f00a6-109">Note on URLs</span></span>](#note-on-urls)
-   [<span data-ttu-id="f00a6-110">Interfacce del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="f00a6-110">Protocol Handler Interfaces</span></span>](#protocol-handler-interfaces)
-   [<span data-ttu-id="f00a6-111">IFilters per i contenitori</span><span class="sxs-lookup"><span data-stu-id="f00a6-111">IFilters for Containers</span></span>](#ifilters-for-containers)
-   [<span data-ttu-id="f00a6-112">Aggiunta della funzionalità opzioni gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="f00a6-112">Adding Protocol Handler Options Functionality</span></span>](#adding-protocol-handler-options-functionality)
    -   [<span data-ttu-id="f00a6-113">ISearchProtocolOptions</span><span class="sxs-lookup"><span data-stu-id="f00a6-113">ISearchProtocolOptions</span></span>](#isearchprotocoloptions)
-   [<span data-ttu-id="f00a6-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f00a6-114">Related topics</span></span>](#related-topics)

## <a name="note-on-urls"></a><span data-ttu-id="f00a6-115">Nota sugli URL</span><span class="sxs-lookup"><span data-stu-id="f00a6-115">Note on URLs</span></span>

<span data-ttu-id="f00a6-116">Microsoft Windows Desktop Search (WDS) USA gli URL per identificare in modo univoco gli elementi in un file system, all'interno di un archivio di tipo database o sul Web.</span><span class="sxs-lookup"><span data-stu-id="f00a6-116">Microsoft Windows Desktop Search (WDS) uses URLs to uniquely identify items in a file system, inside a database-like store, or on the Web.</span></span> <span data-ttu-id="f00a6-117">Un URL che definisce un nodo di immissione è denominato pagina iniziale; WDS inizia da tale pagina iniziale e ricerca in modo ricorsivo l'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="f00a6-117">A URL that defines an entry node is called a start page; WDS begins at that start page and recursively crawls the data store.</span></span> <span data-ttu-id="f00a6-118">La struttura di URL tipica è la seguente:</span><span class="sxs-lookup"><span data-stu-id="f00a6-118">The typical URL structure is:</span></span>

`protocol://host/path/name.extension`

> [!Note]
>
> <span data-ttu-id="f00a6-119">Quando si vuole aggiungere un nuovo archivio dati, è necessario selezionare un nome per identificarlo che non sia in conflitto con quelli correnti.</span><span class="sxs-lookup"><span data-stu-id="f00a6-119">When you want to add a new data store, you'll need to select a name to identify it that does not conflict with current ones.</span></span> <span data-ttu-id="f00a6-120">Questa convenzione di denominazione è consigliata: companyName. Scheme.</span><span class="sxs-lookup"><span data-stu-id="f00a6-120">We recommend this naming convention: companyName.scheme.</span></span>

 

## <a name="protocol-handler-interfaces"></a><span data-ttu-id="f00a6-121">Interfacce del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="f00a6-121">Protocol Handler Interfaces</span></span>

<span data-ttu-id="f00a6-122">**ISearchProtocol**</span><span class="sxs-lookup"><span data-stu-id="f00a6-122">**ISearchProtocol**</span></span>

<span data-ttu-id="f00a6-123">L'interfaccia [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) richiama, Inizializza e gestisce gli oggetti UrlAccessor.</span><span class="sxs-lookup"><span data-stu-id="f00a6-123">The [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) interface invokes, initializes, and manages UrlAccessor objects.</span></span> <span data-ttu-id="f00a6-124">Per ulteriori informazioni sull'implementazione dell'interfaccia ISearchProtocol, vedere **riferimento all'interfaccia ISearchProtocol**.</span><span class="sxs-lookup"><span data-stu-id="f00a6-124">For more information on implementing the ISearchProtocol interface, see **ISearchProtocol Interface reference**.</span></span>

<span data-ttu-id="f00a6-125">**IUrlAccessor**</span><span class="sxs-lookup"><span data-stu-id="f00a6-125">**IUrlAccessor**</span></span>

<span data-ttu-id="f00a6-126">Per un URL specificato, l'interfaccia [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) genera i metadati sulla struttura del percorso e sugli elementi contenuti e associa tali elementi a un filtro.</span><span class="sxs-lookup"><span data-stu-id="f00a6-126">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface generates metadata about the location structure as well as contained items, and it binds those items to an filter.</span></span> <span data-ttu-id="f00a6-127">Viene creata un'istanza dell'oggetto **IUrlAccessor** che viene inizializzato da un oggetto SearchProtocol. Tuttavia, è anche possibile implementare un metodo di inizializzazione interna, in modo che l'oggetto **IUrlAccessor** possa eseguire attività di inizializzazione specifiche del gestore di protocollo, ad esempio la convalida dell'URL per un elemento a cui si accede o il controllo dell'ora dell'Ultima modifica per determinare se un file deve essere elaborato nella ricerca corrente.</span><span class="sxs-lookup"><span data-stu-id="f00a6-127">The **IUrlAccessor** object is instantiated and initialized by an SearchProtocol object; however, you can also implement an internal initialization method so your **IUrlAccessor** object can perform initialization tasks specific to your protocol handler, such as validating the URL for an item being accessed or checking the last modified time to determine if a file must be processed in the current crawl.</span></span>

> [!Note]
>
> <span data-ttu-id="f00a6-128">Gli orari modificati per le directory vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="f00a6-128">Modified times for directories are ignored.</span></span> <span data-ttu-id="f00a6-129">L'oggetto [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) deve enumerare gli oggetti figlio per determinare se sono state apportate modifiche o eliminazioni.</span><span class="sxs-lookup"><span data-stu-id="f00a6-129">The [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) object must enumerate the child objects to determine whether there have been any modifications or deletions.</span></span>

 

<span data-ttu-id="f00a6-130">Gran parte della progettazione dell'oggetto **UrlAccessor** dipende dal fatto che la struttura sia gerarchica o basata sul collegamento.</span><span class="sxs-lookup"><span data-stu-id="f00a6-130">Much of the design of the **UrlAccessor** object is dependent on whether the structure is hierarchical or link-based.</span></span> <span data-ttu-id="f00a6-131">Per gli archivi dati gerarchici, l'oggetto **UrlAccessor** deve trovare un filtro in grado di enumerarne il contenuto.</span><span class="sxs-lookup"><span data-stu-id="f00a6-131">For hierarchical data stores, the **UrlAccessor** object must find an filter that can enumerate their contents.</span></span> <span data-ttu-id="f00a6-132">Un'altra distinzione tra i gestori di protocollo gerarchici e basati sui collegamenti è l'utilizzo del metodo di directory.</span><span class="sxs-lookup"><span data-stu-id="f00a6-132">Another distinction between hierarchical and link-based protocol handlers is the use of the IsDirectory method.</span></span> <span data-ttu-id="f00a6-133">Nei gestori di protocollo basati sul collegamento, questo metodo deve restituire S \_ false.</span><span class="sxs-lookup"><span data-stu-id="f00a6-133">In link-based protocol handlers, this method should return S\_FALSE.</span></span> <span data-ttu-id="f00a6-134">I gestori di protocollo gerarchico devono restituire S \_ OK per i contenitori.</span><span class="sxs-lookup"><span data-stu-id="f00a6-134">Hierarchical protocol handlers must return S\_OK for containers.</span></span>

<span data-ttu-id="f00a6-135">Per altre istruzioni sull'implementazione di un'interfaccia [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) , vedere informazioni di riferimento sull' [**interfaccia IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) .</span><span class="sxs-lookup"><span data-stu-id="f00a6-135">For further instructions on implementing an [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface, see the [**IUrlAccessor Interface**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) reference.</span></span>

<span data-ttu-id="f00a6-136">**IProtocolHandlerSite**</span><span class="sxs-lookup"><span data-stu-id="f00a6-136">**IProtocolHandlerSite**</span></span>

<span data-ttu-id="f00a6-137">Questa interfaccia viene utilizzata per creare un'istanza di un oggetto **SearchProtocol** e fornisce anche l'oggetto **UrlAccessor** con un filtro appropriato per un ID di classe specificato (CLSID).</span><span class="sxs-lookup"><span data-stu-id="f00a6-137">This interface is used to instantiate a **SearchProtocol** object and also provides the **UrlAccessor** object with an appropriate filter for a specified class ID (CLSID).</span></span>

## <a name="ifilters-for-containers"></a><span data-ttu-id="f00a6-138">IFilters per i contenitori</span><span class="sxs-lookup"><span data-stu-id="f00a6-138">IFilters for Containers</span></span>

<span data-ttu-id="f00a6-139">Se si implementa un gestore di protocollo gerarchico, è necessario implementare un componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)del contenitore che enumera gli URL che rappresentano i contenitori o le cartelle.</span><span class="sxs-lookup"><span data-stu-id="f00a6-139">If you are implementing a hierarchical protocol handler, you must implement a container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component that enumerates URLs representing containers or folders.</span></span> <span data-ttu-id="f00a6-140">Il processo di enumerazione è un ciclo attraverso i metodi **GetChunk** e **GetValue** dell'interfaccia IFilter che restituiscono un elenco di URL che rappresentano ogni elemento nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="f00a6-140">The enumeration process is a loop through the **GetChunk** and **GetValue** methods of the IFilter interface that return a list of URLs that represent each item in the container.</span></span>

<span data-ttu-id="f00a6-141">In primo luogo, **GetChunk** restituisce un FULLPROSPEC con il set di proprietà gather \_ propset e uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="f00a6-141">First, **GetChunk** returns a FULLPROSPEC with the property set GATHER\_PROPSET and either:</span></span>

-   <span data-ttu-id="f00a6-142">PID \_ gthr \_ DIRLINK, l'URL dell'elemento senza l'ora dell'Ultima modifica o</span><span class="sxs-lookup"><span data-stu-id="f00a6-142">PID\_GTHR\_DIRLINK, the URL to the item without the last modified time, or</span></span>
-   <span data-ttu-id="f00a6-143">PID \_ gthr \_ DIRLINK \_ con il \_ tempo, l'URL e l'ora dell'Ultima modifica</span><span class="sxs-lookup"><span data-stu-id="f00a6-143">PID\_GTHR\_DIRLINK\_WITH\_TIME, the URL along with the last modified time</span></span>

<span data-ttu-id="f00a6-144">Il GUID del set di proprietà per GATHER \_ propset è 0B63E343-9CCC-11D0-Bcdb-00805FCCCE04.</span><span class="sxs-lookup"><span data-stu-id="f00a6-144">The property set GUID for GATHER\_PROPSET is 0B63E343-9CCC-11D0-BCDB-00805FCCCE04.</span></span> <span data-ttu-id="f00a6-145">La proprietà Campo PROPSPEC è PID \_ gthr \_ DIRLINK = 2 o PID \_ gthr \_ DIRLINK \_ with \_ Time = 12 Decimal.</span><span class="sxs-lookup"><span data-stu-id="f00a6-145">The PROPSPEC Property is either PID\_GTHR\_DIRLINK=2 or PID\_GTHR\_DIRLINK\_WITH\_TIME = 12 decimal.</span></span>

<span data-ttu-id="f00a6-146">La restituzione \_ di PID gthr \_ DIRLINK \_ con \_ l'ora è più efficiente perché l'indicizzatore può determinare immediatamente se l'elemento deve essere indicizzato senza chiamare i metodi ISearchProtocol->CreateUrlAccessor () e IUrlAccessor->GetLastModified ().</span><span class="sxs-lookup"><span data-stu-id="f00a6-146">Returning PID\_GTHR\_DIRLINK\_WITH\_TIME is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the ISearchProtocol->CreateUrlAccessor() and IUrlAccessor->GetLastModified() methods.</span></span>

<span data-ttu-id="f00a6-147">Quindi **GetValue** restituisce un PROPVARIANT per l'URL (e l'ora dell'Ultima modifica, se usato), come:</span><span class="sxs-lookup"><span data-stu-id="f00a6-147">Then **GetValue** returns a PROPVARIANT for the URL (and last modified time if used), as either:</span></span>

-   <span data-ttu-id="f00a6-148">VT \_ LPWSTR, URL dell'elemento figlio oppure</span><span class="sxs-lookup"><span data-stu-id="f00a6-148">VT\_LPWSTR, the URL of the child item, or</span></span>
-   <span data-ttu-id="f00a6-149">Vettore dell'URL seguito da un FILETIME</span><span class="sxs-lookup"><span data-stu-id="f00a6-149">Vector of the URL followed by a FILETIME</span></span>

<span data-ttu-id="f00a6-150">Il codice di esempio seguente illustra come compilare il PID \_ gthr \_ DIRLINK appropriato \_ con il \_ tempo.</span><span class="sxs-lookup"><span data-stu-id="f00a6-150">The following sample code demonstrates how to build the proper PID\_GTHR\_DIRLINK\_WITH\_TIME.</span></span>

> [!Note]
>
> <span data-ttu-id="f00a6-151">**QUESTO CODICE E LE INFORMAZIONI VENGONO FORNITE "COSÌ COME SONO" SENZA GARANZIA DI ALCUN TIPO, ESPRESSA O IMPLICITA, INCLUSE, A TITOLO ESEMPLIFICATIVO, LE GARANZIE IMPLICITE DI COMMERCIABILITÀ E/O IDONEITÀ PER UNO SCOPO SPECIFICO.**</span><span class="sxs-lookup"><span data-stu-id="f00a6-151">**THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.**</span></span>
>
> <span data-ttu-id="f00a6-152">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f00a6-152">Copyright (C) Microsoft.</span></span> <span data-ttu-id="f00a6-153">Tutti i diritti sono riservati.</span><span class="sxs-lookup"><span data-stu-id="f00a6-153">All rights reserved.</span></span>

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
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
>
> <span data-ttu-id="f00a6-154">Un componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)del contenitore deve sempre enumerare tutti gli URL figlio anche se gli URL figlio non sono stati modificati, perché l'indicizzatore rileva le eliminazioni tramite il processo di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="f00a6-154">A container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component should always enumerate all child URLs even if the child URLs have not changed, because the Indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="f00a6-155">Se l'output della data in un \_ collegamento dir \_ con l' \_ ora indica che i dati non sono stati modificati, l'indicizzatore non aggiorna i dati per tale URL.</span><span class="sxs-lookup"><span data-stu-id="f00a6-155">If the date output in a DIR\_LINKS\_WITH\_TIME indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

<span data-ttu-id="f00a6-156">L'URL fisico è l'URL elaborato dall'oggetto **UrlAccessor** .</span><span class="sxs-lookup"><span data-stu-id="f00a6-156">The physical URL is the URL that the **UrlAccessor** object processes.</span></span> <span data-ttu-id="f00a6-157">Se il filtro non genera un DisplayUrl intuitivo, WDS Visualizza l'URL fisico all'utente come parte dei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="f00a6-157">If the filter does not emit a user-friendly DisplayUrl, WDS displays the physical URL to the user as part of the search results.</span></span> <span data-ttu-id="f00a6-158">Lo schema WDS contiene due proprietà che consentono di controllare ciò che viene visualizzato all'utente finale, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f00a6-158">The WDS schema contains two properties to control what is displayed to the end user, as shown in the table below.</span></span>



| <span data-ttu-id="f00a6-159">GUID</span><span class="sxs-lookup"><span data-stu-id="f00a6-159">GUID</span></span>                                 | <span data-ttu-id="f00a6-160">Campo PROPSPEC</span><span class="sxs-lookup"><span data-stu-id="f00a6-160">PROPSPEC</span></span>      | <span data-ttu-id="f00a6-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f00a6-161">Description</span></span>                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| <span data-ttu-id="f00a6-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="f00a6-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="f00a6-163">DisplayFolder</span><span class="sxs-lookup"><span data-stu-id="f00a6-163">DisplayFolder</span></span> | <span data-ttu-id="f00a6-164">Percorso della cartella visualizzato all'utente nei risultati della ricerca</span><span class="sxs-lookup"><span data-stu-id="f00a6-164">Folder Path displayed to the user in search results</span></span> |
| <span data-ttu-id="f00a6-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="f00a6-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="f00a6-166">FolderName</span><span class="sxs-lookup"><span data-stu-id="f00a6-166">FolderName</span></span>    | <span data-ttu-id="f00a6-167">Nome visualizzato della cartella padre</span><span class="sxs-lookup"><span data-stu-id="f00a6-167">Display name of the parent folder</span></span>                   |



 

<span data-ttu-id="f00a6-168">Se il codice non genera DisplayFolder o FolderName, questi valori vengono calcolati da DisplayUrl.</span><span class="sxs-lookup"><span data-stu-id="f00a6-168">If your code does not emit a DisplayFolder or FolderName, these values are computed from the DisplayUrl.</span></span> <span data-ttu-id="f00a6-169">Le barre nell'URL indicano i contenitori all'interno dell'archivio o file system.</span><span class="sxs-lookup"><span data-stu-id="f00a6-169">Forward slashes in the URL denote containers within the store or file system.</span></span>

## <a name="adding-protocol-handler-options-functionality"></a><span data-ttu-id="f00a6-170">Aggiunta della funzionalità opzioni gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="f00a6-170">Adding Protocol Handler Options Functionality</span></span>

<span data-ttu-id="f00a6-171">Affinché il gestore di protocollo disponga di una pagina iniziale predefinita e di un URL del nodo di ingresso, è necessario implementare l'interfaccia **ISearchProtocolOptions** .</span><span class="sxs-lookup"><span data-stu-id="f00a6-171">For your protocol handler to have a default start page (and entry node URL), you must implement the **ISearchProtocolOptions** interface.</span></span> <span data-ttu-id="f00a6-172">Nelle versioni future di WDS questa interfaccia fornirà Hook alla finestra di dialogo Opzioni per un'esperienza utente migliorata.</span><span class="sxs-lookup"><span data-stu-id="f00a6-172">In future versions of WDS, this interface will provide hooks to the Options dialog for an enhanced user experience.</span></span> <span data-ttu-id="f00a6-173">Questa interfaccia offre le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="f00a6-173">This interface provides the following functionality:</span></span>

-   <span data-ttu-id="f00a6-174">Determina se i requisiti per il gestore di protocollo sono soddisfatti.</span><span class="sxs-lookup"><span data-stu-id="f00a6-174">Determines whether the requirements for your protocol handler are met.</span></span> <span data-ttu-id="f00a6-175">Ad esempio, l'archivio del gestore di protocollo potrebbe richiedere l'accesso a una determinata applicazione per indicizzare correttamente i dati dell'applicazione, ma l'applicazione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="f00a6-175">For example, your protocol handler's store may require access to a given application to properly index the application's data but that application is unavailable.</span></span>
-   <span data-ttu-id="f00a6-176">Identifica i requisiti minimi necessari al gestore di protocollo per elaborare un elemento.</span><span class="sxs-lookup"><span data-stu-id="f00a6-176">Identifies the minimum requirements your protocol handler needs to process an item.</span></span> <span data-ttu-id="f00a6-177">I requisiti possono essere espressi in una descrizione intuitiva e localizzata, ad esempio "Microsoft Outlook 2000 o versione successiva".</span><span class="sxs-lookup"><span data-stu-id="f00a6-177">Requirements can be expressed in a user-friendly, localized description, such as "Microsoft Outlook 2000 or greater."</span></span>
-   <span data-ttu-id="f00a6-178">Definisce gli URL che devono essere elaborati dal gestore di protocollo per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f00a6-178">Defines the URLs your protocol handler should process by default.</span></span>

### <a name="isearchprotocoloptions"></a><span data-ttu-id="f00a6-179">ISearchProtocolOptions</span><span class="sxs-lookup"><span data-stu-id="f00a6-179">ISearchProtocolOptions</span></span>

<span data-ttu-id="f00a6-180">Nella tabella seguente vengono descritti i metodi che è necessario implementare per l'interfaccia **ISearchProtocolOptions** .</span><span class="sxs-lookup"><span data-stu-id="f00a6-180">The following table describes the methods you need to implement for the **ISearchProtocolOptions** interface.</span></span>



| <span data-ttu-id="f00a6-181">Metodo</span><span class="sxs-lookup"><span data-stu-id="f00a6-181">Method</span></span>               | <span data-ttu-id="f00a6-182">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f00a6-182">Description</span></span>                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f00a6-183">CheckRequirements</span><span class="sxs-lookup"><span data-stu-id="f00a6-183">CheckRequirements</span></span>    | <span data-ttu-id="f00a6-184">Determina se vengono soddisfatti i requisiti minimi di un gestore di protocollo personalizzato</span><span class="sxs-lookup"><span data-stu-id="f00a6-184">Determines whether a custom protocol handler's minimum requirements are met</span></span>                             |
| <span data-ttu-id="f00a6-185">GetDefaultCrawlScope</span><span class="sxs-lookup"><span data-stu-id="f00a6-185">GetDefaultCrawlScope</span></span> | <span data-ttu-id="f00a6-186">Restituisce un elenco di URL predefiniti all'interno di un archivio specificato per un gestore di protocollo personalizzato</span><span class="sxs-lookup"><span data-stu-id="f00a6-186">Returns a list of default URLs within a specified store for a custom protocol handler</span></span>                   |
| <span data-ttu-id="f00a6-187">Getrequirements</span><span class="sxs-lookup"><span data-stu-id="f00a6-187">GetRequirements</span></span>      | <span data-ttu-id="f00a6-188">Identifica una descrizione intuitiva e localizzata dei requisiti minimi per un gestore di protocollo personalizzato</span><span class="sxs-lookup"><span data-stu-id="f00a6-188">Identifies a user-friendly, localized description of minimum requirements for a custom protocol handler</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f00a6-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f00a6-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f00a6-190">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f00a6-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f00a6-191">Notifica dell'indice delle modifiche</span><span class="sxs-lookup"><span data-stu-id="f00a6-191">Notifying the Index of Changes</span></span>](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="f00a6-192">Aggiunta di icone, anteprime e menu di scelta rapida con le estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="f00a6-192">Adding Icons, Previews, and Context Menus with Shell Extensions</span></span>](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="f00a6-193">Installazione e registrazione di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="f00a6-193">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 