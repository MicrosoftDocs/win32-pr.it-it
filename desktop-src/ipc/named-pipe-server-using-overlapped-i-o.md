---
description: Esempio di codice di un server pipe a thread singolo che usa operazioni sovrapposte per il servizio di connessioni simultanee a più client pipe.
ms.assetid: c0ac70cc-4ab9-47e5-b0e6-c0b373d16b25
title: Server named pipe con I/O sovrapposti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f9134582a50c2053893cf6ee4908e447e3cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967641"
---
# <a name="named-pipe-server-using-overlapped-io"></a><span data-ttu-id="b0f11-103">Server named pipe con I/O sovrapposti</span><span class="sxs-lookup"><span data-stu-id="b0f11-103">Named Pipe Server Using Overlapped I/O</span></span>

<span data-ttu-id="b0f11-104">Di seguito è riportato un esempio di un server pipe a thread singolo che utilizza operazioni sovrapposte per il servizio di connessioni simultanee a più client pipe.</span><span class="sxs-lookup"><span data-stu-id="b0f11-104">The following is an example of a single-threaded pipe server that uses overlapped operations to service simultaneous connections to multiple pipe clients.</span></span> <span data-ttu-id="b0f11-105">Il server pipe crea un numero fisso di istanze di pipe.</span><span class="sxs-lookup"><span data-stu-id="b0f11-105">The pipe server creates a fixed number of pipe instances.</span></span> <span data-ttu-id="b0f11-106">Ogni istanza di pipe può essere connessa a un client di pipe separato.</span><span class="sxs-lookup"><span data-stu-id="b0f11-106">Each pipe instance can be connected to a separate pipe client.</span></span> <span data-ttu-id="b0f11-107">Quando un client pipe ha terminato di utilizzare l'istanza di pipe, il server si disconnette dal client e riutilizza l'istanza della pipe per connettersi a un nuovo client.</span><span class="sxs-lookup"><span data-stu-id="b0f11-107">When a pipe client has finished using its pipe instance, the server disconnects from the client and reuses the pipe instance to connect to a new client.</span></span> <span data-ttu-id="b0f11-108">Questo server pipe può essere utilizzato con il client pipe descritto nel [client named pipe](named-pipe-client.md).</span><span class="sxs-lookup"><span data-stu-id="b0f11-108">This pipe server can be used with the pipe client described in [Named Pipe Client](named-pipe-client.md).</span></span>

<span data-ttu-id="b0f11-109">La struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) viene specificata come parametro in ogni operazione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) sull'istanza della pipe.</span><span class="sxs-lookup"><span data-stu-id="b0f11-109">The [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure is specified as a parameter in each [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operation on the pipe instance.</span></span> <span data-ttu-id="b0f11-110">Sebbene l'esempio mostri operazioni simultanee su istanze di pipe diverse, evita le operazioni simultanee su una singola istanza di pipe usando l'oggetto evento nella struttura **sovrapposta** .</span><span class="sxs-lookup"><span data-stu-id="b0f11-110">Although the example shows simultaneous operations on different pipe instances, it avoids simultaneous operations on a single pipe instance by using the event object in the **OVERLAPPED** structure.</span></span> <span data-ttu-id="b0f11-111">Poiché lo stesso oggetto evento viene usato per le operazioni di lettura, scrittura e connessione per ogni istanza, non esiste alcun modo per individuare il completamento dell'operazione che ha causato l'impostazione dell'evento sullo stato segnalato per le operazioni simultanee usando la stessa istanza di pipe.</span><span class="sxs-lookup"><span data-stu-id="b0f11-111">Because the same event object is used for read, write, and connect operations for each instance, there is no way to know which operation's completion caused the event to be set to the signaled state for simultaneous operations using the same pipe instance.</span></span>

