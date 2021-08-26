---
title: Notifiche delle operazioni del file system
description: Viene descritto in che modo un provider può ricevere notifiche file system operazioni.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 2e09efcc9d1a1aea99f79b70446162df5e3ef924067ac6619a443aa15e06e9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031241"
---
# <a name="file-system-operation-notifications"></a>Notifiche delle operazioni del file system

Oltre ai callback necessari per la gestione dell'enumerazione, la restituzione di metadati di file e il contenuto del file, un provider può facoltativamente registrare un callback **[PRJ_NOTIFICATION_CB]()** nella chiamata a **[PrjStartVirtualizing.]()**  Questo callback riceve le notifiche delle file system eseguite su file e directory sotto la radice di virtualizzazione dell'istanza.  Alcune notifiche sono di tipo "post-operazione", che indica al provider che un'operazione è stata appena completata.  Le altre notifiche sono notifiche di "pre-operazione", vale a dire che il provider viene informato prima dell'esecuzione dell'operazione.  In una notifica di pre-operazione il provider può veto all'operazione tramite la restituzione di un codice di errore dal callback.  In questo modo l'operazione ha esito negativo con il codice di errore restituito.

## <a name="how-to-specify-notifications-to-receive"></a>Come specificare le notifiche da ricevere

Se il provider fornisce un'implementazione di **PRJ_NOTIFICATION_CB** all'avvio di un'istanza di virtualizzazione, deve anche specificare le notifiche da ricevere.  Le notifiche per cui il provider può [](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) eseguire la registrazione sono definite nell PRJ_NOTIFICATION enum .

Quando il provider specifica le notifiche che vuole ricevere, lo fa [](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) usando una matrice di una o più PRJ_NOTIFICATION_MAPPING struttura .  Questi definiscono "mapping di notifica".  Un mapping di notifica è un'associazione tra una directory, definita "radice di notifica" e un set di notifiche, espresse come maschera di bit, che ProjFS deve inviare per tale directory e i relativi discendenti.  È anche possibile stabilire un mapping di notifica per un singolo file.  Non è necessario che un file o una directory specificata in un mapping di notifica esista già nel momento in cui il provider chiama **PrjStartVirtualizing,** il provider può specificare qualsiasi percorso e il mapping verrà applicato se viene creato.

Se il provider specifica più mapping di notifica e alcuni sono discendenti di altri, i mapping devono essere specificati in profondità decrescente.  I mapping delle notifiche a livelli più approfonditi eseguono l'override di quelli di livello superiore per i relativi discendenti.

Se il provider non specifica un set di mapping di notifica, ProjFS lo invierà per impostazione predefinita PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED e PRJ_NOTIFY_FILE_OVERWRITTEN per tutti i file e le directory sotto la radice di virtualizzazione.

Il frammento di codice seguente illustra come registrare un set di notifiche all'avvio di un'istanza di virtualizzazione.

```C++
PRJ_CALLBACKS callbackTable;

// Supply required callbacks.
callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
callbackTable.GetFileDataCallback = MyGetFileDataCallback;

// The rest of the callbacks are optional.  We want notifications, so specify
// our notification callback.
callbackTable.QueryFileNameCallback = nullptr;
callbackTable.NotificationCallback = MyNotificationCallback;
callbackTable.CancelCommandCallback = nullptr;

// Assume the provider has created a new virtualization root at C:\VirtRoot and
// initialized it with this layout:
//
//     C:\VirtRoot
//     +--- baz
//     \--- foo
//          +--- subdir1
//          \--- subdir2
//
// The provider wants these notifications:
// * Notification of new file/directory creates for all locations within the
//   virtualization root that are not subject to one of the following more
//   specific notification mappings.
// * Notification of new file/directory creates, file opens, post-renames, and
//   pre- and post-deletes for C:\VirtRoot\foo
// * No notifications for C:\VirtRoot\foo\subdir1
PRJ_STARTVIRTUALIZING_OPTIONS startOpts = {};
PRJ_VIRTUALIZATION_MAPPING notificationMappings[3];

// Configure default notifications - notify of new files for most of the tree.
notificationMappings[0].NotificationRoot = L"";
notificationMappings[0].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED;

// Override default notifications - notify of new files, opened files, and file
// deletes for C:\VirtRoot\foo and its descendants.
notificationMappings[1].NotificationRoot = L"foo";
notificationMappings[1].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED |
                                              PRJ_NOTIFY_FILE_OPENED |
                                              PRJ_NOTIFY_PRE_DELETE |
                                              PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED |
                                              PRJ_NOTIFY_FILE_RENAMED;

// Override all notifications for C:\VirtRoot\foo\subdir1 and its descendants.
notificationMappings[2].NotificationRoot = L"foo\\subdir1";
notificationMappings[2].NotificationBitMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;

startOpts.NotificationMappings = notificationMappings;
startOpts.NotificationMappingsCount = ARRAYSIZE(notificationMapping);

// Start the instance and provide our notification mappings.
HRESULT hr;
PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
hr = PrjStartVirtualizing(rootName,
                          &callbackTable,
                          nullptr,
                          &startOpts,
                          &instanceHandle);
if (FAILED(hr))
{
    wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
    return;
}
```

## <a name="receiving-notifications"></a>Ricezione di notifiche

