---
title: Notifiche delle operazioni del file System
description: Viene descritto come un provider può ricevere notifiche di file system operazioni.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 9eae9bde6d56592f371dcd48c24fef96a9eecbdf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727807"
---
# <a name="file-system-operation-notifications"></a><span data-ttu-id="48c1b-103">Notifiche delle operazioni del file System</span><span class="sxs-lookup"><span data-stu-id="48c1b-103">File System Operation Notifications</span></span>

<span data-ttu-id="48c1b-104">Oltre ai callback richiesti per la gestione dell'enumerazione, la restituzione di metadati di file e il contenuto del file, un provider può registrare facoltativamente un callback di **[PRJ_NOTIFICATION_CB]()** nella chiamata a **[PrjStartVirtualizing]()**.</span><span class="sxs-lookup"><span data-stu-id="48c1b-104">In addition to required callbacks for handling enumeration, returning file metadata, and file contents, a provider may optionally register a **[PRJ_NOTIFICATION_CB]()** callback in its call to **[PrjStartVirtualizing]()**.</span></span>  <span data-ttu-id="48c1b-105">Questo callback riceve le notifiche di file system operazioni eseguite su file e directory sotto la radice di virtualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="48c1b-105">This callback receives notifications of file system operations performed on files and directories beneath the instance's virtualization root.</span></span>  <span data-ttu-id="48c1b-106">Alcune notifiche sono notifiche "post-operazione", che indicano al provider che un'operazione è stata appena completata.</span><span class="sxs-lookup"><span data-stu-id="48c1b-106">Some of the notifications are "post-operation" notifications, which tell the provider that an operation has just completed.</span></span>  <span data-ttu-id="48c1b-107">Le altre notifiche sono notifiche di "pre-operazione", vale a dire che il provider riceve una notifica prima che l'operazione venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="48c1b-107">The other notifications are "pre-operation" notifications, meaning that the provider is notified before the operation happens.</span></span>  <span data-ttu-id="48c1b-108">In una notifica di pre-operazione il provider può porre il veto all'operazione restituendo un codice di errore dal callback.</span><span class="sxs-lookup"><span data-stu-id="48c1b-108">In a pre-operation notification the provider can veto the operation by returning an error code from the callback.</span></span>  <span data-ttu-id="48c1b-109">In questo modo l'operazione avrà esito negativo con il codice di errore restituito.</span><span class="sxs-lookup"><span data-stu-id="48c1b-109">This causes the operation to fail with the returned error code.</span></span>

## <a name="how-to-specify-notifications-to-receive"></a><span data-ttu-id="48c1b-110">Come specificare le notifiche da ricevere</span><span class="sxs-lookup"><span data-stu-id="48c1b-110">How to Specify Notifications to Receive</span></span>

<span data-ttu-id="48c1b-111">Se il provider fornisce un'implementazione di **PRJ_NOTIFICATION_CB** quando avvia un'istanza di virtualizzazione, deve specificare anche le notifiche che desidera ricevere.</span><span class="sxs-lookup"><span data-stu-id="48c1b-111">If the provider supplies an implementation of **PRJ_NOTIFICATION_CB** when it starts a virtualization instance, it should also specify which notifications it wishes to receive.</span></span>  <span data-ttu-id="48c1b-112">Le notifiche per le quali il provider è in grado di registrare sono definite nell'enumerazione [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) .</span><span class="sxs-lookup"><span data-stu-id="48c1b-112">The notifications for which the provider can register are defined in the [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) enum.</span></span>

<span data-ttu-id="48c1b-113">Quando il provider specifica le notifiche che desidera ricevere, usa una matrice di una o più strutture di [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) .</span><span class="sxs-lookup"><span data-stu-id="48c1b-113">When the provider specifies the notifications it wishes to receive, it does so using an array of one or more [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) structures.</span></span>  <span data-ttu-id="48c1b-114">Definiscono "mapping notifiche".</span><span class="sxs-lookup"><span data-stu-id="48c1b-114">These define "notification mappings".</span></span>  <span data-ttu-id="48c1b-115">Un mapping delle notifiche è un'associazione tra una directory, denominata "radice di notifica" e un set di notifiche, espresso come maschera di bit, che ProjFS deve inviare per la directory e i relativi discendenti.</span><span class="sxs-lookup"><span data-stu-id="48c1b-115">A notification mapping is a pairing between a directory, referred to as a "notification root", and a set of notifications, expressed as a bit mask, which ProjFS should send for that directory and its descendants.</span></span>  <span data-ttu-id="48c1b-116">È inoltre possibile stabilire un mapping delle notifiche per un singolo file.</span><span class="sxs-lookup"><span data-stu-id="48c1b-116">A notification mapping can also be established for a single file.</span></span>  <span data-ttu-id="48c1b-117">Un file o una directory specificata in un mapping delle notifiche non deve esistere già nel momento in cui il provider chiama **PrjStartVirtualizing**, il provider può specificare qualsiasi percorso e il mapping verrà applicato se viene creato.</span><span class="sxs-lookup"><span data-stu-id="48c1b-117">A file or directory specified in a notification mapping does not have to exist already at the time the provider calls **PrjStartVirtualizing**, the provider can specify any path and the mapping will apply to it if it is ever created.</span></span>

