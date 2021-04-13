---
title: Fornire dati di file
description: Descrive il modo in cui un provider fornisce informazioni sui segnaposto e i dati dei file.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 341a0f1c477b605b2a437edf311c380910744ac0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399396"
---
# <a name="providing-file-data"></a><span data-ttu-id="9ba2b-103">Fornire dati di file</span><span class="sxs-lookup"><span data-stu-id="9ba2b-103">Providing File Data</span></span>

<span data-ttu-id="9ba2b-104">Quando un provider crea innanzitutto una radice di virtualizzazione, è vuota nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-104">When a provider first creates a virtualization root it is empty on the local system.</span></span> <span data-ttu-id="9ba2b-105">Ovvero, nessuno degli elementi nell'archivio dati di supporto è ancora stato memorizzato nella cache su disco.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span> <span data-ttu-id="9ba2b-106">Quando gli elementi vengono aperti, ProjFS richiede informazioni dal provider per consentire la creazione di segnaposto per tali elementi nel file system locale.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-106">As items are opened, ProjFS requests information from the provider to allow placeholders for those items to be created in the local file system.</span></span>  <span data-ttu-id="9ba2b-107">Quando si accede al contenuto dell'elemento, ProjFS richiede il contenuto del provider.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-107">As item contents are accessed, ProjFS requests those contents from the provider.</span></span>  <span data-ttu-id="9ba2b-108">Il risultato è che dal punto di vista dell'utente, i file e le directory virtualizzate appaiono simili ai file e alle directory normali che si trovano già nella file system locale.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-108">The result is that from the user's perspective, virtualized files and directories appear similar to normal files and directories that already reside on the local file system.</span></span>

## <a name="placeholder-creation"></a><span data-ttu-id="9ba2b-109">Creazione di segnaposto</span><span class="sxs-lookup"><span data-stu-id="9ba2b-109">Placeholder Creation</span></span>

<span data-ttu-id="9ba2b-110">Quando un'applicazione tenta di aprire un handle per un file virtualizzato, ProjFS chiama il callback **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** per ogni elemento del percorso che non esiste ancora sul disco.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-110">When an application attempts to open a handle to a virtualized file, ProjFS calls the **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** callback for each item of the path that does not yet exist on disk.</span></span>  <span data-ttu-id="9ba2b-111">Se, ad esempio, un'applicazione tenta di aprire `C:\virtRoot\dir1\dir2\file.txt` , ma solo il percorso `C:\virtRoot\dir1` esiste sul disco, il provider riceverà un callback per `C:\virtRoot\dir1\dir2` , quindi per `C:\virtRoot\dir1\dir2\file.txt` .</span><span class="sxs-lookup"><span data-stu-id="9ba2b-111">For example, if an application tries to open `C:\virtRoot\dir1\dir2\file.txt`, but only the path `C:\virtRoot\dir1` exists on disk, then the provider will receive a callback for `C:\virtRoot\dir1\dir2`, then for `C:\virtRoot\dir1\dir2\file.txt`.</span></span>

<span data-ttu-id="9ba2b-112">Quando ProjFS chiama il callback **PRJ_GET_PLACEHOLDER_INFO_CB** del provider, il provider esegue le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9ba2b-112">When ProjFS calls the provider's **PRJ_GET_PLACEHOLDER_INFO_CB** callback, the provider performs the following actions:</span></span>

1. <span data-ttu-id="9ba2b-113">Il provider determina se il nome richiesto esiste nell'archivio di backup.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-113">The provider determines whether the requested name exists in its backing store.</span></span>  <span data-ttu-id="9ba2b-114">Il provider deve usare **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** come routine di confronto durante la ricerca nell'archivio di backup per determinare se il nome richiesto esiste nell'archivio di backup.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-114">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** as the comparison routine when searching its backing store to determine whether the requested name exists in the backing store.</span></span>  <span data-ttu-id="9ba2b-115">In caso contrario, il provider restituisce HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND) dal callback.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-115">If it does not, the provider returns HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) from the callback.</span></span>

