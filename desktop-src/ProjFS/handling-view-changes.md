---
title: Gestione delle modifiche della visualizzazione
description: Viene descritto come aggiornare la visualizzazione client dell'archivio di backup di un provider.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 1d5a709752f92b7449d2ccc38f67c4417edf8d62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046863"
---
# <a name="handling-view-changes"></a><span data-ttu-id="496fc-103">Gestione delle modifiche della visualizzazione</span><span class="sxs-lookup"><span data-stu-id="496fc-103">Handling View Changes</span></span>

<span data-ttu-id="496fc-104">Quando si aprono i file e le directory sotto la radice di virtualizzazione, il provider crea segnaposto sul disco e, quando i file vengono letti, i segnaposto vengono idratati con il contenuto.</span><span class="sxs-lookup"><span data-stu-id="496fc-104">As files and directories under the virtualization root are opened, the provider creates placeholders on disk, and as files are read the placeholders are hydrated with contents.</span></span>  <span data-ttu-id="496fc-105">Questi segnaposto rappresentano lo stato dell'archivio di backup nel momento in cui sono stati creati.</span><span class="sxs-lookup"><span data-stu-id="496fc-105">These placeholders represent the state of the backing store at the time they were created.</span></span>  <span data-ttu-id="496fc-106">Questi elementi memorizzati nella cache, combinati con gli elementi proiettati dal provider nelle enumerazioni, costituiscono la "visualizzazione" del client dell'archivio di backup.</span><span class="sxs-lookup"><span data-stu-id="496fc-106">These cached items, combined with the items projected by the provider in enumerations, constitute the client's "view" of the backing store.</span></span>  <span data-ttu-id="496fc-107">Di tanto in tanto il provider può voler aggiornare la visualizzazione del client, sia a causa di modifiche nell'archivio di backup, sia a causa di un'azione esplicita eseguita dall'utente per modificare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="496fc-107">From time to time the provider may wish to update the client's view, whether because of changes in the backing store, or because of explicit action taken by the user to change their view.</span></span>

> <span data-ttu-id="496fc-108">Se il provider aggiorna la visualizzazione in modo proattivo, quando viene modificato l'archivio di backup, è consigliabile che la visualizzazione delle modifiche sia relativamente poco frequente.</span><span class="sxs-lookup"><span data-stu-id="496fc-108">If the provider updates the view proactively, as the backing store changes, it is recommended that view changes be relatively infrequent.</span></span>  <span data-ttu-id="496fc-109">Ciò è dovuto al fatto che una vista è stata modificata in un elemento che è stato aperto e pertanto dispone di un segnaposto creato sul disco, richiede che l'elemento su disco venga aggiornato o eliminato per riflettere la modifica della vista.</span><span class="sxs-lookup"><span data-stu-id="496fc-109">This is because a view change to an item that has been opened, and therefore had a placeholder created on disk, requires that the on-disk item be either updated or deleted to reflect the view change.</span></span>  <span data-ttu-id="496fc-110">Gli aggiornamenti frequenti possono comportare attività aggiuntive del disco che possono influire negativamente sulle prestazioni del sistema.</span><span class="sxs-lookup"><span data-stu-id="496fc-110">Frequent updates may result in extra disk activity that can negatively impact system performance.</span></span>

## <a name="item-versioning"></a><span data-ttu-id="496fc-111">Controllo delle versioni degli elementi</span><span class="sxs-lookup"><span data-stu-id="496fc-111">Item Versioning</span></span>

<span data-ttu-id="496fc-112">Per supportare la gestione di più visualizzazioni, ProjFS fornisce lo struct **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** .</span><span class="sxs-lookup"><span data-stu-id="496fc-112">To support maintaining multiple views, ProjFS provides the **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.</span></span>  <span data-ttu-id="496fc-113">Un provider usa questo struct autonomo nelle chiamate a **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** e viene incorporato negli struct **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** e **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** .</span><span class="sxs-lookup"><span data-stu-id="496fc-113">A provider uses this struct standalone in calls to **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)**, and it is embedded in the **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** and **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** structs.</span></span>  <span data-ttu-id="496fc-114">**PRJ_PLACEHOLDER_VERSION_INFO**. Il campo ContentID è il punto in cui il provider archivia fino a 128 byte di informazioni sulla versione per un file o una directory.</span><span class="sxs-lookup"><span data-stu-id="496fc-114">The **PRJ_PLACEHOLDER_VERSION_INFO**.ContentID field is where the provider stores up to 128 bytes of version information for a file or directory.</span></span>  <span data-ttu-id="496fc-115">Il provider può quindi associare internamente questo valore a un valore che identifica una visualizzazione specifica.</span><span class="sxs-lookup"><span data-stu-id="496fc-115">The provider may then internally associate this value to some value that identifies a particular view.</span></span>