<span data-ttu-id="48c1b-118">Se il provider specifica più mapping di notifiche e alcuni sono discendenti di altri, i mapping devono essere specificati in profondità.</span><span class="sxs-lookup"><span data-stu-id="48c1b-118">If the provider specifies multiple notification mappings, and some are descendants of others, the mappings must be specified in descending depth.</span></span>  <span data-ttu-id="48c1b-119">I mapping delle notifiche a livelli più profondi eseguono l'override di quelli di livello superiore per i discendenti.</span><span class="sxs-lookup"><span data-stu-id="48c1b-119">Notification mappings at deeper levels override higher-level ones for their descendants.</span></span>

<span data-ttu-id="48c1b-120">Se il provider non specifica un set di mapping di notifiche, per impostazione predefinita ProjFS lo invierà PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED e PRJ_NOTIFY_FILE_OVERWRITTEN per tutti i file e le directory sotto la radice di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="48c1b-120">If the provider does not specify a set of notification mappings, ProjFS will default to sending it PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED, and PRJ_NOTIFY_FILE_OVERWRITTEN for all files and directories beneath the virtualization root.</span></span>

<span data-ttu-id="48c1b-121">Il frammento di codice seguente illustra come registrare un set di notifiche quando si avvia un'istanza di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="48c1b-121">The following code snippet illustrates how to register a set of notifications when starting a virtualization instance.</span></span>

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

## <a name="receiving-notifications"></a><span data-ttu-id="48c1b-122">Ricezione di notifiche</span><span class="sxs-lookup"><span data-stu-id="48c1b-122">Receiving Notifications</span></span>

<span data-ttu-id="48c1b-123">ProjFS Invia notifiche di file system operazioni chiamando il callback **PRJ_NOTIFICATION_CB** del provider.</span><span class="sxs-lookup"><span data-stu-id="48c1b-123">ProjFS sends notifications of file system operations by calling the provider's **PRJ_NOTIFICATION_CB** callback.</span></span>  <span data-ttu-id="48c1b-124">Questa operazione viene eseguita per ogni operazione per cui il provider ha effettuato la registrazione.</span><span class="sxs-lookup"><span data-stu-id="48c1b-124">It does this for each operation the provider has registered for.</span></span>  <span data-ttu-id="48c1b-125">Se, come nell'esempio precedente, il provider è stato registrato per PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED e un'applicazione ha creato un nuovo file nella radice della notifica, ProjFS chiamerebbe il callback **PRJ_NOTIFICATION_CB** con il nome del nuovo percorso del file e il parametro di _notifica_ impostato su PRJ_NOTIFICATION_NEW_FILE_CREATED.</span><span class="sxs-lookup"><span data-stu-id="48c1b-125">If, as in the above example, the provider registered for PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, and an application created a new file in the notification root, ProjFS would call the **PRJ_NOTIFICATION_CB** callback with the new file's path name and the _notification_ parameter set to PRJ_NOTIFICATION_NEW_FILE_CREATED.</span></span>

<span data-ttu-id="48c1b-126">ProjFS Invia le notifiche nell'elenco seguente prima che venga eseguita l'operazione di file system associata.</span><span class="sxs-lookup"><span data-stu-id="48c1b-126">ProjFS sends the notifications in the following list before the associated file system operation takes place.</span></span>  <span data-ttu-id="48c1b-127">Se il provider restituisce un codice di errore dal callback **PRJ_NOTIFICATION_CB** , l'operazione di file System avrà esito negativo e restituirà il codice di errore specificato dal provider.</span><span class="sxs-lookup"><span data-stu-id="48c1b-127">If the provider returns a failure code from the **PRJ_NOTIFICATION_CB** callback, the file system operation will fail and return the failure code the provider specified.</span></span>

* <span data-ttu-id="48c1b-128">PRJ_NOTIFICATION_PRE_DELETE: il file sta per essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="48c1b-128">PRJ_NOTIFICATION_PRE_DELETE - The file is about to be deleted.</span></span>
* <span data-ttu-id="48c1b-129">PRJ_NOTIFICATION_PRE_RENAME: il file sta per essere rinominato.</span><span class="sxs-lookup"><span data-stu-id="48c1b-129">PRJ_NOTIFICATION_PRE_RENAME - The file is about to be renamed.</span></span>
* <span data-ttu-id="48c1b-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK: sta per essere creato un collegamento reale per il file.</span><span class="sxs-lookup"><span data-stu-id="48c1b-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK - A hard link is about to be created for the file.</span></span>
* <span data-ttu-id="48c1b-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL: un file sta per essere espanso da un segnaposto a un file completo, che ne indica il contenuto che probabilmente verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="48c1b-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL - A file is about to be expanded from a placeholder to a full file, which indicates its contents are likely to be modified.</span></span>

