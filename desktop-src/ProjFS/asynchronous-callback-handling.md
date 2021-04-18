---
title: Completamento callback asincrono
description: Viene descritto in che modo il provider è in grado di servire in modo asincrono i callback.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/12/2018
ms.topic: article
ms.openlocfilehash: 8ec23f5ea6e8ec55be2eaa2811d9dee8b1870edc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300272"
---
# <a name="asynchronous-callback-handling"></a><span data-ttu-id="f9878-103">Gestione asincrona del callback</span><span class="sxs-lookup"><span data-stu-id="f9878-103">Asynchronous Callback Handling</span></span>

<span data-ttu-id="f9878-104">Quando un client interagisce con i file e le directory sotto la radice di virtualizzazione del provider, queste interazioni generano in genere i callback del provider richiamati.</span><span class="sxs-lookup"><span data-stu-id="f9878-104">When a client interacts with the files and directories beneath the provider's virtualization root, these interactions typically result in the provider's callbacks being invoked.</span></span>  <span data-ttu-id="f9878-105">ProjFS richiama i callback del provider inviando un messaggio dalla modalità kernel alla libreria in modalità utente ProjFS, dove un thread di lavoro riceve il messaggio e chiama il callback appropriato.</span><span class="sxs-lookup"><span data-stu-id="f9878-105">ProjFS invokes provider callbacks by sending a message from kernel mode to the ProjFS user-mode library, where a worker thread receives the message and calls the appropriate callback.</span></span>  <span data-ttu-id="f9878-106">Una volta restituito il callback, il thread di lavoro attende che un altro messaggio arrivi dalla modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="f9878-106">Once the callback has returned, the worker thread waits for another message to arrive from kernel mode.</span></span>  <span data-ttu-id="f9878-107">Se tutti i thread di lavoro sono occupati nell'esecuzione del codice di callback del provider, eventuali ulteriori operazioni di I/O client che attivano un blocco di callback fino a quando un thread di lavoro non diventa disponibile per ricevere il messaggio e richiamare il callback pertinente.</span><span class="sxs-lookup"><span data-stu-id="f9878-107">If all the worker threads are busy executing provider callback code, any further client I/O that triggers a callback blocks until a worker thread becomes available to receive the message and invoke the relevant callback.</span></span>  <span data-ttu-id="f9878-108">Quando un provider viene avviato, può specificare il numero di thread di lavoro che desidera che ProjFS crei ai callback del servizio tramite il parametro _options_ di **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)**.</span><span class="sxs-lookup"><span data-stu-id="f9878-108">When a provider starts up, it can specify the number of worker threads it wants ProjFS to create to service callbacks via the _options_ parameter of **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)**.</span></span>  <span data-ttu-id="f9878-109">Un provider può migliorare l'efficienza dei thread di lavoro che ricevono messaggi tramite la manutenzione asincrona dei callback.</span><span class="sxs-lookup"><span data-stu-id="f9878-109">A provider can improve the efficiency of the message-receiving worker threads by servicing its callbacks asynchronously.</span></span>

> <span data-ttu-id="f9878-110">Se il provider non specifica il parametro _options_ per **PrjStartVirtualizing** o se specifica 0 per il membro ConcurrentThreadCount del parametro _options_ , ProjFS utilizzerà il numero di processori logici nel sistema per il valore di ConcurrentThreadCount.</span><span class="sxs-lookup"><span data-stu-id="f9878-110">If the provider does not specify the _options_ parameter to **PrjStartVirtualizing**, or if it specifies 0 for the ConcurrentThreadCount member of the _options_ parameter, ProjFS will use the number of logical processors in the system for the value of ConcurrentThreadCount.</span></span>
>
> <span data-ttu-id="f9878-111">Se il provider non specifica il parametro _options_ per **PrjStartVirtualizing** o se specifica 0 per il membro PoolThreadCount del parametro _options_ , ProjFS utilizzerà il doppio del valore di ConcurrentThreadCount per il valore di PoolThreadCount.</span><span class="sxs-lookup"><span data-stu-id="f9878-111">If the provider does not specify the _options_ parameter to **PrjStartVirtualizing**, or if it specifies 0 for the PoolThreadCount member of the _options_ parameter, ProjFS will use twice the value of ConcurrentThreadCount for the value of PoolThreadCount.</span></span>

