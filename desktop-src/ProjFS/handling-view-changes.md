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
# <a name="handling-view-changes"></a>Gestione delle modifiche della visualizzazione

Quando si aprono i file e le directory sotto la radice di virtualizzazione, il provider crea segnaposto sul disco e, quando i file vengono letti, i segnaposto vengono idratati con il contenuto.  Questi segnaposto rappresentano lo stato dell'archivio di backup nel momento in cui sono stati creati.  Questi elementi memorizzati nella cache, combinati con gli elementi proiettati dal provider nelle enumerazioni, costituiscono la "visualizzazione" del client dell'archivio di backup.  Di tanto in tanto il provider può voler aggiornare la visualizzazione del client, sia a causa di modifiche nell'archivio di backup, sia a causa di un'azione esplicita eseguita dall'utente per modificare la visualizzazione.

> Se il provider aggiorna la visualizzazione in modo proattivo, quando viene modificato l'archivio di backup, è consigliabile che la visualizzazione delle modifiche sia relativamente poco frequente.  Ciò è dovuto al fatto che una vista è stata modificata in un elemento che è stato aperto e pertanto dispone di un segnaposto creato sul disco, richiede che l'elemento su disco venga aggiornato o eliminato per riflettere la modifica della vista.  Gli aggiornamenti frequenti possono comportare attività aggiuntive del disco che possono influire negativamente sulle prestazioni del sistema.

## <a name="item-versioning"></a>Controllo delle versioni degli elementi

Per supportare la gestione di più visualizzazioni, ProjFS fornisce lo struct **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** .  Un provider usa questo struct autonomo nelle chiamate a **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** e viene incorporato negli struct **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** e **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** .  **PRJ_PLACEHOLDER_VERSION_INFO**. Il campo ContentID è il punto in cui il provider archivia fino a 128 byte di informazioni sulla versione per un file o una directory.  Il provider può quindi associare internamente questo valore a un valore che identifica una visualizzazione specifica.

Ad esempio, un provider che virtualizza un repository del controllo del codice sorgente può scegliere di usare un hash del contenuto di un file per fungere da ContentID e potrebbe usare i timestamp per identificare le visualizzazioni del repository in diversi momenti.  I timestamp potrebbero essere i tempi di esecuzione dei commit nel repository.

Usando l'esempio di un repository con indicizzazione timestamp, un flusso tipico per l'uso di ContentID di un elemento potrebbe essere:

1. Il client stabilisce una visualizzazione specificando il timestamp in corrispondenza del quale presentare il contenuto del repository.  Questa operazione viene eseguita tramite un'interfaccia implementata dal provider, non tramite un'API ProjFS.  Ad esempio, il provider può disporre di uno strumento da riga di comando che può essere utilizzato per indicare al provider la visualizzazione desiderata.
1. Quando il client crea un handle per un file o una directory virtualizzata, il provider crea un segnaposto per tale oggetto, usando file system metadati dall'archivio di backup.  Il set specifico di metadati usato viene identificato dal valore ContentID associato al timestamp della visualizzazione desiderata.  Quando il provider chiama **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** per scrivere le informazioni sul segnaposto, fornisce ContentId nel membro VERSIONINFO dell'argomento _placeholderInfo_ .  Il provider deve quindi registrare che in questa visualizzazione è stato creato un segnaposto per il file o la directory.
1. Quando il client legge da un segnaposto, viene richiamato il callback **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** del provider.  Il membro VersionInfo del parametro _callBackData_ contiene ContentId il provider specificato in **PrjWritePlaceholderInfo** durante la creazione del segnaposto del file.  Il provider usa tale ContentID per recuperare il contenuto corretto del file dal relativo archivio di backup.
1. Il client richiede una modifica della visualizzazione specificando un nuovo timestamp.  Per ogni segnaposto creato dal provider nella visualizzazione precedente, se nella nuova visualizzazione è presente una versione diversa del file, il provider può sostituire il segnaposto sul disco con un oggetto aggiornato il cui ContentID è associato al nuovo timestamp chiamando **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.  In alternativa, il provider può eliminare il segnaposto chiamando **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** in modo che la nuova vista del file venga proiettata nelle enumerazioni.  Se il file non esiste nella nuova visualizzazione, il provider deve eliminarlo chiamando **PrjDeleteFile**.

Si noti che il provider deve garantire che, quando il client enumera una directory, il provider fornirà il contenuto che corrisponde alla visualizzazione del client.  Ad esempio, il provider può usare il membro VersionInfo del parametro _callBackData_ del **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** e **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** i callback per recuperare il contenuto della directory in tempo reale.  In alternativa, è possibile creare una struttura di directory per tale visualizzazione nell'archivio di backup come parte della definizione della vista e quindi semplicemente enumerare la struttura.

> Ogni volta che un callback del provider viene richiamato per un segnaposto o un file parziale, le informazioni sulla versione specificate dal provider durante la creazione dell'elemento vengono fornite nel membro VersionInfo del parametro _callBackData_ del callback.

## <a name="updating-the-view"></a>Aggiornamento della vista

Di seguito è riportata una funzione di esempio che illustra come un provider potrebbe aggiornare la visualizzazione locale quando l'utente specifica un nuovo timestamp.  La funzione recupera un elenco dei segnaposto creati dal provider per la visualizzazione da cui l'utente ha appena modificato e aggiorna lo stato della cache locale in base allo stato di ogni segnaposto nella nuova vista.  Per maggiore chiarezza, questa routine omette alcune complessità relative alla gestione del file system.  Nella visualizzazione precedente, ad esempio, è possibile che esista una determinata directory con alcuni file o directory, ma nella nuova visualizzazione la directory (e il relativo contenuto) potrebbe non esistere più.  Per evitare che si verifichino errori in una situazione di questo tipo, il provider deve aggiornare lo stato del file e delle directory sotto la radice di virtualizzazione in modo approfondito.

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