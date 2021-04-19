---
description: Consentire agli utenti di annullare le richieste di I/O lente o bloccate può migliorare l'usabilità e l'affidabilità dell'applicazione.
ms.assetid: adfe6d05-f30b-40a1-b3b0-58e2593e7b25
title: Annullamento di operazioni di I/O in sospeso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d108409eea32cf18a94f83bf7aacd282c60d3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317808"
---
# <a name="canceling-pending-io-operations"></a><span data-ttu-id="d4fa7-103">Annullamento di operazioni di I/O in sospeso</span><span class="sxs-lookup"><span data-stu-id="d4fa7-103">Canceling Pending I/O Operations</span></span>

<span data-ttu-id="d4fa7-104">Consentire agli utenti di annullare le richieste di I/O lente o bloccate può migliorare l'usabilità e l'affidabilità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-104">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span> <span data-ttu-id="d4fa7-105">Se, ad esempio, una chiamata alla funzione [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) è bloccata perché la chiamata è a un dispositivo molto lento, l'annullamento consente di eseguire di nuovo la chiamata con nuovi parametri senza terminare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-105">For example, if a call to the [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) function is blocked because the call is to a very slow device, canceling it enables the call to be made again, with new parameters, without terminating the application.</span></span>

<span data-ttu-id="d4fa7-106">Windows Vista estende le funzionalità di annullamento e include il supporto per l'annullamento delle operazioni sincrone.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-106">Windows Vista extends the cancellation capabilities and includes support for canceling synchronous operations.</span></span>

<span data-ttu-id="d4fa7-107">**Nota**  La chiamata della funzione [**CancelIoEx**](cancelioex-func.md) non garantisce che un'operazione di I/O venga annullata; il driver che gestisce l'operazione deve supportare l'annullamento e l'operazione deve essere in uno stato che può essere annullato.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-107">**Note**  Calling the [**CancelIoEx**](cancelioex-func.md) function does not guarantee that an I/O operation will be canceled; the driver which is handling the operation must support cancellation and the operation must be in a state that can be canceled.</span></span>

## <a name="cancellation-considerations"></a><span data-ttu-id="d4fa7-108">Considerazioni sull'annullamento</span><span class="sxs-lookup"><span data-stu-id="d4fa7-108">Cancellation Considerations</span></span>

<span data-ttu-id="d4fa7-109">Quando si programmano le chiamate di annullamento, tenere presenti le considerazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4fa7-109">When programming cancellation calls, keep in mind the following considerations:</span></span>

-   <span data-ttu-id="d4fa7-110">Non vi è alcuna garanzia che i driver sottostanti supportino correttamente l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-110">There is no guarantee that underlying drivers correctly support cancellation.</span></span>
-   <span data-ttu-id="d4fa7-111">Quando si annulla l'I/O asincrono, quando non viene fornita alcuna struttura sovrapposta alla funzione [**CancelIoEx**](cancelioex-func.md) , la funzione tenta di annullare tutti i/o in attesa sul file in tutti i thread nel processo.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-111">When canceling asynchronous I/O, when no overlapped structure is supplied to the [**CancelIoEx**](cancelioex-func.md) function, the function attempts to cancel all outstanding I/O on the file on all threads in the process.</span></span> <span data-ttu-id="d4fa7-112">Ogni thread viene elaborato singolarmente, quindi, dopo che un thread è stato elaborato, può avviare un'altra operazione di I/O nel file prima che tutti gli altri thread abbiano il relativo I/O per il file annullato, causando problemi di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-112">Each thread is processed individually, so after a thread has been processed it may start another I/O on the file before all the other threads have had their I/O for the file canceled, causing synchronization issues.</span></span>
-   <span data-ttu-id="d4fa7-113">Quando si annulla l'I/O asincrono, non riutilizzare le strutture sovrapposte con l'annullamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-113">When canceling asynchronous I/O, do not reuse overlapped structures with targeted cancellation.</span></span> <span data-ttu-id="d4fa7-114">Dopo che l'operazione di I/O è stata completata correttamente o con uno stato annullato, la struttura sovrapposta non è più utilizzata dal sistema e può essere riutilizzata.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-114">Once the I/O operation completes (either successfully or with a canceled status) then the overlapped structure is no longer in use by the system and can be reused.</span></span>
-   <span data-ttu-id="d4fa7-115">Quando si annulla l'I/O sincrono, la chiamata della funzione [**CancelSynchronousIo**](cancelsynchronousio-func.md) tenta di annullare tutte le chiamate sincrone correnti sul thread.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-115">When canceling synchronous I/O, calling the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function attempts to cancel any current synchronous call on the thread.</span></span> <span data-ttu-id="d4fa7-116">È necessario prestare attenzione per assicurarsi che la sincronizzazione delle chiamate sia corretta; la chiamata errata in una serie di chiamate potrebbe essere annullata.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-116">You must take care to ensure the synchronization of the calls is correct; the wrong call in a series of calls could get canceled.</span></span> <span data-ttu-id="d4fa7-117">Se, ad esempio, la funzione **CancelSynchronousIo** viene chiamata per un'operazione sincrona, x, l'operazione Y viene avviata solo dopo il completamento dell'operazione x, in genere o con un errore.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-117">For example, if the **CancelSynchronousIo** function is called for a synchronous operation, X, operation Y only starts after that operation X is completed (normally or with an error).</span></span> <span data-ttu-id="d4fa7-118">Se il thread che ha chiamato l'operazione X avvia un'altra chiamata sincrona a X, la chiamata Cancel potrebbe interrompere questa nuova richiesta di I/O.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-118">If the thread that called operation X then starts another synchronous call to X, the cancel call could interrupt this new I/O request.</span></span>
-   <span data-ttu-id="d4fa7-119">Quando si annulla l'I/O sincrono, tenere presente che è possibile che esista un race condition ogni volta che un thread viene condiviso tra parti diverse di un'applicazione, ad esempio con un thread del pool di thread.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-119">When canceling synchronous I/O, be aware that a race condition can exist whenever a thread is shared between different parts of an application, for example, with a thread-pool thread.</span></span>