<span data-ttu-id="f9878-112">I servizi provider richiamano in modo asincrono restituendo HRESULT_FROM_WIN32 (ERROR_IO_PENDING) dai relativi callback e successivamente li completano utilizzando **[PrjCompleteCommand](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjcompletecommand)**.</span><span class="sxs-lookup"><span data-stu-id="f9878-112">A provider services callbacks asynchronously by returning HRESULT_FROM_WIN32(ERROR_IO_PENDING) from its callbacks and later completing them using **[PrjCompleteCommand](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjcompletecommand)**.</span></span>  <span data-ttu-id="f9878-113">Un provider che elabora i callback in modo asincrono deve supportare anche l'annullamento del callback implementando il callback **[PRJ_CANCEL_COMMAND_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb)** .</span><span class="sxs-lookup"><span data-stu-id="f9878-113">A provider that processes callbacks asynchronously should also support callback cancellation by implementing the **[PRJ_CANCEL_COMMAND_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb)** callback.</span></span>

<span data-ttu-id="f9878-114">Quando ProjFS chiama il callback di un provider, identifica la chiamata specifica del callback usando il membro CommandID del parametro _callBackData_ del callback.</span><span class="sxs-lookup"><span data-stu-id="f9878-114">When ProjFS calls a provider's callback, it identifies the specific invocation of the callback using the CommandId member of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="f9878-115">Se il provider decide di elaborare tale callback in modo asincrono, deve archiviare il valore del membro CommandID e restituire HRESULT_FROM_WIN32 (ERROR_IO_PENDING) dal callback.</span><span class="sxs-lookup"><span data-stu-id="f9878-115">If the provider decides to process that callback asynchronously, it must store the value of the CommandId member and return HRESULT_FROM_WIN32(ERROR_IO_PENDING) from the callback.</span></span>  <span data-ttu-id="f9878-116">Al termine dell'elaborazione del callback da parte del provider, viene chiamato **PrjCompleteCommand**, passando l'identificatore archiviato nel parametro _CommandID_ .</span><span class="sxs-lookup"><span data-stu-id="f9878-116">Once the provider has finished processing the callback, it calls **PrjCompleteCommand**, passing the stored identifier in the _commandId_ parameter.</span></span>  <span data-ttu-id="f9878-117">Indica a ProjFS quale chiamata di callback è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f9878-117">This tells ProjFS which callback invocation has been completed.</span></span>

<span data-ttu-id="f9878-118">Un provider che implementa il callback **PRJ_CANCEL_COMMAND_CB** deve tenere traccia dei callback non ancora completati.</span><span class="sxs-lookup"><span data-stu-id="f9878-118">A provider that implements the **PRJ_CANCEL_COMMAND_CB** callback must keep track of which callbacks it has not yet completed.</span></span>  <span data-ttu-id="f9878-119">Se il provider riceve questo callback, indica che l'I/O che ha causato la chiamata di uno di questi callback è stato annullato, in modo esplicito o perché il thread su cui è stato emesso è stato terminato.</span><span class="sxs-lookup"><span data-stu-id="f9878-119">If the provider receives this callback, it indicates that the I/O that caused one of those callbacks to be invoked was canceled, either explicitly or because the thread it was issued on terminated.</span></span> <span data-ttu-id="f9878-120">Il provider deve annullare l'elaborazione della chiamata di callback identificata da CommandID appena possibile.</span><span class="sxs-lookup"><span data-stu-id="f9878-120">The provider should cancel processing the callback invocation identified by CommandId as soon as possible.</span></span>

> <span data-ttu-id="f9878-121">Anche se ProjFS richiamerà **PRJ_CANCEL_COMMAND_CB** per un determinato oggetto CommandID solo dopo che il callback da annullare viene richiamato, l'annullamento e la chiamata originale possono essere eseguiti contemporaneamente in un provider multithread.</span><span class="sxs-lookup"><span data-stu-id="f9878-121">Although ProjFS will invoke **PRJ_CANCEL_COMMAND_CB** for a given CommandId only after the callback to be canceled is invoked, the cancellation and original invocation may run concurrently in a multithreaded provider.</span></span>  <span data-ttu-id="f9878-122">Il provider deve essere in grado di gestire normalmente questa situazione.</span><span class="sxs-lookup"><span data-stu-id="f9878-122">The provider must be able to gracefully handle this situation.</span></span>

<span data-ttu-id="f9878-123">L'esempio seguente è una versione dell'esempio fornita per l'argomento [enumerazione di file e directory](enumerating-files-and-directories.md) , modificato per illustrare la gestione asincrona dei callback.</span><span class="sxs-lookup"><span data-stu-id="f9878-123">The following sample is a version of the sample given for the [Enumerating Files and Directories](enumerating-files-and-directories.md) topic, modified to illustrate asynchronous callback handling.</span></span>

