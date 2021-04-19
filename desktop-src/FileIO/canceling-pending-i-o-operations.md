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
# <a name="canceling-pending-io-operations"></a>Annullamento di operazioni di I/O in sospeso

Consentire agli utenti di annullare le richieste di I/O lente o bloccate può migliorare l'usabilità e l'affidabilità dell'applicazione. Se, ad esempio, una chiamata alla funzione [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) è bloccata perché la chiamata è a un dispositivo molto lento, l'annullamento consente di eseguire di nuovo la chiamata con nuovi parametri senza terminare l'applicazione.

Windows Vista estende le funzionalità di annullamento e include il supporto per l'annullamento delle operazioni sincrone.

**Nota**  La chiamata della funzione [**CancelIoEx**](cancelioex-func.md) non garantisce che un'operazione di I/O venga annullata; il driver che gestisce l'operazione deve supportare l'annullamento e l'operazione deve essere in uno stato che può essere annullato.

## <a name="cancellation-considerations"></a>Considerazioni sull'annullamento

Quando si programmano le chiamate di annullamento, tenere presenti le considerazioni seguenti:

-   Non vi è alcuna garanzia che i driver sottostanti supportino correttamente l'annullamento.
-   Quando si annulla l'I/O asincrono, quando non viene fornita alcuna struttura sovrapposta alla funzione [**CancelIoEx**](cancelioex-func.md) , la funzione tenta di annullare tutti i/o in attesa sul file in tutti i thread nel processo. Ogni thread viene elaborato singolarmente, quindi, dopo che un thread è stato elaborato, può avviare un'altra operazione di I/O nel file prima che tutti gli altri thread abbiano il relativo I/O per il file annullato, causando problemi di sincronizzazione.
-   Quando si annulla l'I/O asincrono, non riutilizzare le strutture sovrapposte con l'annullamento di destinazione. Dopo che l'operazione di I/O è stata completata correttamente o con uno stato annullato, la struttura sovrapposta non è più utilizzata dal sistema e può essere riutilizzata.
-   Quando si annulla l'I/O sincrono, la chiamata della funzione [**CancelSynchronousIo**](cancelsynchronousio-func.md) tenta di annullare tutte le chiamate sincrone correnti sul thread. È necessario prestare attenzione per assicurarsi che la sincronizzazione delle chiamate sia corretta; la chiamata errata in una serie di chiamate potrebbe essere annullata. Se, ad esempio, la funzione **CancelSynchronousIo** viene chiamata per un'operazione sincrona, x, l'operazione Y viene avviata solo dopo il completamento dell'operazione x, in genere o con un errore. Se il thread che ha chiamato l'operazione X avvia un'altra chiamata sincrona a X, la chiamata Cancel potrebbe interrompere questa nuova richiesta di I/O.
-   Quando si annulla l'I/O sincrono, tenere presente che è possibile che esista un race condition ogni volta che un thread viene condiviso tra parti diverse di un'applicazione, ad esempio con un thread del pool di thread.

## <a name="operations-that-cannot-be-canceled"></a>Operazioni che non possono essere annullate

Alcune funzioni non possono essere annullate mediante la funzione [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md)o [**CancelSynchronousIo**](cancelsynchronousio-func.md) . Alcune di queste funzioni sono state estese per consentire l'annullamento (ad esempio, la funzione [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) ) ed è consigliabile usarle. Oltre a supportare l'annullamento, queste funzioni dispongono anche di callback predefiniti per supportare l'utente durante il rilevamento dello stato di avanzamento dell'operazione. Le funzioni seguenti non supportano l'annullamento:

-   [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)-USA [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
-   [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)-USA [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)-USA [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

Per ulteriori informazioni, vedere [linee guida di completamento/annullamento di I/O](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).

## <a name="canceling-asynchronous-io"></a>Annullamento di I/O asincrono

È possibile annullare l'I/O asincrono da qualsiasi thread nel processo che ha emesso l'operazione di I/O. È necessario specificare l'handle su cui è stato eseguito l'i/O e, facoltativamente, la struttura sovrapposta usata per eseguire l'i/O. È possibile determinare se l'annullamento si è verificato esaminando lo stato restituito nella struttura sovrapposta o nel callback di completamento. Lo stato dell' **operazione di errore \_ \_ interrotto** indica che l'operazione è stata annullata.

Nell'esempio seguente viene illustrata una routine che accetta un timeout e tenta un'operazione di lettura, annullando la funzione [**CancelIoEx**](cancelioex-func.md) se il timeout scade.


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



## <a name="canceling-synchronous-io"></a>Annullamento di I/O sincrono

È possibile annullare l'I/O sincrono da qualsiasi thread nel processo che ha emesso l'operazione di I/O. È necessario specificare l'handle per il thread che sta attualmente eseguendo l'operazione di I/O.

Nell'esempio seguente vengono illustrate due routine:

-   La funzione **SynchronousIoWorker** è un thread di lavoro che implementa alcuni i/O di file sincroni, a partire da una chiamata alla funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Se la routine ha esito positivo, la routine può essere seguita da operazioni aggiuntive, che non sono incluse in questa sezione. La variabile globale *gCompletionStatus* può essere usata per determinare se tutte le operazioni sono state completate o se un'operazione non è riuscita o è stata annullata. La variabile globale *dwOperationInProgress* indica se l'I/O del file è ancora in corso.

    **Nota**  In questo esempio, il thread dell'interfaccia utente può verificare anche l'esistenza del thread di lavoro.

    I controlli manuali aggiuntivi, che non sono inclusi in questo argomento, sono necessari nella funzione **SynchronousIoWorker** per assicurarsi che se l'annullamento è stato richiesto durante i brevi periodi tra le chiamate di i/O di file, il resto delle operazioni verrà annullato.

-   La funzione **MainUIThreadMessageHandler** simula il gestore di messaggi all'interno di una routine della finestra del thread dell'interfaccia utente. L'utente richiede un set di operazioni sincrone sui file facendo clic su un controllo, che genera un messaggio di finestra definito dall'utente, nella sezione contrassegnata da WM con una **\_ sincope**. Viene creato un nuovo thread utilizzando la funzione **CreateFileThread** , che avvia quindi la funzione **SynchronousIoWorker** è. Il thread dell'interfaccia utente continua a elaborare i messaggi mentre il thread di lavoro esegue l'I/O richiesto. Se l'utente decide di annullare le operazioni non completate, in genere facendo clic su un pulsante Annulla, la routine (nella sezione contrassegnata da **WM \_ Annulla**) chiama la funzione [**CancelSynchronousIo**](cancelsynchronousio-func.md) usando l'handle del thread restituito dalla funzione **CreateFileThread** . La funzione **CancelSynchronousIo** viene restituita immediatamente dopo il tentativo di annullamento. Infine, l'utente o l'applicazione può richiedere successivamente un'altra operazione che dipende dal fatto che le operazioni sui file siano state completate. In questo caso, la routine (nella sezione contrassegnata da **WM \_ PROCESSDATA**) verifica prima di tutto che le operazioni siano state completate e quindi esegue le operazioni di pulizia.

    **Nota**  In questo esempio, dal momento che l'annullamento potrebbe essersi verificato in qualsiasi punto della sequenza di operazioni, potrebbe essere necessario che il chiamante assicuri che lo stato sia coerente o almeno compreso prima di procedere.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[I/O sincrono e asincrono](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