## <a name="operations-that-cannot-be-canceled"></a><span data-ttu-id="d4fa7-120">Operazioni che non possono essere annullate</span><span class="sxs-lookup"><span data-stu-id="d4fa7-120">Operations That Cannot Be Canceled</span></span>

<span data-ttu-id="d4fa7-121">Alcune funzioni non possono essere annullate mediante la funzione [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md)o [**CancelSynchronousIo**](cancelsynchronousio-func.md) .</span><span class="sxs-lookup"><span data-stu-id="d4fa7-121">Some functions cannot be canceled using the [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md), or [**CancelSynchronousIo**](cancelsynchronousio-func.md) function.</span></span> <span data-ttu-id="d4fa7-122">Alcune di queste funzioni sono state estese per consentire l'annullamento (ad esempio, la funzione [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) ) ed è consigliabile usarle.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-122">Some of these functions have been extended to allow cancellation (for example, the [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) function) and you should use these instead.</span></span> <span data-ttu-id="d4fa7-123">Oltre a supportare l'annullamento, queste funzioni dispongono anche di callback predefiniti per supportare l'utente durante il rilevamento dello stato di avanzamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-123">In addition to supporting cancellation, these functions also have built-in callbacks to support you when tracking the progress of the operation.</span></span> <span data-ttu-id="d4fa7-124">Le funzioni seguenti non supportano l'annullamento:</span><span class="sxs-lookup"><span data-stu-id="d4fa7-124">The following functions do not support cancellation:</span></span>

