---
description: Personalizzare l'output di debug con ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Personalizzare l'output di debug con ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ac7dd34b19cfe1fc7835a2026ae2dd28b9dcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049222"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a><span data-ttu-id="48df7-103">Personalizzare l'output di debug con ID3D10InfoQueue (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="48df7-103">Customize Debug Output with ID3D10InfoQueue (Direct3D 10)</span></span>

<span data-ttu-id="48df7-104">La coda di informazioni viene gestita da un'interfaccia (vedere [**interfaccia ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) che archivia, recupera e filtra i messaggi di debug.</span><span class="sxs-lookup"><span data-stu-id="48df7-104">The information queue is managed by an interface (see [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) that stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="48df7-105">La coda è costituita da una coda di messaggi, da uno stack di filtri di archiviazione facoltativo e da uno stack di filtri di recupero facoltativo.</span><span class="sxs-lookup"><span data-stu-id="48df7-105">The queue consists of: a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> <span data-ttu-id="48df7-106">Lo stack del filtro di archiviazione può essere usato per filtrare i messaggi che si desidera archiviare. lo stack del filtro di recupero può essere utilizzato per filtrare i messaggi che si desidera archiviare.</span><span class="sxs-lookup"><span data-stu-id="48df7-106">The storage-filter stack can be used to filter the messages you want stored; the retrieval-filter stack can be used to filter the messages you want stored.</span></span> <span data-ttu-id="48df7-107">Dopo aver filtrato un messaggio, il messaggio verrà stampato nella finestra di debug e archiviato nello stack appropriato.</span><span class="sxs-lookup"><span data-stu-id="48df7-107">Once you have filtered a message, the message will be printed out to the debug window and stored in the appropriate stack.</span></span>

<span data-ttu-id="48df7-108">In generale:</span><span class="sxs-lookup"><span data-stu-id="48df7-108">In general:</span></span>

-   <span data-ttu-id="48df7-109">Chiamare [**ID3D10InfoQueue:: AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) per generare messaggi definiti dall'utente</span><span class="sxs-lookup"><span data-stu-id="48df7-109">Call [**ID3D10InfoQueue::AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) to generate user-defined messages</span></span>
-   <span data-ttu-id="48df7-110">La chiamata [**ID3D10InfoQueue:: GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) viene utilizzata per ottenere i messaggi (che passano un filtro di recupero facoltativo).</span><span class="sxs-lookup"><span data-stu-id="48df7-110">Call [**ID3D10InfoQueue::GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) is used to get messages (that pass an optional retrieval filter).</span></span>

## <a name="registry-controls"></a><span data-ttu-id="48df7-111">Controlli registro di sistema</span><span class="sxs-lookup"><span data-stu-id="48df7-111">Registry Controls</span></span>

<span data-ttu-id="48df7-112">Usare le chiavi del registro di sistema per modificare le impostazioni di filtro, modificare i punti di rottura e disattivare l'output di debug.</span><span class="sxs-lookup"><span data-stu-id="48df7-112">Use registry keys to adjust filter settings, adjust break points, and to mute the debug output.</span></span> <span data-ttu-id="48df7-113">Il livello di debug verificherà questi percorsi per le chiavi del registro di sistema. verrà usato il primo percorso trovato.</span><span class="sxs-lookup"><span data-stu-id="48df7-113">The debug layer will check these paths for registry keys; the first path found will be used.</span></span>

1.  <span data-ttu-id="48df7-114">HKCU \\ software \\ Microsoft \\ Direct3D \\<sottochiave definita dall'utente></span><span class="sxs-lookup"><span data-stu-id="48df7-114">HKCU\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
2.  <span data-ttu-id="48df7-115">HKLM \\ software \\ Microsoft \\ Direct3D \\<sottochiave definita dall'utente></span><span class="sxs-lookup"><span data-stu-id="48df7-115">HKLM\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
3.  <span data-ttu-id="48df7-116">HKCU \\ software \\ Microsoft \\ Direct3D</span><span class="sxs-lookup"><span data-stu-id="48df7-116">HKCU\\Software\\Microsoft\\Direct3D</span></span>

<span data-ttu-id="48df7-117">Dove:</span><span class="sxs-lookup"><span data-stu-id="48df7-117">Where:</span></span>

-   <span data-ttu-id="48df7-118">HKCU sta per l' \_ utente corrente di HKEY \_ e HKLM è il \_ computer locale HKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="48df7-118">HKCU stand for HKEY\_CURRENT\_USER, and HKLM stand for HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="48df7-119"><sottochiave definita dall'utente> è un nome arbitrario per archiviare le impostazioni di debug per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="48df7-119"><user-defined subkey> is an arbitrary name to store debug settings for an application</span></span>

### <a name="filtering-debug-messages-using-registry-keys"></a><span data-ttu-id="48df7-120">Filtro dei messaggi di debug con chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="48df7-120">Filtering Debug Messages using Registry Keys</span></span>