<span data-ttu-id="496fc-116">Ad esempio, un provider che virtualizza un repository del controllo del codice sorgente può scegliere di usare un hash del contenuto di un file per fungere da ContentID e potrebbe usare i timestamp per identificare le visualizzazioni del repository in diversi momenti.</span><span class="sxs-lookup"><span data-stu-id="496fc-116">For example, a provider that virtualizes a source control repository might choose to use a hash of a file's contents to serve as the ContentID, and it might use timestamps to identify views of the repository at various points in time.</span></span>  <span data-ttu-id="496fc-117">I timestamp potrebbero essere i tempi di esecuzione dei commit nel repository.</span><span class="sxs-lookup"><span data-stu-id="496fc-117">The timestamps might be the times that commits to the repository were performed.</span></span>

<span data-ttu-id="496fc-118">Usando l'esempio di un repository con indicizzazione timestamp, un flusso tipico per l'uso di ContentID di un elemento potrebbe essere:</span><span class="sxs-lookup"><span data-stu-id="496fc-118">Using the example of a timestamp-indexed repository, a typical flow for using an item's ContentID might be:</span></span>

1. <span data-ttu-id="496fc-119">Il client stabilisce una visualizzazione specificando il timestamp in corrispondenza del quale presentare il contenuto del repository.</span><span class="sxs-lookup"><span data-stu-id="496fc-119">The client establishes a view by specifying the timestamp at which to present the repository contents.</span></span>  <span data-ttu-id="496fc-120">Questa operazione viene eseguita tramite un'interfaccia implementata dal provider, non tramite un'API ProjFS.</span><span class="sxs-lookup"><span data-stu-id="496fc-120">This would be done through some interface implemented by the provider, not via a ProjFS API.</span></span>  <span data-ttu-id="496fc-121">Ad esempio, il provider può disporre di uno strumento da riga di comando che può essere utilizzato per indicare al provider la visualizzazione desiderata.</span><span class="sxs-lookup"><span data-stu-id="496fc-121">For example, the provider may have a command-line tool that could be used to tell the provider which view the user desires.</span></span>
1. <span data-ttu-id="496fc-122">Quando il client crea un handle per un file o una directory virtualizzata, il provider crea un segnaposto per tale oggetto, usando file system metadati dall'archivio di backup.</span><span class="sxs-lookup"><span data-stu-id="496fc-122">When the client creates a handle to a virtualized file or directory, the provider creates a placeholder for it, using file system metadata from the backing store.</span></span>  <span data-ttu-id="496fc-123">Il set specifico di metadati usato viene identificato dal valore ContentID associato al timestamp della visualizzazione desiderata.</span><span class="sxs-lookup"><span data-stu-id="496fc-123">The particular set of metadata it uses is identified by the ContentID value associated with the timestamp of the desired view.</span></span>  <span data-ttu-id="496fc-124">Quando il provider chiama **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** per scrivere le informazioni sul segnaposto, fornisce ContentId nel membro VERSIONINFO dell'argomento _placeholderInfo_ .</span><span class="sxs-lookup"><span data-stu-id="496fc-124">When the provider calls **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to write the placeholder information, it supplies the ContentID in the VersionInfo member of the _placeholderInfo_ argument.</span></span>  <span data-ttu-id="496fc-125">Il provider deve quindi registrare che in questa visualizzazione è stato creato un segnaposto per il file o la directory.</span><span class="sxs-lookup"><span data-stu-id="496fc-125">The provider should then record that a placeholder for that file or directory was created in this view.</span></span>
1. <span data-ttu-id="496fc-126">Quando il client legge da un segnaposto, viene richiamato il callback **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** del provider.</span><span class="sxs-lookup"><span data-stu-id="496fc-126">When the client reads from a placeholder, the provider's **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback is invoked.</span></span>  <span data-ttu-id="496fc-127">Il membro VersionInfo del parametro _callBackData_ contiene ContentId il provider specificato in **PrjWritePlaceholderInfo** durante la creazione del segnaposto del file.</span><span class="sxs-lookup"><span data-stu-id="496fc-127">The _callbackData_ parameter's VersionInfo member contains the ContentID the provider specified in **PrjWritePlaceholderInfo** when it created the file placeholder.</span></span>  <span data-ttu-id="496fc-128">Il provider usa tale ContentID per recuperare il contenuto corretto del file dal relativo archivio di backup.</span><span class="sxs-lookup"><span data-stu-id="496fc-128">The provider uses that ContentID to retrieve the correct contents of the file from its backing store.</span></span>
1. <span data-ttu-id="496fc-129">Il client richiede una modifica della visualizzazione specificando un nuovo timestamp.</span><span class="sxs-lookup"><span data-stu-id="496fc-129">The client requests a view change by specifying a new timestamp.</span></span>  <span data-ttu-id="496fc-130">Per ogni segnaposto creato dal provider nella visualizzazione precedente, se nella nuova visualizzazione è presente una versione diversa del file, il provider può sostituire il segnaposto sul disco con un oggetto aggiornato il cui ContentID è associato al nuovo timestamp chiamando **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span><span class="sxs-lookup"><span data-stu-id="496fc-130">For each placeholder the provider created in the previous view, if a different version of that file exists in the new view the provider may replace the placeholder on disk with an updated one whose ContentID is associated with the new timestamp by calling **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span></span>  <span data-ttu-id="496fc-131">In alternativa, il provider può eliminare il segnaposto chiamando **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** in modo che la nuova vista del file venga proiettata nelle enumerazioni.</span><span class="sxs-lookup"><span data-stu-id="496fc-131">Alternatively, the provider may delete the placeholder by calling **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** so that the new view of the file will be projected in enumerations.</span></span>  <span data-ttu-id="496fc-132">Se il file non esiste nella nuova visualizzazione, il provider deve eliminarlo chiamando **PrjDeleteFile**.</span><span class="sxs-lookup"><span data-stu-id="496fc-132">If the file does not exist in the new view, the provider must delete it by calling **PrjDeleteFile**.</span></span>