-   <span data-ttu-id="d4fa7-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)-USA [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span><span class="sxs-lookup"><span data-stu-id="d4fa7-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)—use [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span></span>
-   <span data-ttu-id="d4fa7-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)-USA [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="d4fa7-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   <span data-ttu-id="d4fa7-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)-USA [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="d4fa7-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   [<span data-ttu-id="d4fa7-128">**ReplaceFile**</span><span class="sxs-lookup"><span data-stu-id="d4fa7-128">**ReplaceFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

<span data-ttu-id="d4fa7-129">Per ulteriori informazioni, vedere [linee guida di completamento/annullamento di I/O](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span><span class="sxs-lookup"><span data-stu-id="d4fa7-129">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

## <a name="canceling-asynchronous-io"></a><span data-ttu-id="d4fa7-130">Annullamento di I/O asincrono</span><span class="sxs-lookup"><span data-stu-id="d4fa7-130">Canceling Asynchronous I/O</span></span>

<span data-ttu-id="d4fa7-131">È possibile annullare l'I/O asincrono da qualsiasi thread nel processo che ha emesso l'operazione di I/O.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-131">You can cancel asynchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="d4fa7-132">È necessario specificare l'handle su cui è stato eseguito l'i/O e, facoltativamente, la struttura sovrapposta usata per eseguire l'i/O.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-132">You must specify the handle which the I/O was performed on and, optionally, the overlapped structure that was used to perform the I/O.</span></span> <span data-ttu-id="d4fa7-133">È possibile determinare se l'annullamento si è verificato esaminando lo stato restituito nella struttura sovrapposta o nel callback di completamento.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-133">You can determine if the cancel occurred by examining the status returned in the overlapped structure or in the completion callback.</span></span> <span data-ttu-id="d4fa7-134">Lo stato dell' **operazione di errore \_ \_ interrotto** indica che l'operazione è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-134">A status of **ERROR\_OPERATION\_ABORTED** indicates that the operation was canceled.</span></span>

<span data-ttu-id="d4fa7-135">Nell'esempio seguente viene illustrata una routine che accetta un timeout e tenta un'operazione di lettura, annullando la funzione [**CancelIoEx**](cancelioex-func.md) se il timeout scade.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-135">The following example shows a routine that takes a timeout and attempts a read operation, canceling it with the [**CancelIoEx**](cancelioex-func.md) function if the timeout expires.</span></span>


```C++
#include <windows.h>

BOOL DoCancelableRead(HANDLE hFile,
                 LPVOID lpBuffer,
                 DWORD nNumberOfBytesToRead,
                 LPDWORD lpNumberOfBytesRead,
                 LPOVERLAPPED lpOverlapped,
                 DWORD dwTimeout,
                 LPBOOL pbCancelCalled)
//
// Parameters:
//
//      hFile - An open handle to a readable file or device.
//
//      lpBuffer - A pointer to the buffer to store the data being read.
//
//      nNumberOfBytesToRead - The number of bytes to read from the file or 
//          device. Must be less than or equal to the actual size of
//          the buffer referenced by lpBuffer.
//
//      lpNumberOfBytesRead - A pointer to a DWORD to receive the number 
//          of bytes read after all I/O is complete or canceled.
//
//      lpOverlapped - A pointer to a preconfigured OVERLAPPED structure that
//          has a valid hEvent.
//          If the caller does not properly initialize this structure, this
//          routine will fail.
//
//      dwTimeout - The desired time-out, in milliseconds, for the I/O read.
//          After this time expires, the I/O is canceled.
// 
//      pbCancelCalled - A pointer to a Boolean to notify the caller if this
//          routine attempted to perform an I/O cancel.
//
// Return Value:
//
//      TRUE on success, FALSE on failure.
//
{
    BOOL result;
    DWORD waitTimer;
    BOOL bIoComplete = FALSE;
    const DWORD PollInterval = 100; // milliseconds

    // Initialize "out" parameters
    *pbCancelCalled = FALSE;
    *lpNumberOfBytesRead = 0;

    // Perform the I/O, in this case a read operation.
    result = ReadFile(hFile,
                  lpBuffer,
                  nNumberOfBytesToRead,
                  lpNumberOfBytesRead,
                  lpOverlapped );

    if (result == FALSE) 
    {
        if (GetLastError() != ERROR_IO_PENDING) 
        {
            // The function call failed. ToDo: Error logging and recovery.
            return FALSE; 
        }
    } 
    else 
    {
        // The I/O completed, done.
        return TRUE;
    }
        
    // The I/O is pending, so wait and see if the call times out.
    // If so, cancel the I/O using the CancelIoEx function.

    for (waitTimer = 0; waitTimer < dwTimeout; waitTimer += PollInterval)
    {
        result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, FALSE );
        if (result == FALSE)
        {
            if (GetLastError() != ERROR_IO_PENDING)
            {
                // The function call failed. ToDo: Error logging and recovery.
                return FALSE;
            }
            Sleep(PollInterval);
        }
        else
        {
            bIoComplete = TRUE;
            break;
        }
    }

    if (bIoComplete == FALSE) 
    {
        result = CancelIoEx( hFile, lpOverlapped );
        
        *pbCancelCalled = TRUE;

        if (result == TRUE || GetLastError() != ERROR_NOT_FOUND) 
        {
            // Wait for the I/O subsystem to acknowledge our cancellation.
            // Depending on the timing of the calls, the I/O might complete with a
            // cancellation status, or it might complete normally (if the ReadFile was
            // in the process of completing at the time CancelIoEx was called, or if
            // the device does not support cancellation).
            // This call specifies TRUE for the bWait parameter, which will block
            // until the I/O either completes or is canceled, thus resuming execution, 
            // provided the underlying device driver and associated hardware are functioning 
            // properly. If there is a problem with the driver it is better to stop 
            // responding here than to try to continue while masking the problem.

            result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, TRUE );

            // ToDo: check result and log errors. 
        }
    }

    return result;
}
```



## <a name="canceling-synchronous-io"></a><span data-ttu-id="d4fa7-136">Annullamento di I/O sincrono</span><span class="sxs-lookup"><span data-stu-id="d4fa7-136">Canceling Synchronous I/O</span></span>

<span data-ttu-id="d4fa7-137">È possibile annullare l'I/O sincrono da qualsiasi thread nel processo che ha emesso l'operazione di I/O.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-137">You can cancel synchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="d4fa7-138">È necessario specificare l'handle per il thread che sta attualmente eseguendo l'operazione di I/O.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-138">You must specify the handle to the thread which is currently performing the I/O operation.</span></span>

<span data-ttu-id="d4fa7-139">Nell'esempio seguente vengono illustrate due routine:</span><span class="sxs-lookup"><span data-stu-id="d4fa7-139">The following example shows two routines:</span></span>

-   <span data-ttu-id="d4fa7-140">La funzione **SynchronousIoWorker** è un thread di lavoro che implementa alcuni i/O di file sincroni, a partire da una chiamata alla funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="d4fa7-140">The **SynchronousIoWorker** function is a worker thread that implements some synchronous file I/O, starting with a call to the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="d4fa7-141">Se la routine ha esito positivo, la routine può essere seguita da operazioni aggiuntive, che non sono incluse in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-141">If the routine is successful, the routine can be followed by additional operations, which are not included here.</span></span> <span data-ttu-id="d4fa7-142">La variabile globale *gCompletionStatus* può essere usata per determinare se tutte le operazioni sono state completate o se un'operazione non è riuscita o è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-142">The global variable *gCompletionStatus* can be used to determine whether all operations succeeded or whether an operation failed or was canceled.</span></span> <span data-ttu-id="d4fa7-143">La variabile globale *dwOperationInProgress* indica se l'I/O del file è ancora in corso.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-143">The global variable *dwOperationInProgress* indicates whether file I/O is still in progress.</span></span>

    <span data-ttu-id="d4fa7-144">**Nota**  In questo esempio, il thread dell'interfaccia utente può verificare anche l'esistenza del thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-144">**Note**  In this example, the UI thread could also check for the existence of the worker thread.</span></span>

    <span data-ttu-id="d4fa7-145">I controlli manuali aggiuntivi, che non sono inclusi in questo argomento, sono necessari nella funzione **SynchronousIoWorker** per assicurarsi che se l'annullamento è stato richiesto durante i brevi periodi tra le chiamate di i/O di file, il resto delle operazioni verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-145">Additional manual checks, which are not included here, are required in the **SynchronousIoWorker** function is to ensure that if the cancellation was requested during the brief periods between file I/O calls, the rest of the operations will be canceled.</span></span>

-   <span data-ttu-id="d4fa7-146">La funzione **MainUIThreadMessageHandler** simula il gestore di messaggi all'interno di una routine della finestra del thread dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-146">The **MainUIThreadMessageHandler** function simulates the message handler within a UI thread's window procedure.</span></span> <span data-ttu-id="d4fa7-147">L'utente richiede un set di operazioni sincrone sui file facendo clic su un controllo, che genera un messaggio di finestra definito dall'utente, nella sezione contrassegnata da WM con una **\_ sincope**.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-147">The user requests a set of synchronous file operations by clicking a control, which generates a user-defined window message, (in the section marked by **WM\_MYSYNCOPS**).</span></span> <span data-ttu-id="d4fa7-148">Viene creato un nuovo thread utilizzando la funzione **CreateFileThread** , che avvia quindi la funzione **SynchronousIoWorker** è.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-148">This creates a new thread using the **CreateFileThread** function, which then starts the **SynchronousIoWorker** function is.</span></span> <span data-ttu-id="d4fa7-149">Il thread dell'interfaccia utente continua a elaborare i messaggi mentre il thread di lavoro esegue l'I/O richiesto.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-149">The UI thread continues to process messages while the worker thread performs the requested I/O.</span></span> <span data-ttu-id="d4fa7-150">Se l'utente decide di annullare le operazioni non completate, in genere facendo clic su un pulsante Annulla, la routine (nella sezione contrassegnata da **WM \_ Annulla**) chiama la funzione [**CancelSynchronousIo**](cancelsynchronousio-func.md) usando l'handle del thread restituito dalla funzione **CreateFileThread** .</span><span class="sxs-lookup"><span data-stu-id="d4fa7-150">If the user decides to cancel the unfinished operations (typically by clicking a cancel button), the routine (in the section marked by **WM\_MYCANCEL**) calls the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function using the thread handle returned by the **CreateFileThread** function.</span></span> <span data-ttu-id="d4fa7-151">La funzione **CancelSynchronousIo** viene restituita immediatamente dopo il tentativo di annullamento.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-151">The **CancelSynchronousIo** function returns immediately after the cancellation attempt.</span></span> <span data-ttu-id="d4fa7-152">Infine, l'utente o l'applicazione può richiedere successivamente un'altra operazione che dipende dal fatto che le operazioni sui file siano state completate.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-152">Finally, the user or application may later request some other operation that depends on whether the file operations have completed.</span></span> <span data-ttu-id="d4fa7-153">In questo caso, la routine (nella sezione contrassegnata da **WM \_ PROCESSDATA**) verifica prima di tutto che le operazioni siano state completate e quindi esegue le operazioni di pulizia.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-153">In this case, the routine (in the section marked by **WM\_PROCESSDATA**) first verifies that the operations have completed and then executes the clean-up operations.</span></span>

    <span data-ttu-id="d4fa7-154">**Nota**  In questo esempio, dal momento che l'annullamento potrebbe essersi verificato in qualsiasi punto della sequenza di operazioni, potrebbe essere necessario che il chiamante assicuri che lo stato sia coerente o almeno compreso prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-154">**Note**  In this example, since the cancellation could have occurred anywhere in the sequence of operations, it may be necessary for the caller to ensure that the state is consistent, or at least understood, before proceeding.</span></span>


```C++
// User-defined codes for the message-pump, which is outside the scope 
// of this sample. Windows messaging and message pumps are well-documented
// elsewhere.
#define WM_MYSYNCOPS    1
#define WM_MYCANCEL     2
#define WM_PROCESSDATA  3

VOID SynchronousIoWorker( VOID *pv )
{
    LPCSTR lpFileName = (LPCSTR)pv;
    HANDLE hFile;
    g_dwOperationInProgress = TRUE;    
    g_CompletionStatus = ERROR_SUCCESS;
     
    hFile = CreateFileA(lpFileName,
                        GENERIC_READ,
                        0,
                        NULL,
                        OPEN_EXISTING,
                        0,
                        NULL);


    if (hFile != INVALID_HANDLE_VALUE) 
    {
        BOOL result = TRUE;
        // TODO: CreateFile succeeded. 
        // Insert your code to make more synchronous calls with hFile.
        // The result variable is assumed to act as the error flag here,
        // but can be whatever your code needs.
        
        if (result == FALSE) 
        {
            // An operation failed or was canceled. If it was canceled,
            // GetLastError() returns ERROR_OPERATION_ABORTED.

            g_CompletionStatus = GetLastError();            
        }
             
        CloseHandle(hFile);
    } 
    else 
    {
        // CreateFile failed or was canceled. If it was canceled,
        // GetLastError() returns ERROR_OPERATION_ABORTED.
        g_CompletionStatus = GetLastError();
    }

    g_dwOperationInProgress = FALSE;
}  


LRESULT
CALLBACK
MainUIThreadMessageHandler(HWND hwnd,
                           UINT uMsg,
                           WPARAM wParam,
                           LPARAM lParam)
{
    UNREFERENCED_PARAMETER(hwnd);
    UNREFERENCED_PARAMETER(wParam);
    UNREFERENCED_PARAMETER(lParam);
    HANDLE syncThread = INVALID_HANDLE_VALUE;

    //  Insert your initializations here.

    switch (uMsg) 
    {
        // User requested an operation on a file.  Insert your code to 
        // retrieve filename from parameters.
        case WM_MYSYNCOPS:    
            syncThread = CreateThread(
                          NULL,
                          0,
                          (LPTHREAD_START_ROUTINE)SynchronousIoWorker,
                          &g_lpFileName,
                          0,
                          NULL);

            if (syncThread == INVALID_HANDLE_VALUE) 
            {
                // Insert your code to handle the failure.
            }
        break;
    
        // User clicked a cancel button.
        case WM_MYCANCEL:
            if (syncThread != INVALID_HANDLE_VALUE) 
            {
                CancelSynchronousIo(syncThread);
            }
        break;

        // User requested other operations.
        case WM_PROCESSDATA:
            if (!g_dwOperationInProgress) 
            {
                if (g_CompletionStatus == ERROR_OPERATION_ABORTED) 
                {
                    // Insert your cleanup code here.
                } 
                else
                {
                    // Insert code to handle other cases.
                }
            }
        break;
    } 

    return TRUE;
} 
```



## <a name="related-topics"></a><span data-ttu-id="d4fa7-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d4fa7-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4fa7-156">I/O sincrono e asincrono</span><span class="sxs-lookup"><span data-stu-id="d4fa7-156">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