<span data-ttu-id="48c1b-132">ProjFS Invia le notifiche nell'elenco seguente dopo il completamento dell'operazione di file system associata.</span><span class="sxs-lookup"><span data-stu-id="48c1b-132">ProjFS sends the notifications in the following list after the associated file system operation has completed.</span></span>

* <span data-ttu-id="48c1b-133">PRJ_NOTIFICATION_FILE_OPENED: è stato aperto un file esistente.</span><span class="sxs-lookup"><span data-stu-id="48c1b-133">PRJ_NOTIFICATION_FILE_OPENED - An existing file has been opened.</span></span>
  * <span data-ttu-id="48c1b-134">Anche se questa notifica viene inviata dopo l'apertura del file, il provider può restituire un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="48c1b-134">Even though this notification is sent after the file has been opened, the provider can return a failure code.</span></span>  <span data-ttu-id="48c1b-135">In risposta, ProjFS cancellerà l'apertura e restituirà l'errore al chiamante.</span><span class="sxs-lookup"><span data-stu-id="48c1b-135">In response, ProjFS will cancel the open and return the failure to the caller.</span></span>
* <span data-ttu-id="48c1b-136">PRJ_NOTIFICATION_NEW_FILE_CREATED: è stato creato un nuovo file.</span><span class="sxs-lookup"><span data-stu-id="48c1b-136">PRJ_NOTIFICATION_NEW_FILE_CREATED - A new file has been created.</span></span>
* <span data-ttu-id="48c1b-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN: un file esistente è stato sovrascritto, ad esempio chiamando [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) con il flag di **CREATE_ALWAYS** _dwCreationDisposition_ .</span><span class="sxs-lookup"><span data-stu-id="48c1b-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN - An existing file has been overwritten, for example by calling [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) with the **CREATE_ALWAYS** _dwCreationDisposition_ flag.</span></span>
* <span data-ttu-id="48c1b-138">PRJ_NOTIFICATION_FILE_RENAMED: un file è stato rinominato.</span><span class="sxs-lookup"><span data-stu-id="48c1b-138">PRJ_NOTIFICATION_FILE_RENAMED - A file has been renamed.</span></span>
* <span data-ttu-id="48c1b-139">PRJ_NOTIFICATION_HARDLINK_CREATED: è stato creato un [collegamento](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) reale per un file.</span><span class="sxs-lookup"><span data-stu-id="48c1b-139">PRJ_NOTIFICATION_HARDLINK_CREATED - A [hard link](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) has been created for a file.</span></span>
* <span data-ttu-id="48c1b-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION: un handle di file è stato chiuso e il contenuto del file non è stato modificato, né il file è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="48c1b-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION - A file handle has been closed, and the file's content was not modified, nor was the file deleted.</span></span>
* <span data-ttu-id="48c1b-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED: un handle di file è stato chiuso e il contenuto del file è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="48c1b-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED - A file handle has been closed, and the file's content has been modified.</span></span>
* <span data-ttu-id="48c1b-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED: un handle di file è stato chiuso e il file è stato eliminato come parte della chiusura dell'handle.</span><span class="sxs-lookup"><span data-stu-id="48c1b-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED - A file handle has been closed, and the file was deleted as part of closing the handle.</span></span>

<span data-ttu-id="48c1b-143">Per ulteriori informazioni su ogni notifica, fare riferimento alla documentazione per **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span><span class="sxs-lookup"><span data-stu-id="48c1b-143">For more details on each notification refer to the documentation for **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span></span>

<span data-ttu-id="48c1b-144">Il parametro _notificationParameters_ del callback **PRJ_NOTIFICATION_CB** specifica parametri aggiuntivi per determinate notifiche.</span><span class="sxs-lookup"><span data-stu-id="48c1b-144">The **PRJ_NOTIFICATION_CB** callback's _notificationParameters_ parameter specifies extra parameters for certain notifications.</span></span>  <span data-ttu-id="48c1b-145">Se un provider riceve un PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED o PRJ_NOTIFICATION_FILE_OVERWRITTEN, o PRJ_NOTIFICATION_FILE_RENAMED notifica, il provider può specificare un nuovo set di notifiche da ricevere per il file.</span><span class="sxs-lookup"><span data-stu-id="48c1b-145">If a provider receives a PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED, or PRJ_NOTIFICATION_FILE_OVERWRITTEN, or PRJ_NOTIFICATION_FILE_RENAMED notification, the provider can specify a new set of notifications to receive for the file.</span></span> <span data-ttu-id="48c1b-146">Per ulteriori informazioni, fare riferimento alla documentazione per **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span><span class="sxs-lookup"><span data-stu-id="48c1b-146">For further details, refer to the documentation for **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span></span>

<span data-ttu-id="48c1b-147">Nell'esempio seguente vengono illustrati esempi semplici di come un provider può elaborare le notifiche registrate per nel frammento di codice riportato sopra.</span><span class="sxs-lookup"><span data-stu-id="48c1b-147">The following sample shows simple examples of how a provider might process the notifications it registered for in the code snippet above.</span></span>

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