ProjFS invia le notifiche file system operazioni chiamando il **callback** PRJ_NOTIFICATION_CB provider.  Questa operazione viene eseguita per ogni operazione per cui il provider è registrato.  Se, come nell'esempio precedente, il provider è registrato per PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED e un'applicazione ha creato un nuovo file nella radice della notifica, ProjFS chiama il callback **PRJ_NOTIFICATION_CB** con il nome del percorso del nuovo file e il parametro di notifica impostato su PRJ_NOTIFICATION_NEW_FILE_CREATED. 

ProjFS invia le notifiche nell'elenco seguente prima che venga eseguita file system'operazione associata.  Se il provider restituisce un codice di errore dal callback **PRJ_NOTIFICATION_CB,** l'operazione di file system avrà esito negativo e restituirà il codice di errore specificato dal provider.

* PRJ_NOTIFICATION_PRE_DELETE: il file sta per essere eliminato.
* PRJ_NOTIFICATION_PRE_RENAME: il file sta per essere rinominato.
* PRJ_NOTIFICATION_PRE_SET_HARDLINK: sta per essere creato un collegamento rigido per il file.
* PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL: un file sta per essere espanso da un segnaposto a un file completo, a indicare che è probabile che il relativo contenuto sia stato modificato.

ProjFS invia le notifiche nell'elenco seguente dopo il completamento file system'operazione associata.

* PRJ_NOTIFICATION_FILE_OPENED: è stato aperto un file esistente.
  * Anche se questa notifica viene inviata dopo l'apertura del file, il provider può restituire un codice di errore.  In risposta, ProjFS annullerà l'apertura e restituirà l'errore al chiamante.
* PRJ_NOTIFICATION_NEW_FILE_CREATED: è stato creato un nuovo file.
* PRJ_NOTIFICATION_FILE_OVERWRITTEN: un file esistente è stato sovrascritto, ad esempio chiamando [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) con **il** flag _CREATE_ALWAYS dwCreationDisposition._
* PRJ_NOTIFICATION_FILE_RENAMED: un file è stato rinominato.
* PRJ_NOTIFICATION_HARDLINK_CREATED: è [stato creato un collegamento](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) rigido per un file.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION: un handle di file è stato chiuso e il contenuto del file non è stato modificato, né è stato eliminato.
* PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED: un handle di file è stato chiuso e il contenuto del file è stato modificato.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED: un handle di file è stato chiuso e il file è stato eliminato come parte della chiusura dell'handle.

Per altri dettagli su ogni notifica, vedere la documentazione **[per PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.

Il **PRJ_NOTIFICATION_CB** _notificationParameters_ del callback specifica parametri aggiuntivi per determinate notifiche.  Se un provider riceve una notifica PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED, PRJ_NOTIFICATION_FILE_OVERWRITTEN o PRJ_NOTIFICATION_FILE_RENAMED, il provider può specificare un nuovo set di notifiche da ricevere per il file. Per altri dettagli, vedere la documentazione per **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.

L'esempio seguente illustra semplici esempi di come un provider potrebbe elaborare le notifiche per cui è stato registrato nel frammento di codice precedente.

```C++
#include <windows.h>

HRESULT
MyNotificationCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ BOOLEAN isDirectory,
    _In_ PRJ_NOTIFICATION notification,
    _In_opt_z_ PCWSTR destinationFileName,
    _Inout_ PRJ_NOTIFICATION_PARAMETERS* operationParameters
    )
{
    HRESULT hr = S_OK;

    switch (notification)
    {
    case PRJ_NOTIFY_NEW_FILE_CREATED:

        wprintf(L"A new %ls was created at [%ls].\n",
                isDirectory ? L"directory" : L"file",
                callbackData->FilePathName);

        // Let's stop getting notifications inside newly-created directories.
        if (isDirectory)
        {
            operationParameters->PostCreate.NotificationMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;
        }
        break;

    case PRJ_NOTIFY_FILE_OPENED:

        wprintf(L"Handle opened to %ls [%ls].\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_PRE_DELETE:

        wprintf(L"Attempt to delete %ls [%ls]: ",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);

        // MyAllowDelete is a routine the provider might implement to decide
        // whether to allow a given file/directory to be deleted.
        if (!MyAllowDelete(callbackData->FilePathName, isDirectory))
        {
            wprintf(L"DENIED\n");
            hr = HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED);
        }
        else
        {
            wprintf(L"ALLOWED\n");
        }
        break;

    case PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED:

        wprintf(L"The %ls [%ls] was deleted.\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_FILE_RENAMED:

        if (wcslen(callbackData->FilePathName) == 0)
        {
            // If callbackData->FilePathName is an empty string, then the item
            // that was renamed was originally in a location not under the
            // virtualization root.
            wprintf(L"A %ls was renamed into the virtualization root,\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its new location is [%ls].\n",
                    destinationFileName);
        }
        else if (wcslen(destinationFileName) == 0)
        {
            // If destinationFileName is an empty string, then the item that was
            // renamed is now in a location not under the virtualization root.
            wprintf(L"A %ls was renamed out of the virtualization root.\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its original location was [%ls].\n",
                    callbackData->FilePathName);
        }
        else
        {
            // If both names are specified, both the new and old names are under
            // the virtualization root (it is never the case that nether name is
            // specified).
            wprintf(L"A %ls [%ls] was renamed.\n",
                    isDirectory ? L"directory": L"file",
                    callbackData->FilePathName);
            wprintf(L"Its new name is [%ls].\n", destinationFileName);
        }
        break;

    default:
        wprintf(L"Unrecognized notification: 0x%08x");
    }

    // Note that this may be a failure code from MyAllowDelete().
    return hr;
}
```