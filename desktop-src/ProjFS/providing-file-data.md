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
# <a name="providing-file-data"></a>Fornire dati di file

Quando un provider crea innanzitutto una radice di virtualizzazione, è vuota nel sistema locale. Ovvero, nessuno degli elementi nell'archivio dati di supporto è ancora stato memorizzato nella cache su disco. Quando gli elementi vengono aperti, ProjFS richiede informazioni dal provider per consentire la creazione di segnaposto per tali elementi nel file system locale.  Quando si accede al contenuto dell'elemento, ProjFS richiede il contenuto del provider.  Il risultato è che dal punto di vista dell'utente, i file e le directory virtualizzate appaiono simili ai file e alle directory normali che si trovano già nella file system locale.

## <a name="placeholder-creation"></a>Creazione di segnaposto

Quando un'applicazione tenta di aprire un handle per un file virtualizzato, ProjFS chiama il callback **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** per ogni elemento del percorso che non esiste ancora sul disco.  Se, ad esempio, un'applicazione tenta di aprire `C:\virtRoot\dir1\dir2\file.txt` , ma solo il percorso `C:\virtRoot\dir1` esiste sul disco, il provider riceverà un callback per `C:\virtRoot\dir1\dir2` , quindi per `C:\virtRoot\dir1\dir2\file.txt` .

Quando ProjFS chiama il callback **PRJ_GET_PLACEHOLDER_INFO_CB** del provider, il provider esegue le azioni seguenti:

1. Il provider determina se il nome richiesto esiste nell'archivio di backup.  Il provider deve usare **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** come routine di confronto durante la ricerca nell'archivio di backup per determinare se il nome richiesto esiste nell'archivio di backup.  In caso contrario, il provider restituisce HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND) dal callback.

1. Se il nome richiesto esiste nell'archivio di backup, il provider popola una struttura di [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) con i metadati file System dell'elemento e chiama **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** per inviare i dati a ProjFS.  ProjFS utilizzerà tali informazioni per creare un segnaposto nella file system locale per l'elemento.

    > ProjFS utilizzerà qualsiasi FILE_ATTRIBUTE flag che il provider imposta nel membro **FileBasicInfo. FileAttributes** di PRJ_PLACEHOLDER_INFO ad eccezione di FILE_ATTRIBUTE_DIRECTORY; il valore corretto per FILE_ATTRIBUTE_DIRECTORY nel membro **FileBasicInfo. FileAttributes** verrà impostato in base al valore fornito del membro **FileBasicInfo. directory** .

    > Se l'archivio di backup supporta i collegamenti simbolici, il provider deve usare **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** per inviare i dati segnaposto a ProjFS.  **PrjWritePlaceholderInfo2** supporta un input del buffer aggiuntivo che consente al provider di specificare che il segnaposto è un collegamento simbolico e la relativa destinazione.  In caso contrario, si comporta come descritto in precedenza per **PrjWritePlaceholderInfo**.  Nell'esempio seguente viene illustrato come utilizzare **PrjWritePlaceholderInfo2** per fornire supporto per i collegamenti simbolici.
    >
    > Si noti che **PrjWritePlaceholderInfo2** è supportato a partire da Windows 10, versione 2004.  Un provider deve verificare l'esistenza di **PrjWritePlaceholderInfo2**, ad esempio usando **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

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

## <a name="providing-file-contents"></a>Fornire il contenuto del file

Quando ProjFS deve garantire che un file virtualizzato includa dati, ad esempio quando un'applicazione tenta di leggere dal file, ProjFS chiama il callback **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** per tale elemento per richiedere che il provider fornisca il contenuto del file.  Il provider recupera i dati del file dal relativo archivio di backup e USA **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** per inviare i dati al file system locale.

> Quando ProjFS chiama questo callback, il membro **FilePathName** del parametro _callBackData_ fornisce il nome del file al momento della creazione del segnaposto.  Ovvero, se il file è stato rinominato dopo la creazione del segnaposto, il callback fornisce il nome originale (pre-Rinomina), non il nome corrente (post-Rinomina).  Se necessario, il provider può usare il membro **VERSIONINFO** del parametro _callBackData_ per determinare quali dati del file vengono richiesti.
>
> Per ulteriori informazioni sulla modalità di utilizzo del membro **VERSIONINFO** di PRJ_CALLBACK_DATA, vedere la documentazione per [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) e l'argomento relativo alle modifiche della [vista di gestione](handling-view-changes.md) .

Il provider può suddividere l'intervallo di dati richiesti nella **PRJ_GET_FILE_DATA_CB** callback in più chiamate a **PrjWriteFileData**, ognuna delle quali fornisce una parte dell'intervallo richiesto.  Tuttavia, il provider deve fornire l'intero intervallo richiesto prima di completare il callback.  Se, ad esempio, il callback richiede 10 MB di dati da _byteOffset_ 0 per la _lunghezza_ 10.485.760, il provider può scegliere di fornire i dati in 10 chiamate a **PrjWriteFileData**, ognuno dei quali Invia 1 MB.

Il provider è anche libero di fornire un numero di intervalli superiore a quello richiesto, fino alla lunghezza del file.  L'intervallo fornito dal provider deve coprire l'intervallo richiesto.  Se, ad esempio, il callback richiede 1 MB di dati da _byteOffset_ 4096 per la _lunghezza_ 1.052.672 e il file ha una dimensione totale di 10 MB, il provider può scegliere di restituire 2 MB di dati a partire dall'offset 0.

### <a name="buffer-alignment-considerations"></a>Considerazioni sull'allineamento del buffer

ProjFS usa il [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) dal chiamante che richiede che i dati scrivano i dati nel file system locale.  Tuttavia, ProjFS non è in grado di controllare se la FILE_OBJECT è stata aperta per l'I/O memorizzato nel buffer o non memorizzato nel buffer.  Se il FILE_OBJECT è stato aperto per le operazioni di I/O senza buffer, le letture e le scritture nel file devono rispettare determinati requisiti di allineamento.  Il provider può soddisfare i requisiti di allineamento eseguendo due operazioni:

1. Usare **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** per allocare il buffer da passare nel parametro di _buffer_ di **PrjWriteFileData**.
1. Verificare che i parametri _byteOffset_ e _length_ di **PrjWriteFileData** siano multipli integer del requisito di allineamento del dispositivo di archiviazione (si noti che il parametro _length_ non deve soddisfare questo requisito se la   +  _lunghezza_ di byteOffset è uguale alla fine del file).  Il provider può usare **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** per recuperare il requisito di allineamento del dispositivo di archiviazione.

ProjFS lascia al provider il calcolo dell'allineamento appropriato.  Questo perché quando si elabora un callback **PRJ_GET_FILE_DATA_CB** il provider può scegliere di restituire i dati richiesti tra più chiamate **PrjWriteFileData** , ognuna delle quali restituisce parte del totale dei dati richiesti, prima di completare il callback.

> Se il provider userà una singola chiamata a **PrjWriteFileData** per scrivere l'intero file, ad esempio da _byteOffset_ = 0 a _length_ = size del file o per restituire l'intervallo esatto richiesto nel callback **PRJ_GET_FILE_DATA_CB** , il provider non deve eseguire alcun calcolo di allineamento.  Tuttavia, deve comunque usare **PrjAllocateAlignedBuffer** per garantire che il _buffer_ soddisfi i requisiti di allineamento del dispositivo di archiviazione.

Per ulteriori informazioni sull'I/O memorizzato nel buffer e non memorizzato nel buffer, vedere l'argomento [buffering dei file](/windows/desktop/FileIO/file-buffering) .

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