1. <span data-ttu-id="9ba2b-116">Se il nome richiesto esiste nell'archivio di backup, il provider popola una struttura di [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) con i metadati file System dell'elemento e chiama **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** per inviare i dati a ProjFS.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-116">If the requested name does exist in the backing store, the provider populates a [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) structure with the item's file system metadata and calls **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to send the data to ProjFS.</span></span>  <span data-ttu-id="9ba2b-117">ProjFS utilizzerà tali informazioni per creare un segnaposto nella file system locale per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-117">ProjFS will use that information to create a placeholder in the local file system for the item.</span></span>

    > <span data-ttu-id="9ba2b-118">ProjFS utilizzerà qualsiasi FILE_ATTRIBUTE flag che il provider imposta nel membro **FileBasicInfo. FileAttributes** di PRJ_PLACEHOLDER_INFO ad eccezione di FILE_ATTRIBUTE_DIRECTORY; il valore corretto per FILE_ATTRIBUTE_DIRECTORY nel membro **FileBasicInfo. FileAttributes** verrà impostato in base al valore fornito del membro **FileBasicInfo. directory** .</span><span class="sxs-lookup"><span data-stu-id="9ba2b-118">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileBasicInfo.FileAttributes** member of PRJ_PLACEHOLDER_INFO except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileBasicInfo.FileAttributes** member according to the supplied value of the **FileBasicInfo.IsDirectory** member.</span></span>

    > <span data-ttu-id="9ba2b-119">Se l'archivio di backup supporta i collegamenti simbolici, il provider deve usare **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** per inviare i dati segnaposto a ProjFS.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-119">If the backing store supports symbolic links, the provider must use **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** to send the placeholder data to ProjFS.</span></span>  <span data-ttu-id="9ba2b-120">**PrjWritePlaceholderInfo2** supporta un input del buffer aggiuntivo che consente al provider di specificare che il segnaposto è un collegamento simbolico e la relativa destinazione.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-120">**PrjWritePlaceholderInfo2** supports an extra buffer input that allows the provider to specify that the placeholder is a symbolic link and what its target is.</span></span>  <span data-ttu-id="9ba2b-121">In caso contrario, si comporta come descritto in precedenza per **PrjWritePlaceholderInfo**.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-121">It otherwise behaves as described above for **PrjWritePlaceholderInfo**.</span></span>  <span data-ttu-id="9ba2b-122">Nell'esempio seguente viene illustrato come utilizzare **PrjWritePlaceholderInfo2** per fornire supporto per i collegamenti simbolici.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-122">The following sample illustrates how to use **PrjWritePlaceholderInfo2** to provide support for symbolic links.</span></span>
    >
    > <span data-ttu-id="9ba2b-123">Si noti che **PrjWritePlaceholderInfo2** è supportato a partire da Windows 10, versione 2004.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-123">Note that **PrjWritePlaceholderInfo2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="9ba2b-124">Un provider deve verificare l'esistenza di **PrjWritePlaceholderInfo2**, ad esempio usando **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-124">A provider should probe for the existence of **PrjWritePlaceholderInfo2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

```C++
HRESULT
MyGetPlaceholderInfoCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
    )
{
    // MyGetItemInfo is a routine the provider might implement to get
    // information from its backing store for a given file path.  The first
    // parameter is an _In_ parameter that supplies the name to look for.
    // If the item exists the routine provides the file information in the
    // remaining parameters, all of which are annotated _Out_:
    // * 2nd parameter: the name as it appears in the backing store
    // * 3rd-9th parameters: basic file info
    // * 10th parameter: if the item is a symbolic link, a pointer to a 
    //   NULL-terminated string identifying the link's target
    //
    // Note that the routine returns the name that is in the backing
    // store.  This is because the input file path may not be in the same
    // case as what is in the backing store.  The provider should create
    // the placeholder with the name it has in the backing store.
    //
    // Note also that this example does not provide anything beyond basic
    // file information and a possible symbolic link target.
    HRESULT hr;
    WCHAR* backingStoreName = NULL;
    WCHAR* symlinkTarget = NULL;
    PRJ_PLACEHOLDER_INFO placeholderInfo = {};
    hr = MyGetItemInfo(callbackData->FilePathName,
                       &backingStoreName,
                       &placeholderInfo.FileBasicInfo.IsDirectory,
                       &placeholderInfo.FileBasicInfo.FileSize,
                       &placeholderInfo.FileBasicInfo.CreationTime,
                       &placeholderInfo.FileBasicInfo.LastAccessTime,
                       &placeholderInfo.FileBasicInfo.LastWriteTime,
                       &placeholderInfo.FileBasicInfo.ChangeTime,
                       &placeholderInfo.FileBasicInfo.FileAttributes,
                       &symlinkTarget);

    if (FAILED(hr))
    {
        // If callbackData->FilePathName doesn't exist in our backing store then
        // MyGetItemInfo should HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND).
        // If this is some other error, e.g. E_OUTOFMEMORY because MyGetItemInfo
        // couldn't allocate space for backingStoreName, we return that.
        return hr;
    }

    // If the file path is for a symbolic link, pass that in with the placeholder info.
    if (symlinkTarget != NULL)
    {
        PRJ_EXTENDED_INFO extraInfo = {};

        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
        extraInfo.Symlink.TargetName = symlinkTarget;

        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo2(callbackData->NamespaceVirtualizationContext,
                                      backingStoreName,
                                      &placeholderInfo,
                                      sizeof(placeholderInfo),
                                      &extraInfo);
    }
    else
    {
        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo(callbackData->NamespaceVirtualizationContext,
                                     backingStoreName,
                                     &placeholderInfo,
                                     sizeof(placeholderInfo));
    }

    free(backingStoreName);

    if (symlinkTarget != NULL)
    {
        free(symlinkTarget);
    }

    return hr;
}
```