```C++
typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

typedef struct MY_ENUM_ENTRY {
    MY_ENUM_ENTRY* Next;
    PWSTR Name;
    BOOLEAN IsDirectory;
    INT64 FileSize;
} MY_ENUM_ENTRY;

typedef struct MY_ENUM_SESSION {
    GUID EnumerationId;
    PWSTR SearchExpression;
    USHORT SearchExpressionMaxLen;
    BOOLEAN SearchExpressionCaptured;
    MY_ENUM_ENTRY* EnumHead;
    MY_ENUM_ENTRY* LastEnumEntry;
    BOOLEAN EnumCompleted;
} MY_ENUM_SESSION;

typedef struct MY_ENUM_PARAMS {
    GUID EnumerationId;
    PRJ_DIR_ENTRY_BUFFER_HANDLE DirEntryBufferHandle;
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT NamespaceVirtualizationContext;
    INT32 CommandId;
    PRJ_CALLBACK_DATA_FLAGS Flags;
    WCHAR SearchExpression[1];
} MY_ENUM_PARAMS;

// Prototype for the enumeration worker routine.  In this example this is a
// ThreadProc.  See https://msdn.microsoft.com/library/windows/desktop/ms686736.aspx
DWORD WINAPI MyGetEnumCallbackWorker(_In_ LPVOID parameter);

#define ROLLBACK_NONE           0
#define ROLLBACK_PARAM_ALLOC    1
#define ROLLBACK_TRACK_ENUM     2

HRESULT
MyGetEnumCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ const GUID* enumerationId,
    _In_opt_z_ PCWSTR searchExpression,
    _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
    )
{
    UINT rollback = ROLLBACK_NONE;

    // This example creates a thread to run the enumeration in.  The provider
    // can access callbackData only while the callback is running, so we copy
    // out the fields that the worker thread will need.
    MY_ENUM_PARAMS* enumParams = NULL;
    size_t bufSize = sizeof(MY_ENUM_PARAMS);

    // Allocate enough space for the parameter buffer and the search expression
    // string plus a terminating NULL character.
    if (searchExpression != NULL)
    {
        bufSize += (wcslen(searchExpression) + 1) * sizeof(WCHAR);
    }
    else
    {
        // We'll store "*" as the search expression in this case.
        bufSize += 2 * sizeof(WCHAR);
    }

    enumParams = (MY_ENUM_PARAMS*) calloc(1, bufSize);

    if (enumParams == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // enumParams allocated.
    rollback = ROLLBACK_PARAM_ALLOC;

    // Copy the search expression into our parameter buffer.
    if (searchExpression != NULL)
    {
        wcsncpy_s(enumParams->SearchExpression,
                  wcslen(searchExpression),
                  searchExpression,
                  wcslen(searchExpression));
    }
    else
    {
        wcsncpy_s(enumParams->SearchExpression, 1, "*", 1);
    }

    // Copy the other parameters into our parameter buffer.
    enumParams->EnumerationId = enumerationId;
    enumParams->DirEntryBufferHandle = dirEntryBufferHandle;
    enumParams->NamespaceVirtualizationContext = callbackData->NamespaceVirtualizationContext
    enumParams->CommandId = callbackData->CommandId;
    enumParams->Flags = callbackData->Flags;

    // MyTrackEnumForCancellation is a routine the provider might implement to
    // track active enumeration callbacks in case they are cancelled.  It stores
    // the CommandId for the callback in some structure.
    hr = MyTrackEnumForCancellation(callbackData->CommandId);

    if (FAILED(hr))
    {
        goto RollbackOnError;
    }

    // Enum callback tracked.
    rollback = ROLLBACK_TRACK_ENUM;

    // Create the worker thread.
    HANDLE workerThread = NULL;
    workerThread = CreateThread(NULL,
                                0,
                                MyGetEnumCallbackWorker,
                                enumParams,
                                0
                                NULL);

    // We'll treat failure to create the thread as a low-resources error.
    if (workerThread == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // Return pending to signal that we'll complete the enumeration later.
    return HRESULT_FROM_WIN32(ERROR_IO_PENDING);

RollbackOnError:

    // Clean up manually.  Note the fall-through structure of the switch, and that
    // we clean up in reverse order.
    switch(rollback)
    {
    case ROLLBACK_TRACK_ENUM:
        // MyUntrackEnumForCancellation removes the CommandId for the callback
        // from the structure that MyTrackEnumForCancellation put it in.
        MyUntrackEnumForCancellation(callbackData->CommandId);

    case ROLLBACK_PARAM_ALLOC:
        free(enumParams);

    default:
        break;
    }

    return hr;
}

DWORD
WINAPI
MyGetEnumCallbackWorker(
    _In_ LPVOID parameter
)
{
    HRESULT hr = S_OK;
    MY_ENUM_PARAMS* enumParams = (MY_ENUM_PARAMS*) parameter;

    // MyCheckEnumForCancellation is a routine the provider might implement to
    // check whether a pended enumeration callback has been cancelled.  Even
    // though the enumeration has been cancelled, ProjFS will still call the
    // provider's end-enumeration callback.  This allows general cleanup, such
    // as tearing down the enumeration session, to always happen in that callback.
    if (MyCheckEnumForCancellation(enumParams->CommandId))
    {
        // The operation has been cancelled.  Clean up and get out.
        free(enumParams);
        return 0;
    }

    // MyGetEnumSession is a routine the provider might implement to find
    // information about the enumeration session that it first stored
    // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
    //
    // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
    // already retrieved a list of the items in the backing store located at
    // callbackData->FilePathName, sorted them using PrjFileNameCompare()
    // to determine collation order, and stored the list in session->EnumHead.
    MY_ENUM_SESSION* session = NULL;
    session = MyGetEnumSession(enumParams->EnumerationId);

    if (session == NULL)
    {
        hr = HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        goto CompleteCallback;
    }

    if (!session->SearchExpressionCaptured ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
    {
        if (wcsncpy_s(session->SearchExpression,
                      session->SearchExpressionMaxLen,
                      enumParams->SearchExpression,
                      wcslen(enumParams->SearchExpression)))
        {
            // Failed to copy the search expression; perhaps the provider
            // could try reallocating session->SearchExpression.
        }

        session->SearchExpressionCaptured = TRUE;
    }

    MY_ENUM_ENTRY* enumHead = NULL;

    // We have to start the enumeration from the beginning if we aren't
    // continuing an existing session or if the caller is requesting a restart.
    if (((session->LastEnumEntry == NULL) &&
         !session->EnumCompleted) ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
    {
        // Ensure that if the caller is requesting a restart we reset our
        // bookmark of how far we got in the enumeration.
        session->LastEnumEntry = NULL;

        // In case we're restarting ensure we don't think we're done.
        session->EnumCompleted = FALSE;

        // We need to start considering items from the beginning of the list
        // retrieved from the backing store.
        enumHead = session->EnumHead;
    }
    else
    {
        // We are resuming an existing enumeration session.  Note that
        // session->LastEnumEntry may be NULL.  That is okay; it means
        // we got all the entries the last time this callback was invoked.
        // Returning S_OK without adding any new entries to the
        // enumParams->DirEntryBufferHandle buffer signals ProjFS that the
        // enumeration has returned everything it can.
        enumHead = session->LastEnumEntry;
    }

    if (enumHead == NULL)
    {
        // There are no items to return.  Remember that we've returned everything
        // we can.
        session->EnumCompleted = TRUE;
    }
    else
    {
        MY_ENUM_ENTRY* thisEntry = enumHead;
        while (thisEntry != NULL)
        {
            // We'll insert the entry into the return buffer if it matches
            // the search expression captured for this enumeration session.
            if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
            {
                PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                fileBasicInfo.FileSize = thisEntry->FileSize;

                // Format the entry for return to ProjFS.
                if (S_OK != PrjFillDirEntryBuffer(thisEntry->Name,
                                                  &fileBasicInfo,
                                                  enumParams->DirEntryBufferHandle))
                {
                    // We couldn't add this entry to the buffer; remember where we left
                    // off for the next time we're called for this enumeration session.
                    session->LastEnumEntry = thisEntry;
                    hr = S_OK;

                    goto CompleteCallback;
                }
            }

            thisEntry = thisEntry->Next;
        }

        // We reached the end of the list of entries; remember that we've returned
        // everything we can.
        session->EnumCompleted = TRUE;
    }

CompleteCallback:

    // Signal ProjFS that we've completed this callback.  Since this is an enumeration
    // we use the extendedParameters parameter to PrjCompleteCommand.
    PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS extendedParams = {};
    extendedParams.CommandType = PRJ_COMPLETE_COMMAND_TYPE_ENUMERATION;
    extendedParams.enumeration.DirEntryBufferHandle = enumParams->DirEntryBufferHandle;

    PrjCompleteCommand(enumParams->NamespaceVirtualizationContext,
                       enumParams->CommandId,
                       hr,
                       &extendedParams);

    MyUntrackEnumForCancellation(enumParams->CommandId);

    free(enumParams);

    // ThreadProc returns 0 on successful completion.
    return 0;
}
```

<span data-ttu-id="f9878-124">Ecco un breve esempio PRJ_CANCEL_COMMAND_CB che funziona con il codice di esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="f9878-124">And here is a brief example PRJ_CANCEL_COMMAND_CB that works with the preceding sample code.</span></span>

```C++
void
MyCancelCommandCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
)
{
    // MyMarkEnumForCancellation is a routine the provider might implement to
    // mark a pended enumeration callback as cancelled.  If the given CommandId
    // is not found, it is not an error.  It may not yet have been tracked or
    // it may already have completed and been untracked.
    MyMarkEnumForCancellation(callbackData->CommandId);
}
```