<span data-ttu-id="b0f11-112">Gli handle di evento per ogni istanza di pipe vengono archiviati in una matrice passata alla funzione [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) .</span><span class="sxs-lookup"><span data-stu-id="b0f11-112">The event handles for each pipe instance are stored in an array that is passed to the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function.</span></span> <span data-ttu-id="b0f11-113">Questa funzione attende che uno degli eventi venga segnalato e restituisce l'indice della matrice dell'evento che ha causato il completamento dell'operazione di attesa.</span><span class="sxs-lookup"><span data-stu-id="b0f11-113">This function waits for one of the events to be signaled, and returns the array index of the event that caused the wait operation to complete.</span></span> <span data-ttu-id="b0f11-114">Nell'esempio riportato in questo argomento viene utilizzato questo indice di matrice per recuperare una struttura contenente informazioni per l'istanza di pipe.</span><span class="sxs-lookup"><span data-stu-id="b0f11-114">The example in this topic uses this array index to retrieve a structure containing information for the pipe instance.</span></span> <span data-ttu-id="b0f11-115">Il server utilizza il membro **fPendingIO** della struttura per tenere traccia della presenza dell'operazione di i/O più recente sull'istanza in sospeso, che richiede una chiamata alla funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="b0f11-115">The server uses the **fPendingIO** member of the structure to keep track of whether the most recent I/O operation on the instance was pending, which requires a call to the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="b0f11-116">Il server utilizza il membro **dwState** della struttura per determinare l'operazione successiva da eseguire per l'istanza della pipe.</span><span class="sxs-lookup"><span data-stu-id="b0f11-116">The server uses the **dwState** member of the structure to determine the next operation that must be performed for the pipe instance.</span></span>