## <a name="providing-file-contents"></a><span data-ttu-id="9ba2b-125">Fornire il contenuto del file</span><span class="sxs-lookup"><span data-stu-id="9ba2b-125">Providing File Contents</span></span>

<span data-ttu-id="9ba2b-126">Quando ProjFS deve garantire che un file virtualizzato includa dati, ad esempio quando un'applicazione tenta di leggere dal file, ProjFS chiama il callback **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** per tale elemento per richiedere che il provider fornisca il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-126">When ProjFS needs to ensure that a virtualized file contains data, such as when an application attempts to read from the file, ProjFS calls the **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback for that item to request that the provider supply the file's contents.</span></span>  <span data-ttu-id="9ba2b-127">Il provider recupera i dati del file dal relativo archivio di backup e USA **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** per inviare i dati al file system locale.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-127">The provider retrieves the file's data from its backing store and uses **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** to send the data to the local file system.</span></span>

> <span data-ttu-id="9ba2b-128">Quando ProjFS chiama questo callback, il membro **FilePathName** del parametro _callBackData_ fornisce il nome del file al momento della creazione del segnaposto.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-128">When ProjFS calls this callback, the **FilePathName** member of the _callbackData_ parameter supplies the name the file had when its placeholder was created.</span></span>  <span data-ttu-id="9ba2b-129">Ovvero, se il file è stato rinominato dopo la creazione del segnaposto, il callback fornisce il nome originale (pre-Rinomina), non il nome corrente (post-Rinomina).</span><span class="sxs-lookup"><span data-stu-id="9ba2b-129">That is, if the file has been renamed since its placeholder was created, the callback supplies the original (pre-rename) name, not the current (post-rename) name.</span></span>  <span data-ttu-id="9ba2b-130">Se necessario, il provider può usare il membro **VERSIONINFO** del parametro _callBackData_ per determinare quali dati del file vengono richiesti.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-130">If necessary, the provider can use the **VersionInfo** member of the _callbackData_ parameter to determine which file's data is being requested.</span></span>
>
> <span data-ttu-id="9ba2b-131">Per ulteriori informazioni sulla modalità di utilizzo del membro **VERSIONINFO** di PRJ_CALLBACK_DATA, vedere la documentazione per [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) e l'argomento relativo alle modifiche della [vista di gestione](handling-view-changes.md) .</span><span class="sxs-lookup"><span data-stu-id="9ba2b-131">For more information on how the **VersionInfo** member of PRJ_CALLBACK_DATA may be used, see the documentation for [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) and the [Handling View Changes](handling-view-changes.md) topic.</span></span>

<span data-ttu-id="9ba2b-132">Il provider può suddividere l'intervallo di dati richiesti nella **PRJ_GET_FILE_DATA_CB** callback in più chiamate a **PrjWriteFileData**, ognuna delle quali fornisce una parte dell'intervallo richiesto.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-132">The provider is allowed to split the range of data requested in the **PRJ_GET_FILE_DATA_CB** callback into multiple calls to **PrjWriteFileData**, each supplying a portion of the requested range.</span></span>  <span data-ttu-id="9ba2b-133">Tuttavia, il provider deve fornire l'intero intervallo richiesto prima di completare il callback.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-133">However, the provider must supply the entire requested range before completing the callback.</span></span>  <span data-ttu-id="9ba2b-134">Se, ad esempio, il callback richiede 10 MB di dati da _byteOffset_ 0 per la _lunghezza_ 10.485.760, il provider può scegliere di fornire i dati in 10 chiamate a **PrjWriteFileData**, ognuno dei quali Invia 1 MB.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-134">For example, if the callback requests 10 MB of data from _byteOffset_ 0 for _length_ 10,485,760, the provider may choose to supply the data in 10 calls to **PrjWriteFileData**, each sending 1 MB.</span></span>