<span data-ttu-id="48df7-121">Se il registro di sistema contiene una chiave InfoQueueStorageFilterOverride (e è diverso da zero), i messaggi (e l'output di debug) possono essere filtrati aggiungendo i controlli del registro di sistema seguenti.</span><span class="sxs-lookup"><span data-stu-id="48df7-121">If the registry contains an InfoQueueStorageFilterOverride key (and is non-zero), then messages (and debug output) can be filtered by adding the following registry controls.</span></span>

-   <span data-ttu-id="48df7-122">Categoria silenziamento \_ DWORD \_ \* : output di debug se questa chiave è diversa da zero.</span><span class="sxs-lookup"><span data-stu-id="48df7-122">DWORD Mute\_CATEGORY\_\* - Debug output if this key is non-zero.</span></span>
-   <span data-ttu-id="48df7-123">Gravità del silenziamento DWORD \_ \_ \* : l'output di debug è disabilitato se questa chiave è diversa da zero.</span><span class="sxs-lookup"><span data-stu-id="48df7-123">DWORD Mute\_SEVERITY\_\* - Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="48df7-124">ID silenziamento \_ DWORD \_ \* : il nome o il numero del messaggio può essere usato per \* (proprio come per l' \_ ID BreakOn descritto in \_ \* precedenza).</span><span class="sxs-lookup"><span data-stu-id="48df7-124">DWORD Mute\_ID\_\* - Message name or number can be used for \* (just like for BreakOn\_ID\_\* described earlier).</span></span> <span data-ttu-id="48df7-125">L'output di debug è disabilitato se questa chiave è diversa da zero.</span><span class="sxs-lookup"><span data-stu-id="48df7-125">Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="48df7-126">Informazioni sulla gravità dello stato di inattivazione DWORD \_ \_ : l'output di debug è abilitato se questa chiave è diversa da zero.</span><span class="sxs-lookup"><span data-stu-id="48df7-126">DWORD Unmute\_SEVERITY\_INFO - Debug output is ENABLED if this key is non-zero.</span></span> <span data-ttu-id="48df7-127">Per impostazione predefinita, quando InfoQueueStorageFilterOverride è abilitato, i messaggi di debug con informazioni di gravità vengono disabilitati. Pertanto, per questa chiave è possibile riattivare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="48df7-127">By default when InfoQueueStorageFilterOverride is enabled, debug messages with severity INFO are muted - therefore for this key allows INFO to be turned back on.</span></span>

<span data-ttu-id="48df7-128">Questi controlli modificano se un messaggio viene registrato o visualizzato; non influiscono sull'eventuale esito positivo o negativo di un'API.</span><span class="sxs-lookup"><span data-stu-id="48df7-128">These controls change whether a message is recorded or displayed; they do not affect whether an API passes or fails.</span></span>

### <a name="setting-break-conditions-using-registry-keys"></a><span data-ttu-id="48df7-129">Impostazione delle condizioni di interruzioni tramite chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="48df7-129">Setting Break Conditions using Registry Keys</span></span>

<span data-ttu-id="48df7-130">Le applicazioni possono essere forzate a interrompere un messaggio usando le seguenti chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="48df7-130">Applications can be forced to break on a message using the following registry keys.</span></span>

<span data-ttu-id="48df7-131">**EnableBreakOnMessage** : questa chiave consente di suddividere i messaggi (e determina l'Ignorazione delle impostazioni di SetBreakOnCategory ()/SetBreakOnSeverity ()/SetBreakOnID ().</span><span class="sxs-lookup"><span data-stu-id="48df7-131">**EnableBreakOnMessage** - This key enables breaking on messages (and causes i's SetBreakOnCategory()/SetBreakOnSeverity()/SetBreakOnID() settings to be ignored).</span></span> <span data-ttu-id="48df7-132">I messaggi effettivi da interrompere vengono definiti usando uno o più \_ \* valori BreakOn definiti di seguito.</span><span class="sxs-lookup"><span data-stu-id="48df7-132">The actual messages to break on are defined using one or more BreakOn\_\* values defined below.</span></span>

