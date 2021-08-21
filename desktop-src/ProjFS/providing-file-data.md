---
title: Fornire dati di file
description: Descrive il modo in cui un provider fornisce informazioni segnaposto e dati di file.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 4f0da65095e908ec3211bb23be654ee9e0e2853c093bb36e8a92701c24106ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792395"
---
# <a name="providing-file-data"></a>Fornire dati di file

Quando un provider crea per la prima volta una radice di virtualizzazione è vuota nel sistema locale. Ciò significa che nessuno degli elementi nell'archivio dati di backup è ancora stato memorizzato nella cache su disco. Quando gli elementi vengono aperti, ProjFS richiede informazioni al provider per consentire la creazione di segnaposto per tali elementi nel file system.  Quando si accede al contenuto dell'elemento, ProjFS richiede tali contenuti al provider.  Il risultato è che, dal punto di vista dell'utente, i file e le directory virtualizzati sono simili ai normali file e directory che si trovano già nel file system.

## <a name="placeholder-creation"></a>Creazione di segnaposto

Quando un'applicazione tenta di aprire un handle a un file virtualizzato, ProjFS chiama il callback **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** per ogni elemento del percorso che non esiste ancora sul disco.  Ad esempio, se un'applicazione tenta di aprire , ma sul disco esiste solo il percorso , il provider riceverà un `C:\virtRoot\dir1\dir2\file.txt` callback per , quindi per `C:\virtRoot\dir1` `C:\virtRoot\dir1\dir2` `C:\virtRoot\dir1\dir2\file.txt` .

Quando ProjFS chiama il callback PRJ_GET_PLACEHOLDER_INFO_CB **provider,** il provider esegue le azioni seguenti:

1. Il provider determina se il nome richiesto esiste nell'archivio di backup.  Il provider deve usare **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** come routine di confronto durante la ricerca nell'archivio di backup per determinare se il nome richiesto esiste nell'archivio di backup.  In caso contrario, il provider restituisce HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) dal callback.

1. Se il nome richiesto esiste nell'archivio di backup, il provider popola una struttura [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) con i metadati file system dell'elemento e chiama **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** per inviare i dati a ProjFS.  ProjFS userà queste informazioni per creare un segnaposto nel file system locale per l'elemento.

    > ProjFS userà qualsiasi FILE_ATTRIBUTE contrassegna il provider impostato nel membro **FileBasicInfo.FileAttributes** di PRJ_PLACEHOLDER_INFO ad eccezione di FILE_ATTRIBUTE_DIRECTORY; verrà impostato il valore corretto per FILE_ATTRIBUTE_DIRECTORY nel membro **FileBasicInfo.FileAttributes** in base al valore fornito del **membro FileBasicInfo.IsDirectory.**

    > Se l'archivio di backup supporta i collegamenti simbolici, il provider deve usare **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** per inviare i dati segnaposto a ProjFS.  **PrjWritePlaceholderInfo2** supporta un input del buffer aggiuntivo che consente al provider di specificare che il segnaposto è un collegamento simbolico e qual è la destinazione.  In caso contrario, si comporta come descritto in precedenza **per PrjWritePlaceholderInfo.**  L'esempio seguente illustra come usare **PrjWritePlaceholderInfo2** per fornire supporto per i collegamenti simbolici.
    >
    > Si noti **che PrjWritePlaceholderInfo2** è supportato a Windows 10 versione 2004.  Un provider deve cercare l'esistenza di **PrjWritePlaceholderInfo2,** ad esempio usando **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

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

## <a name="providing-file-contents"></a>Specifica del contenuto dei file

Quando ProjFS deve garantire che un file virtualizzato contenga dati, ad esempio quando un'applicazione tenta di leggere dal file, ProjFS chiama il callback **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** per tale elemento per richiedere che il provider fornirà il contenuto del file.  Il provider recupera i dati del file dall'archivio di backup e usa **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** per inviare i dati al file system.