<span data-ttu-id="9ba2b-135">Il provider è anche libero di fornire un numero di intervalli superiore a quello richiesto, fino alla lunghezza del file.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-135">The provider is also free to supply more than the requested range, up to the length of the file.</span></span>  <span data-ttu-id="9ba2b-136">L'intervallo fornito dal provider deve coprire l'intervallo richiesto.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-136">The range the provider supplies must cover the requested range.</span></span>  <span data-ttu-id="9ba2b-137">Se, ad esempio, il callback richiede 1 MB di dati da _byteOffset_ 4096 per la _lunghezza_ 1.052.672 e il file ha una dimensione totale di 10 MB, il provider può scegliere di restituire 2 MB di dati a partire dall'offset 0.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-137">For example, if the callback requests 1 MB of data from _byteOffset_ 4096 for _length_ 1,052,672, and the file has a total size of 10 MB, the provider could choose to return 2 MB of data starting at offset 0.</span></span>

### <a name="buffer-alignment-considerations"></a><span data-ttu-id="9ba2b-138">Considerazioni sull'allineamento del buffer</span><span class="sxs-lookup"><span data-stu-id="9ba2b-138">Buffer Alignment Considerations</span></span>

<span data-ttu-id="9ba2b-139">ProjFS usa il [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) dal chiamante che richiede che i dati scrivano i dati nel file system locale.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-139">ProjFS uses the [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) from the caller who requires the data to write the data to the local file system.</span></span>  <span data-ttu-id="9ba2b-140">Tuttavia, ProjFS non è in grado di controllare se la FILE_OBJECT è stata aperta per l'I/O memorizzato nel buffer o non memorizzato nel buffer.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-140">However ProjFS cannot control whether that FILE_OBJECT was opened for buffered or unbuffered I/O.</span></span>  <span data-ttu-id="9ba2b-141">Se il FILE_OBJECT è stato aperto per le operazioni di I/O senza buffer, le letture e le scritture nel file devono rispettare determinati requisiti di allineamento.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-141">If the FILE_OBJECT was opened for unbuffered I/O, reads and writes to the file must adhere to certain alignment requirements.</span></span>  <span data-ttu-id="9ba2b-142">Il provider può soddisfare i requisiti di allineamento eseguendo due operazioni:</span><span class="sxs-lookup"><span data-stu-id="9ba2b-142">The provider can meet those alignment requirements by doing two things:</span></span>

1. <span data-ttu-id="9ba2b-143">Usare **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** per allocare il buffer da passare nel parametro di _buffer_ di **PrjWriteFileData**.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-143">Use **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** to allocate the buffer to pass in **PrjWriteFileData**'s _buffer_ parameter.</span></span>
1. <span data-ttu-id="9ba2b-144">Verificare che i parametri _byteOffset_ e _length_ di **PrjWriteFileData** siano multipli integer del requisito di allineamento del dispositivo di archiviazione (si noti che il parametro _length_ non deve soddisfare questo requisito se la   +  _lunghezza_ di byteOffset è uguale alla fine del file).</span><span class="sxs-lookup"><span data-stu-id="9ba2b-144">Ensure that the _byteOffset_ and _length_ parameters of **PrjWriteFileData** are integer multiples of the storage device's alignment requirement (note that the _length_ parameter does not have to meet this requirement if _byteOffset_ + _length_ is equal to the end of the file).</span></span>  <span data-ttu-id="9ba2b-145">Il provider può usare **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** per recuperare il requisito di allineamento del dispositivo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-145">The provider can use **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** to retrieve the storage device's alignment requirement.</span></span>

<span data-ttu-id="9ba2b-146">ProjFS lascia al provider il calcolo dell'allineamento appropriato.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-146">ProjFS leaves it up to the provider to calculate proper alignment.</span></span>  <span data-ttu-id="9ba2b-147">Questo perché quando si elabora un callback **PRJ_GET_FILE_DATA_CB** il provider può scegliere di restituire i dati richiesti tra più chiamate **PrjWriteFileData** , ognuna delle quali restituisce parte del totale dei dati richiesti, prima di completare il callback.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-147">This is because when processing a **PRJ_GET_FILE_DATA_CB** callback the provider may opt to return the requested data across multiple **PrjWriteFileData** calls, each returning part of the total requested data, before completing the callback.</span></span>