<span data-ttu-id="b0f11-117">Le operazioni [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) sovrapposte possono terminare nel momento in cui la funzione restituisce.</span><span class="sxs-lookup"><span data-stu-id="b0f11-117">Overlapped [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operations can finish by the time the function returns.</span></span> <span data-ttu-id="b0f11-118">In caso contrario, se l'operazione è in sospeso, l'oggetto evento nella struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) specificata viene impostato sullo stato non segnalato prima che la funzione restituisca.</span><span class="sxs-lookup"><span data-stu-id="b0f11-118">Otherwise, if the operation is pending, the event object in the specified [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure is set to the nonsignaled state before the function returns.</span></span> <span data-ttu-id="b0f11-119">Al termine dell'operazione in sospeso, il sistema imposta lo stato dell'oggetto evento su segnalato.</span><span class="sxs-lookup"><span data-stu-id="b0f11-119">When the pending operation finishes, the system sets the state of the event object to signaled.</span></span> <span data-ttu-id="b0f11-120">Lo stato dell'oggetto evento non viene modificato se l'operazione viene completata prima che la funzione restituisca.</span><span class="sxs-lookup"><span data-stu-id="b0f11-120">The state of the event object is not changed if the operation finishes before the function returns.</span></span>

<span data-ttu-id="b0f11-121">Poiché nell'esempio vengono utilizzati oggetti evento di reimpostazione manuale, lo stato di un oggetto evento non viene modificato in non segnalato dalla funzione [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) .</span><span class="sxs-lookup"><span data-stu-id="b0f11-121">Because the example uses manual-reset event objects, the state of an event object is not changed to nonsignaled by the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function.</span></span> <span data-ttu-id="b0f11-122">Questo è importante, poiché l'esempio si basa sugli oggetti evento rimanenti nello stato segnalato, tranne quando è presente un'operazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="b0f11-122">This is important, because the example relies on the event objects remaining in the signaled state, except when there is a pending operation.</span></span>

<span data-ttu-id="b0f11-123">Se l'operazione è già terminata quando [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)o [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) restituisce, il valore restituito della funzione indica il risultato.</span><span class="sxs-lookup"><span data-stu-id="b0f11-123">If the operation has already finished when [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), or [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) returns, the function's return value indicates the result.</span></span> <span data-ttu-id="b0f11-124">Per le operazioni di lettura e scrittura, viene restituito anche il numero di byte trasferiti.</span><span class="sxs-lookup"><span data-stu-id="b0f11-124">For read and write operations, the number of bytes transferred is also returned.</span></span> <span data-ttu-id="b0f11-125">Se l'operazione è ancora in sospeso, la funzione **ReadFile**, **WriteFile** o **ConnectNamedPipe** restituisce zero e la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ io \_ in sospeso.</span><span class="sxs-lookup"><span data-stu-id="b0f11-125">If the operation is still pending, the **ReadFile**, **WriteFile**, or **ConnectNamedPipe** function returns zero and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_IO\_PENDING.</span></span> <span data-ttu-id="b0f11-126">In questo caso, usare la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per recuperare i risultati al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b0f11-126">In this case, use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to retrieve the results after the operation has finished.</span></span> <span data-ttu-id="b0f11-127">**GetOverlappedResult** restituisce solo i risultati delle operazioni in sospeso.</span><span class="sxs-lookup"><span data-stu-id="b0f11-127">**GetOverlappedResult** returns only the results of pending operations.</span></span> <span data-ttu-id="b0f11-128">Non vengono segnalati i risultati delle operazioni completate prima della funzione **ReadFile**, **WriteFile** o **ConnectNamedPipe** sovrapposta.</span><span class="sxs-lookup"><span data-stu-id="b0f11-128">It does not report the results of operations that were completed before the overlapped **ReadFile**, **WriteFile**, or **ConnectNamedPipe** function returned.</span></span>

<span data-ttu-id="b0f11-129">Prima di eseguire la disconnessione da un client, è necessario attendere un segnale indicante che il client è terminato.</span><span class="sxs-lookup"><span data-stu-id="b0f11-129">Before disconnecting from a client, you must wait for a signal indicating the client has finished.</span></span> <span data-ttu-id="b0f11-130">(Lo svuotamento dei buffer di file comporta la sconfitta dello scopo dell'I/O sovrapposto, perché l'operazione di svuotamento blocca l'esecuzione del thread del server mentre attende che il client Svuoti la pipe.) In questo esempio, il segnale è l'errore generato tentando di leggere dalla pipe dopo che il client pipe ha chiuso il relativo handle.</span><span class="sxs-lookup"><span data-stu-id="b0f11-130">(Flushing the file buffers would defeat the purpose of overlapped I/O, because the flush operation would block the execution of the server thread while it waits for the client to empty the pipe.) In this example, the signal is the error generated by trying to read from the pipe after the pipe client closes its handle.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>
 
#define CONNECTING_STATE 0 
#define READING_STATE 1 
#define WRITING_STATE 2 
#define INSTANCES 4 
#define PIPE_TIMEOUT 5000
#define BUFSIZE 4096
 
typedef struct 
{ 
   OVERLAPPED oOverlap; 
   HANDLE hPipeInst; 
   TCHAR chRequest[BUFSIZE]; 
   DWORD cbRead;
   TCHAR chReply[BUFSIZE];
   DWORD cbToWrite; 
   DWORD dwState; 
   BOOL fPendingIO; 
} PIPEINST, *LPPIPEINST; 
 
 
VOID DisconnectAndReconnect(DWORD); 
BOOL ConnectToNewClient(HANDLE, LPOVERLAPPED); 
VOID GetAnswerToRequest(LPPIPEINST); 
 
PIPEINST Pipe[INSTANCES]; 
HANDLE hEvents[INSTANCES]; 
 
int _tmain(VOID) 
{ 
   DWORD i, dwWait, cbRet, dwErr; 
   BOOL fSuccess; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 
 
// The initial loop creates several instances of a named pipe 
// along with an event object for each instance.  An 
// overlapped ConnectNamedPipe operation is started for 
// each instance. 
 
   for (i = 0; i < INSTANCES; i++) 
   { 
 
   // Create an event object for this instance. 
 
      hEvents[i] = CreateEvent( 
         NULL,    // default security attribute 
         TRUE,    // manual-reset event 
         TRUE,    // initial state = signaled 
         NULL);   // unnamed event object 

      if (hEvents[i] == NULL) 
      {
         printf("CreateEvent failed with %d.\n", GetLastError()); 
         return 0;
      }
 
      Pipe[i].oOverlap.hEvent = hEvents[i]; 
 
      Pipe[i].hPipeInst = CreateNamedPipe( 
         lpszPipename,            // pipe name 
         PIPE_ACCESS_DUPLEX |     // read/write access 
         FILE_FLAG_OVERLAPPED,    // overlapped mode 
         PIPE_TYPE_MESSAGE |      // message-type pipe 
         PIPE_READMODE_MESSAGE |  // message-read mode 
         PIPE_WAIT,               // blocking mode 
         INSTANCES,               // number of instances 
         BUFSIZE*sizeof(TCHAR),   // output buffer size 
         BUFSIZE*sizeof(TCHAR),   // input buffer size 
         PIPE_TIMEOUT,            // client time-out 
         NULL);                   // default security attributes 

      if (Pipe[i].hPipeInst == INVALID_HANDLE_VALUE) 
      {
         printf("CreateNamedPipe failed with %d.\n", GetLastError());
         return 0;
      }
 
   // Call the subroutine to connect to the new client
 
      Pipe[i].fPendingIO = ConnectToNewClient( 
         Pipe[i].hPipeInst, 
         &Pipe[i].oOverlap); 
 
      Pipe[i].dwState = Pipe[i].fPendingIO ? 
         CONNECTING_STATE : // still connecting 
         READING_STATE;     // ready to read 
   } 
 
   while (1) 
   { 
   // Wait for the event object to be signaled, indicating 
   // completion of an overlapped read, write, or 
   // connect operation. 
 
      dwWait = WaitForMultipleObjects( 
         INSTANCES,    // number of event objects 
         hEvents,      // array of event objects 
         FALSE,        // does not wait for all 
         INFINITE);    // waits indefinitely 
 
   // dwWait shows which pipe completed the operation. 
 
      i = dwWait - WAIT_OBJECT_0;  // determines which pipe 
      if (i < 0 || i > (INSTANCES - 1)) 
      {
         printf("Index out of range.\n"); 
         return 0;
      }
 
   // Get the result if the operation was pending. 
 
      if (Pipe[i].fPendingIO) 
      { 
         fSuccess = GetOverlappedResult( 
            Pipe[i].hPipeInst, // handle to pipe 
            &Pipe[i].oOverlap, // OVERLAPPED structure 
            &cbRet,            // bytes transferred 
            FALSE);            // do not wait 
 
         switch (Pipe[i].dwState) 
         { 
         // Pending connect operation 
            case CONNECTING_STATE: 
               if (! fSuccess) 
               {
                   printf("Error %d.\n", GetLastError()); 
                   return 0;
               }
               Pipe[i].dwState = READING_STATE; 
               break; 
 
         // Pending read operation 
            case READING_STATE: 
               if (! fSuccess || cbRet == 0) 
               { 
                  DisconnectAndReconnect(i); 
                  continue; 
               }
               Pipe[i].cbRead = cbRet;
               Pipe[i].dwState = WRITING_STATE; 
               break; 
 
         // Pending write operation 
            case WRITING_STATE: 
               if (! fSuccess || cbRet != Pipe[i].cbToWrite) 
               { 
                  DisconnectAndReconnect(i); 
                  continue; 
               } 
               Pipe[i].dwState = READING_STATE; 
               break; 
 
            default: 
            {
               printf("Invalid pipe state.\n"); 
               return 0;
            }
         }  
      } 
 
   // The pipe state determines which operation to do next. 
 
      switch (Pipe[i].dwState) 
      { 
      // READING_STATE: 
      // The pipe instance is connected to the client 
      // and is ready to read a request from the client. 
 
         case READING_STATE: 
            fSuccess = ReadFile( 
               Pipe[i].hPipeInst, 
               Pipe[i].chRequest, 
               BUFSIZE*sizeof(TCHAR), 
               &Pipe[i].cbRead, 
               &Pipe[i].oOverlap); 
 
         // The read operation completed successfully. 
 
            if (fSuccess && Pipe[i].cbRead != 0) 
            { 
               Pipe[i].fPendingIO = FALSE; 
               Pipe[i].dwState = WRITING_STATE; 
               continue; 
            } 
 
         // The read operation is still pending. 
 
            dwErr = GetLastError(); 
            if (! fSuccess && (dwErr == ERROR_IO_PENDING)) 
            { 
               Pipe[i].fPendingIO = TRUE; 
               continue; 
            } 
 
         // An error occurred; disconnect from the client. 
 
            DisconnectAndReconnect(i); 
            break; 
 
      // WRITING_STATE: 
      // The request was successfully read from the client. 
      // Get the reply data and write it to the client. 
 
         case WRITING_STATE: 
            GetAnswerToRequest(&Pipe[i]); 
 
            fSuccess = WriteFile( 
               Pipe[i].hPipeInst, 
               Pipe[i].chReply, 
               Pipe[i].cbToWrite, 
               &cbRet, 
               &Pipe[i].oOverlap); 
 
         // The write operation completed successfully. 
 
            if (fSuccess && cbRet == Pipe[i].cbToWrite) 
            { 
               Pipe[i].fPendingIO = FALSE; 
               Pipe[i].dwState = READING_STATE; 
               continue; 
            } 
 
         // The write operation is still pending. 
 
            dwErr = GetLastError(); 
            if (! fSuccess && (dwErr == ERROR_IO_PENDING)) 
            { 
               Pipe[i].fPendingIO = TRUE; 
               continue; 
            } 
 
         // An error occurred; disconnect from the client. 
 
            DisconnectAndReconnect(i); 
            break; 
 
         default: 
         {
            printf("Invalid pipe state.\n"); 
            return 0;
         }
      } 
  } 
 
  return 0; 
} 
 
 
// DisconnectAndReconnect(DWORD) 
// This function is called when an error occurs or when the client 
// closes its handle to the pipe. Disconnect from this client, then 
// call ConnectNamedPipe to wait for another client to connect. 
 
VOID DisconnectAndReconnect(DWORD i) 
{ 
// Disconnect the pipe instance. 
 
   if (! DisconnectNamedPipe(Pipe[i].hPipeInst) ) 
   {
      printf("DisconnectNamedPipe failed with %d.\n", GetLastError());
   }
 
// Call a subroutine to connect to the new client. 
 
   Pipe[i].fPendingIO = ConnectToNewClient( 
      Pipe[i].hPipeInst, 
      &Pipe[i].oOverlap); 
 
   Pipe[i].dwState = Pipe[i].fPendingIO ? 
      CONNECTING_STATE : // still connecting 
      READING_STATE;     // ready to read 
} 
 
// ConnectToNewClient(HANDLE, LPOVERLAPPED) 
// This function is called to start an overlapped connect operation. 
// It returns TRUE if an operation is pending or FALSE if the 
// connection has been completed. 
 
BOOL ConnectToNewClient(HANDLE hPipe, LPOVERLAPPED lpo) 
{ 
   BOOL fConnected, fPendingIO = FALSE; 
 
// Start an overlapped connection for this pipe instance. 
   fConnected = ConnectNamedPipe(hPipe, lpo); 
 
// Overlapped ConnectNamedPipe should return zero. 
   if (fConnected) 
   {
      printf("ConnectNamedPipe failed with %d.\n", GetLastError()); 
      return 0;
   }
 
   switch (GetLastError()) 
   { 
   // The overlapped connection in progress. 
      case ERROR_IO_PENDING: 
         fPendingIO = TRUE; 
         break; 
 
   // Client is already connected, so signal an event. 
 
      case ERROR_PIPE_CONNECTED: 
         if (SetEvent(lpo->hEvent)) 
            break; 
 
   // If an error occurs during the connect operation... 
      default: 
      {
         printf("ConnectNamedPipe failed with %d.\n", GetLastError());
         return 0;
      }
   } 
 
   return fPendingIO; 
}

VOID GetAnswerToRequest(LPPIPEINST pipe)
{
   _tprintf( TEXT("[%d] %s\n"), pipe->hPipeInst, pipe->chRequest);
   StringCchCopy( pipe->chReply, BUFSIZE, TEXT("Default answer from server") );
   pipe->cbToWrite = (lstrlen(pipe->chReply)+1)*sizeof(TCHAR);
}

```



## <a name="related-topics"></a><span data-ttu-id="b0f11-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0f11-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0f11-132">Client named pipe</span><span class="sxs-lookup"><span data-stu-id="b0f11-132">Named Pipe Client</span></span>](named-pipe-client.md)
</dt> </dl>

 

 