<span data-ttu-id="496fc-133">Si noti che il provider deve garantire che, quando il client enumera una directory, il provider fornirà il contenuto che corrisponde alla visualizzazione del client.</span><span class="sxs-lookup"><span data-stu-id="496fc-133">Note that the provider must ensure that when the client enumerates a directory, the provider will supply the contents that correspond to the client's view.</span></span>  <span data-ttu-id="496fc-134">Ad esempio, il provider può usare il membro VersionInfo del parametro _callBackData_ del **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** e **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** i callback per recuperare il contenuto della directory in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="496fc-134">For example, the provider could use the VersionInfo member of the _callbackData_ parameter of the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** and **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** callbacks to retrieve directory contents on the fly.</span></span>  <span data-ttu-id="496fc-135">In alternativa, è possibile creare una struttura di directory per tale visualizzazione nell'archivio di backup come parte della definizione della vista e quindi semplicemente enumerare la struttura.</span><span class="sxs-lookup"><span data-stu-id="496fc-135">Alternatively it could build a directory structure for that view in its backing store as part of establishing the view, and then simply enumerate that structure.</span></span>

> <span data-ttu-id="496fc-136">Ogni volta che un callback del provider viene richiamato per un segnaposto o un file parziale, le informazioni sulla versione specificate dal provider durante la creazione dell'elemento vengono fornite nel membro VersionInfo del parametro _callBackData_ del callback.</span><span class="sxs-lookup"><span data-stu-id="496fc-136">Whenever a provider callback is invoked for a placeholder or partial file, the version information the provider specified when creating the item is provided in the VersionInfo member of the callback's _callbackData_ parameter.</span></span>

## <a name="updating-the-view"></a><span data-ttu-id="496fc-137">Aggiornamento della vista</span><span class="sxs-lookup"><span data-stu-id="496fc-137">Updating the View</span></span>