> Quando ProjFS chiama questo callback, il membro **FilePathName** del parametro _callbackData_ fornisce il nome del file al momento della creazione del segnaposto.  Ovvero, se il file è stato rinominato dopo la creazione del segnaposto, il callback fornisce il nome originale (pre-ridenominazione), non il nome corrente (post-ridenominazione).  Se necessario, il provider può usare il membro **VersionInfo** del parametro _callbackData_ per determinare i dati del file richiesti.
>
> Per altre informazioni sull'uso del membro **VersionInfo** di PRJ_CALLBACK_DATA, [](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) vedere la documentazione per PRJ_PLACEHOLDER_VERSION_INFO e l'argomento Gestione delle [modifiche alle visualizzazione.](handling-view-changes.md)

Il provider può suddividere l'intervallo di dati richiesto nel callback **PRJ_GET_FILE_DATA_CB in** più chiamate a **PrjWriteFileData,** ognuna delle quali fornisce una parte dell'intervallo richiesto.  Tuttavia, il provider deve fornire l'intero intervallo richiesto prima di completare il callback.  Ad esempio, se il callback richiede 10 MB  di dati da _byteOffset_ 0 per la lunghezza 10.485.760, il provider può scegliere di fornire i dati in 10 chiamate a **PrjWriteFileData**, ognuna delle quali invia 1 MB.

Il provider è anche libero di fornire più dell'intervallo richiesto, fino alla lunghezza del file.  L'intervallo fornito dal provider deve coprire l'intervallo richiesto.  Ad esempio, se il callback richiede 1 MB di dati da _byteOffset_ 4096 per la lunghezza  1.052.672 e le dimensioni totali del file sono pari a 10 MB, il provider può scegliere di restituire 2 MB di dati a partire dall'offset 0.

### <a name="buffer-alignment-considerations"></a>Considerazioni sull'allineamento del buffer

ProjFS usa il [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) dal chiamante che richiede che i dati scrivono i dati nel file system.  Tuttavia, ProjFS non può controllare se FILE_OBJECT è stato aperto per I/O memorizzato nel buffer o non memorizzato nel buffer.  Se il FILE_OBJECT è stato aperto per operazioni di I/O senza buffer, le operazioni di lettura e scrittura nel file devono rispettare determinati requisiti di allineamento.  Il provider può soddisfare questi requisiti di allineamento eseguendo due operazioni:

1. Usare **[PrjAllocateAlignedBuffer per](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** allocare il buffer da passare al parametro _buffer_ di **PrjWriteFileData.**
1. Assicurarsi che i _parametri byteOffset_ e _length_ di **PrjWriteFileData** siano multipli interi del requisito di allineamento del dispositivo di archiviazione. Si noti che il parametro _length_ non deve soddisfare questo requisito se la lunghezza di _byteOffset_ è uguale alla fine del  +   file.  Il provider può usare **[PrjGetVirtualizationInstanceInfo per](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** recuperare il requisito di allineamento del dispositivo di archiviazione.

ProjFS lascia al provider il controllo per calcolare l'allineamento corretto.  Ciò è dovuto al fatto che **durante l'elaborazione** di un callback PRJ_GET_FILE_DATA_CB il provider può scegliere di restituire i dati richiesti tra più **chiamate PrjWriteFileData,** ognuna delle quali restituisce parte dei dati totali richiesti, prima di completare il callback.

> Se il provider userà una singola chiamata a **PrjWriteFileData** per scrivere l'intero file, ad esempio da _byteOffset_ = 0 a _length_ = size del file o per restituire l'intervallo esatto richiesto nel callback **PRJ_GET_FILE_DATA_CB,** il provider non deve eseguire calcoli di allineamento.  Tuttavia, deve comunque usare **PrjAllocateAlignedBuffer** per garantire che _il buffer_ soddisfi i requisiti di allineamento del dispositivo di archiviazione.

Per altre informazioni [sull'I/O](/windows/desktop/FileIO/file-buffering) memorizzato nel buffer e non memorizzato nel buffer, vedere l'argomento Buffering dei file.

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