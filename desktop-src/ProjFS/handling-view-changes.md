---
title: Gestione delle modifiche della visualizzazione
description: Viene descritto come aggiornare la visualizzazione client dell'archivio di backup di un provider.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 99ace7849b8967748f26210d9d6b770e424c349359aa39e828c8ad9af36a65af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792648"
---
# <a name="handling-view-changes"></a>Gestione delle modifiche della visualizzazione

Quando vengono aperti file e directory nella radice di virtualizzazione, il provider crea segnaposto su disco e, durante la lettura dei file, i segnaposto vengono idratati con il contenuto.  Questi segnaposto rappresentano lo stato dell'archivio di backup al momento della creazione.  Questi elementi memorizzati nella cache, combinati con gli elementi proiettati dal provider nelle enumerazioni, costituiscono la "visualizzazione" del client dell'archivio di backup.  Di tanto in tanto il provider può voler aggiornare la visualizzazione del client, a causa di modifiche nell'archivio di backup o a causa di un'azione esplicita eseguita dall'utente per modificare la visualizzazione.

> Se il provider aggiorna la visualizzazione in modo proattivo, con le modifiche apportate all'archivio di backup, è consigliabile che le modifiche apportate alla visualizzazione siano relativamente poco frequenti.  Ciò è dovuto al fatto che una modifica della visualizzazione a un elemento che è stato aperto e che quindi ha creato un segnaposto su disco richiede che l'elemento su disco sia aggiornato o eliminato per riflettere la modifica della visualizzazione.  Gli aggiornamenti frequenti possono comportare un'attività aggiuntiva del disco che può influire negativamente sulle prestazioni del sistema.

## <a name="item-versioning"></a>Controllo delle versioni degli elementi

Per supportare la gestione di più viste, ProjFS fornisce **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.  Un provider usa questo struct autonomo nelle chiamate **[a PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** ed è incorporato negli struct PRJ_PLACEHOLDER_INFO e **[PRJ_CALLBACK_DATA.](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** **[](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)**  Oggetto **PRJ_PLACEHOLDER_VERSION_INFO**. Il campo ContentID è il punto in cui il provider archivia fino a 128 byte di informazioni sulla versione per un file o una directory.  Il provider può quindi associare internamente questo valore a un valore che identifica una vista specifica.

Ad esempio, un provider che virtualizza un repository del controllo del codice sorgente potrebbe scegliere di usare un hash del contenuto di un file da usare come ContentID e potrebbe usare i timestamp per identificare le visualizzazioni del repository in vari punti nel tempo.  I timestamp potrebbero essere le ore in cui è stato eseguito il commit nel repository.

Usando l'esempio di un repository con timestamp indicizzato, un flusso tipico per l'uso di ContentID di un elemento potrebbe essere:

1. Il client stabilisce una vista specificando il timestamp in corrispondenza del quale presentare il contenuto del repository.  Questa operazione viene eseguita tramite un'interfaccia implementata dal provider, non tramite un'API ProjFS.  Ad esempio, il provider può avere uno strumento da riga di comando che può essere usato per indicare al provider quale visualizzazione desidera l'utente.
1. Quando il client crea un handle per un file o una directory virtualizzata, il provider crea un segnaposto per esso, usando file system metadati dall'archivio sottostante.  Il particolare set di metadati che usa è identificato dal valore ContentID associato al timestamp della visualizzazione desiderata.  Quando il provider chiama **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** per scrivere le informazioni segnaposto, specifica ContentID nel membro VersionInfo _dell'argomento placeholderInfo._  Il provider deve quindi registrare che in questa visualizzazione è stato creato un segnaposto per il file o la directory.
1. Quando il client legge da un segnaposto, viene richiamato il **[callback](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** PRJ_GET_FILE_DATA_CB del provider.  Il _membro VersionInfo_ del parametro callbackData contiene il ContentID del provider specificato in **PrjWritePlaceholderInfo** al momento della creazione del segnaposto del file.  Il provider usa tale ContentID per recuperare il contenuto corretto del file dal relativo archivio di backup.
1. Il client richiede una modifica della visualizzazione specificando un nuovo timestamp.  Per ogni segnaposto creato nella visualizzazione precedente, se nella nuova vista è presente una versione diversa del file, il provider può sostituire il segnaposto su disco con uno aggiornato il cui ContentID è associato al nuovo timestamp chiamando **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.  In alternativa, il provider può eliminare il segnaposto chiamando **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** in modo che la nuova visualizzazione del file venga proiettata nelle enumerazioni.  Se il file non esiste nella nuova visualizzazione, il provider deve eliminarlo chiamando **PrjDeleteFile**.

Si noti che il provider deve assicurarsi che quando il client enumera una directory, il provider fornirà il contenuto corrispondente alla visualizzazione del client.  Ad esempio, il provider può usare il membro VersionInfo del parametro _callbackData_ dei callback **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** **[e PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** per recuperare il contenuto della directory in tempo reale.  In alternativa, può compilare una struttura di directory per tale vista nell'archivio sottostante come parte della definizione della vista e quindi semplicemente enumerare tale struttura.

> Ogni volta che viene richiamato un callback del provider per un segnaposto o un file parziale, le informazioni sulla versione specificate dal provider durante la creazione dell'elemento vengono fornite nel membro VersionInfo del parametro _callbackData del_ callback.

## <a name="updating-the-view"></a>Aggiornamento della vista

Di seguito è riportata una funzione di esempio che illustra come un provider potrebbe aggiornare la visualizzazione locale quando l'utente specifica un nuovo timestamp.  La funzione recupera un elenco dei segnaposto creati dal provider per la vista da cui l'utente ha appena modificato e aggiorna lo stato della cache locale in base allo stato di ogni segnaposto nella nuova vista.  Per maggiore chiarezza, questa routine omette determinate complessità di gestione delle file system.  Nella visualizzazione precedente, ad esempio, una determinata directory potrebbe essere presente con alcuni file o directory, ma nella nuova visualizzazione tale directory (e il relativo contenuto) potrebbe non esistere più.  Per evitare che si verifichino errori in una situazione di questo tipo, il provider deve aggiornare lo stato del file e delle directory sotto la radice di virtualizzazione in modo approfondito.

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