<span data-ttu-id="496fc-138">Di seguito è riportata una funzione di esempio che illustra come un provider potrebbe aggiornare la visualizzazione locale quando l'utente specifica un nuovo timestamp.</span><span class="sxs-lookup"><span data-stu-id="496fc-138">Below is a sample function illustrating how a provider might update the local view when the user specifies a new timestamp.</span></span>  <span data-ttu-id="496fc-139">La funzione recupera un elenco dei segnaposto creati dal provider per la visualizzazione da cui l'utente ha appena modificato e aggiorna lo stato della cache locale in base allo stato di ogni segnaposto nella nuova vista.</span><span class="sxs-lookup"><span data-stu-id="496fc-139">The function retrieves a list of the placeholders the provider created for the view the user has just changed from, and updates the local cache state based on each placeholder's state in the new view.</span></span>  <span data-ttu-id="496fc-140">Per maggiore chiarezza, questa routine omette alcune complessità relative alla gestione del file system.</span><span class="sxs-lookup"><span data-stu-id="496fc-140">For clarity, this routine omits certain complexities of dealing with the file system.</span></span>  <span data-ttu-id="496fc-141">Nella visualizzazione precedente, ad esempio, è possibile che esista una determinata directory con alcuni file o directory, ma nella nuova visualizzazione la directory (e il relativo contenuto) potrebbe non esistere più.</span><span class="sxs-lookup"><span data-stu-id="496fc-141">For example, in the old view a given directory may have existed with some files or directories in it, but in the new view that directory (and its contents) may no longer exist.</span></span>  <span data-ttu-id="496fc-142">Per evitare che si verifichino errori in una situazione di questo tipo, il provider deve aggiornare lo stato del file e delle directory sotto la radice di virtualizzazione in modo approfondito.</span><span class="sxs-lookup"><span data-stu-id="496fc-142">To avoid encountering errors in such a situation the provider should update the state of the file and directories beneath the virtualization root in a depth-first fashion.</span></span>

```C++
typedef struct MY_ON_DISK_PLACEHOLDER MY_ON_DISK_PLACEHOLDER;

typedef struct MY_ON_DISK_PLACEHOLDER {
    MY_ON_DISK_PLACEHOLDER* Next;
    PWSTR RelativePath;
} MY_ON_DISK_PLACEHOLDER;

HRESULT
MyViewUpdater(
    _In_ PRJ_CALLBACK_DATA callbackData,
    _In_ time_t newViewTime
    )
{
    HRESULT hr = S_OK;

    // MyGetOnDiskPlaceholders is a routine the provider might implement to produce
    // a pointer to a list of the placeholders the provider has created in the view.
    MY_ON_DISK_PLACEHOLDER* placeholder = MyGetOnDiskPlaceholders();
    while (placeholder != NULL)
    {
        // MyGetProjectedFileInfo is a routine the provider might implement to
        // determine whether a given file exists in its backing store at a
        // particular timestamp.  If it does, the routine returns a pointer to
        // a PRJ_PLACEHOLDER_INFO struct populated with information about the
        // file.
        PRJ_PLACEHOLDER_INFO* newViewPlaceholderInfo = NULL;
        UINT32 newViewPlaceholderInfoSize = 0;

        newViewPlaceholderInfo = MyGetProjectedFileInfo(placeholder->RelativePath,
                                                 newViewTime,
                                                 &newViewPlaceholderInfoSize);
        if (newViewPlaceholderInfo == NULL)
        {
            // The file no longer exists in the new view.  We want to remove its
            // placeholder from the local cache.
            PRJ_UPDATE_FAILURE_CAUSES deleteFailureReason;
            hr = PrjDeleteFile(callbackData->NamespaceVirtualizationContext,
                               placeholder->RelativePath,
                               PRJ_UPDATE_ALLOW_DIRTY_METADATA
                               | PRJ_UPDATE_ALLOW_DIRTY_DATA
                               | PRJ_UPDATE_ALLOW_TOMBSTONE,
                               &deleteFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not delete [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", deleteFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error deleting [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyRemovePlaceholderData is a routine the provider might implement
            // to remove an item from its list of placeholders it has created in
            // the view.
            MyRemovePlaceholderData(placeholder);
        }
        else
        {
            // The file exists in the new view.  Its local cache state may need
            // to be updated, for example if its content is different in this view.
            // As an optimization, the provider may compare the file's ContentID
            // in the new view (stored in newViewPlaceholderInfo->ContentId) with
            // the ContentID it had in the old view.  If they are the same, calling
            // PrjUpdateFileIfNeeded would not be needed.
            PRJ_UPDATE_FAILURE_CAUSES updateFailureReason;
            hr = PrjUpdateFileIfNeeded(callbackData->NamespaceVirtualizationContext,
                                       placeholder->RelativePath,
                                       newViewPlaceholderInfo,
                                       newViewPlaceholderInfoSize,
                                       PRJ_UPDATE_ALLOW_DIRTY_METADATA
                                       | PRJ_UPDATE_ALLOW_DIRTY_DATA
                                       | PRJ_UPDATE_ALLOW_TOMBSTONE,
                                       &updateFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not update [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", updateFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error updating [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyUpdatePlaceholderData is a routine the provider might implement
            // to update information about a placeholder it has created in the view.
            MyUpdatePlaceholderData(placeholder, newViewPlaceholderInfo);
        }

        placeholder = placeholder->Next;
    }

    return hr;
}
```