> <span data-ttu-id="9ba2b-148">Se il provider userà una singola chiamata a **PrjWriteFileData** per scrivere l'intero file, ad esempio da _byteOffset_ = 0 a _length_ = size del file o per restituire l'intervallo esatto richiesto nel callback **PRJ_GET_FILE_DATA_CB** , il provider non deve eseguire alcun calcolo di allineamento.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-148">If the provider is going to use a single call to **PrjWriteFileData** to either write the entire file, i.e. from _byteOffset_ = 0 to _length_ = size of the file, or to return the exact range requested in the **PRJ_GET_FILE_DATA_CB** callback, the provider does not have to do any alignment calculations.</span></span>  <span data-ttu-id="9ba2b-149">Tuttavia, deve comunque usare **PrjAllocateAlignedBuffer** per garantire che il _buffer_ soddisfi i requisiti di allineamento del dispositivo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9ba2b-149">However, it must still use **PrjAllocateAlignedBuffer** to ensure that _buffer_ meets the storage device’s alignment requirements.</span></span>

<span data-ttu-id="9ba2b-150">Per ulteriori informazioni sull'I/O memorizzato nel buffer e non memorizzato nel buffer, vedere l'argomento [buffering dei file](/windows/desktop/FileIO/file-buffering) .</span><span class="sxs-lookup"><span data-stu-id="9ba2b-150">See the topic [File Buffering](/windows/desktop/FileIO/file-buffering) for more information on buffered vs. unbuffered I/O.</span></span>

```C++
//  BlockAlignTruncate(): Aligns P on the previous V boundary (V must be != 0).
#define BlockAlignTruncate(P,V) ((P) & (0-((UINT64)(V))))

// This sample illustrates both returning the entire requested range in a
// single call to PrjWriteFileData(), and splitting it up into smaller 
// units.  Note that the provider must return all the requested data before
// completing the PRJ_GET_FILE_DATA_CB callback with S_OK.
HRESULT
MyGetFileDataCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ UINT64 byteOffset,
    _In_ UINT32 length
    )
{
    HRESULT hr;

    // For the purposes of this sample our provider has a 1 MB limit to how
    // much data it can return at once (perhaps its backing store imposes such
    // a limit).
    UINT64 writeStartOffset;
    UINT32 writeLength;
    if (length <= 1024*1024)
    {
        // The range requested in the callback is less than 1MB, so we can return
        // the data in a single call, without doing any alignment calculations.
        writeStartOffset = byteOffset;
        writeLength = length;
    }
    else
    {
        // The range requested is more than 1MB.  Retrieve the device alignment
        // and calculate a transfer size that conforms to the device alignment and
        // is <= 1MB.
        PRJ_VIRTUALIZATION_INSTANCE_INFO instanceInfo;
        UINT32 infoSize = sizeof(instanceInfo);
        hr = PrjGetVirtualizationInstanceInfo(callbackData->NamespaceVirtualizationContext,
                                              &infoSize,
                                              &instanceInfo);

        if (FAILED(hr))
        {
            return hr;
        }

        // The first transfer will start at the beginning of the requested range,
        // which is guaranteed to have the correct alignment.
        writeStartOffset = byteOffset;

        // Ensure our transfer size is aligned to the device alignment, and is
        // no larger than 1 MB (note this assumes the device alignment is less
        // than 1 MB).
        UINT64 writeEndOffset = BlockAlignTruncate(writeStartOffset + 1024*1024,
                                                   instanceInfo->WriteAlignment);
        assert(writeEndOffset > 0);
        assert(writeEndOffset > writeStartOffset);

        writeLength = writeEndOffset - writeStartOffset;
    }

    // Allocate a buffer that adheres to the needed memory alignment.
    void* writeBuffer = NULL;
    writeBuffer = PrjAllocateAlignedBuffer(callbackData->NamespaceVirtualizationContext,
                                           writeLength);

    if (writeBuffer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    do
    {
        // MyGetFileDataFromStore is a routine the provider might implement to copy
        // data for the specified file from the provider's backing store to a
        // buffer.  The routine finds the file located at callbackData->FilePathName
        // and copies writeLength bytes of its data, starting at writeStartOffset,
        // to the buffer pointed to by writeBuffer.
        hr = MyGetFileDataFromStore(callbackData->FilePathName,
                                    writeStartOffset,
                                    writeLength,
                                    writeBuffer);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // Write the data to the file in the local file system.
        hr = PrjWriteFileData(callbackData->NamespaceVirtualizationContext,
                              callbackData->DataStreamId,
                              writeBuffer,
                              writeStartOffset,
                              writeLength);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // The length parameter to the callback is guaranteed to be either
        // correctly aligned or to result in a write to the end of the file.
        length -= writeLength;
        if (length < writeLength)
        {
            writeLength = length;
        }
    }
    while (writeLength > 0);

    PrjFreeAlignedBuffer(writeBuffer);
    return hr;
}
```