-   <span data-ttu-id="48df7-133">\**BreakOn \_ \_Categoria \** _-Interrompi in tutti i messaggi che passano attraverso i filtri di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="48df7-133">\**BreakOn\_CATEGORY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="48df7-134">\_ è uno dei messaggi di \_ categoria del messaggio D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="48df7-134">\_ is one of the D3D10\_MESSAGE\_CATEGORY messages.</span></span>
-   <span data-ttu-id="48df7-135">\**BreakOn \_ \_Gravità \** _-Interrompi in tutti i messaggi che passano attraverso i filtri di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="48df7-135">\**BreakOn\_SEVERITY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="48df7-136">\_ è uno dei messaggi di \_ gravità del messaggio D3D10 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="48df7-136">\_ is one of the D3D10\_MESSAGE\_SEVERITY\_ messages.</span></span>
-   <span data-ttu-id="48df7-137">\**BreakOn \_ \_ID \** _-Interrompi in tutti i messaggi che passano attraverso i filtri di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="48df7-137">\**BreakOn\_ID\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="48df7-138">\_ è uno dei \_ \_ messaggi ID messaggio D3D10 \_ o può essere il valore numerico dell'enumerazione Error.</span><span class="sxs-lookup"><span data-stu-id="48df7-138">\_ is one of the D3D10\_MESSAGE\_ID\_ messages or can be the numerical value of the error enumeration.</span></span> <span data-ttu-id="48df7-139">Si supponga, ad esempio, che il messaggio con ID "D3D10 \_ message \_ ID \_ ipotetico" disponga del valore 123 nell' \_ enumerazione D3D10 message \_ ID.</span><span class="sxs-lookup"><span data-stu-id="48df7-139">For example, Suppose the message with ID "D3D10\_MESSAGE\_ID\_HYPOTHETICAL" had the value 123 in the D3D10\_MESSAGE\_ID enumeration.</span></span> <span data-ttu-id="48df7-140">In questo caso, la creazione del valore BreakOn \_ ID \_ ipotetico = 1 o BreakOn \_ ID \_ 123 = 1 avrebbe lo stesso risultato quando viene rilevato un messaggio con ID D3D10 \_ messaggio \_ ID \_ ipotetico.</span><span class="sxs-lookup"><span data-stu-id="48df7-140">In this case, creating the value BreakOn\_ID\_HYPOTHETICAL=1 or BreakOn\_ID\_123=1 would both accomplish the same thing - break when a message having ID D3D10\_MESSAGE\_ID\_HYPOTHETICAL is encountered.</span></span>

### <a name="muting-debug-output-using-registry-keys"></a><span data-ttu-id="48df7-141">Silenziamento dell'output di debug con chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="48df7-141">Muting Debug Output using Registry Keys</span></span>

<span data-ttu-id="48df7-142">L'output di debug può essere disattivato usando una chiave di MuteDebugOutput.</span><span class="sxs-lookup"><span data-stu-id="48df7-142">Debug output can be muted using a MuteDebugOutput key.</span></span> <span data-ttu-id="48df7-143">La presenza di questo valore nel registro di sistema impone l'override del metodo [**ID3D10InfoQueue:: SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) di InfoQueue.</span><span class="sxs-lookup"><span data-stu-id="48df7-143">The presence of this value in the registry forces override of the InfoQueue's [**ID3D10InfoQueue::SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) method.</span></span> <span data-ttu-id="48df7-144">MuteDebugOutput interrompe l'invio dei messaggi che passano il filtro di archiviazione all'output di debug.</span><span class="sxs-lookup"><span data-stu-id="48df7-144">MuteDebugOutput stops messages that pass the storage filter from being sent to debug output.</span></span>

## <a name="disabling-debug-layer-messages"></a><span data-ttu-id="48df7-145">Disabilitazione dei messaggi del livello di debug</span><span class="sxs-lookup"><span data-stu-id="48df7-145">Disabling Debug Layer Messages</span></span>

<span data-ttu-id="48df7-146">I messaggi del livello di debug possono essere disabilitati singolarmente o come gruppo in fase di esecuzione specificando filtri con [**ID3D10InfoQueue:: AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span><span class="sxs-lookup"><span data-stu-id="48df7-146">Debug layer messages can be disabled individualy or as a group at runtime by specifying filters using [**ID3D10InfoQueue::AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span></span> <span data-ttu-id="48df7-147">L'argomento *pFilter* di **ID3D10InfoQueue:: AddStorageFilterEntries** accetta una struttura di filtro della [**\_ \_ coda \_ di informazioni D3D10**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) che contiene un elenco Consenti e un elenco di accesso negato.</span><span class="sxs-lookup"><span data-stu-id="48df7-147">The *pFilter* argument to **ID3D10InfoQueue::AddStorageFilterEntries** takes a [**D3D10\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) structure that contains an allow list and a deny list.</span></span> <span data-ttu-id="48df7-148">Gli elenchi Consenti e nega sono descritti da [**D3D10 \_ info \_ Queue \_ Filter strutture \_ desc**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) che consentono di specificare il filtro in base a pullula, gravità e singolo ID messaggio.</span><span class="sxs-lookup"><span data-stu-id="48df7-148">The allow and deny lists are described by [**D3D10\_INFO\_QUEUE\_FILTER\_DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) structures that allow filtering to be specified by catergory, severity and individual message ID.</span></span>

<span data-ttu-id="48df7-149">Il codice seguente è un esempio di configurazione dell' [**interfaccia ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) per negare un messaggio di errore del buffer dell'indice del messaggio D3D10 message \_ ID del \_ \_ dispositivo \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="48df7-149">The following code is an example of setting up the [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) to deny the D3D10\_MESSAGE\_ID\_DEVICE\_DRAW\_INDEX\_BUFFER\_TOO\_SMALL message.</span></span>


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a><span data-ttu-id="48df7-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48df7-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48df7-151">Livelli API</span><span class="sxs-lookup"><span data-stu-id="48df7-151">API Layers</span></span>](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[<span data-ttu-id="48df7-152">Funzionalità API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="48df7-152">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



