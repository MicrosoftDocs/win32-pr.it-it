---
description: Una transazione named pipe è una comunicazione client/server che combina un'operazione di scrittura e un'operazione di lettura in una singola operazione di rete. Le transazioni migliorano le prestazioni delle comunicazioni di rete tra un client e un server remoto.
ms.assetid: aedce207-7dea-4670-b6dd-0c61b3f6f690
title: Transazioni su named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 489039b92b65f57cefc71c5d78a01b1824b1418a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530109"
---
# <a name="transactions-on-named-pipes"></a><span data-ttu-id="5342b-104">Transazioni su named pipe</span><span class="sxs-lookup"><span data-stu-id="5342b-104">Transactions on Named Pipes</span></span>

<span data-ttu-id="5342b-105">Una transazione named pipe è una comunicazione client/server che combina un'operazione di scrittura e un'operazione di lettura in una singola operazione di rete.</span><span class="sxs-lookup"><span data-stu-id="5342b-105">A named pipe transaction is a client/server communication that combines a write operation and a read operation into a single network operation.</span></span> <span data-ttu-id="5342b-106">Una transazione può essere utilizzata solo su una pipe duplex di tipo messaggio.</span><span class="sxs-lookup"><span data-stu-id="5342b-106">A transaction can be used only on a duplex, message-type pipe.</span></span> <span data-ttu-id="5342b-107">Le transazioni migliorano le prestazioni delle comunicazioni di rete tra un client e un server remoto.</span><span class="sxs-lookup"><span data-stu-id="5342b-107">Transactions improve the performance of network communications between a client and a remote server.</span></span> <span data-ttu-id="5342b-108">I processi possono utilizzare le funzioni [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) e [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) per eseguire named pipe transazioni.</span><span class="sxs-lookup"><span data-stu-id="5342b-108">Processes can use the [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) and [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) functions to perform named pipe transactions.</span></span>

<span data-ttu-id="5342b-109">La funzione [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) viene usata più comunemente da un client pipe per scrivere un messaggio di richiesta nel server di named pipe e leggere il messaggio di risposta del server.</span><span class="sxs-lookup"><span data-stu-id="5342b-109">The [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) function is most commonly used by a pipe client to write a request message to the named pipe server and read the server's response message.</span></span> <span data-ttu-id="5342b-110">Il client pipe deve specificare l' \_ \| \_ accesso in scrittura generico di lettura generico quando apre il relativo handle di pipe chiamando la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="5342b-110">The pipe client must specify GENERIC\_READ \| GENERIC\_WRITE access when it opens its pipe handle by calling the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="5342b-111">Quindi, il client pipe imposta l'handle della pipe sulla modalità di lettura del messaggio chiamando la funzione [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) .</span><span class="sxs-lookup"><span data-stu-id="5342b-111">Then, the pipe client sets the pipe handle to message-read mode by calling the [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) function.</span></span> <span data-ttu-id="5342b-112">Se il buffer di lettura specificato nella chiamata a **TransactNamedPipe** non è sufficientemente grande da consentire l'inserimento dell'intero messaggio scritto dal server, la funzione restituisce zero e [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore di \_ altri \_ dati.</span><span class="sxs-lookup"><span data-stu-id="5342b-112">If the read buffer specified in the call to **TransactNamedPipe** is not large enough to hold the entire message written by the server, the function returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_MORE\_DATA.</span></span> <span data-ttu-id="5342b-113">Il client può leggere il resto del messaggio chiamando la funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)o [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) .</span><span class="sxs-lookup"><span data-stu-id="5342b-113">The client can read the remainder of the message by calling either the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex), or [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) function.</span></span>

<span data-ttu-id="5342b-114">[**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) viene in genere chiamato da client pipe, ma può anche essere usato da un server pipe.</span><span class="sxs-lookup"><span data-stu-id="5342b-114">[**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) is typically called by pipe clients, but can also be used by a pipe server.</span></span>

<span data-ttu-id="5342b-115">Nell'esempio seguente viene illustrato un client pipe che usa [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe).</span><span class="sxs-lookup"><span data-stu-id="5342b-115">The following example shows a pipe client using [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe).</span></span> <span data-ttu-id="5342b-116">Questo client pipe può essere usato con uno qualsiasi dei server pipe elencati in vedere anche.</span><span class="sxs-lookup"><span data-stu-id="5342b-116">This pipe client can be used with any of the pipe servers listed under See Also.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
   // Try to open a named pipe; wait for it, if necessary. 
    while (1) 
   { 
      hPipe = CreateFile( 
         lpszPipename,   // pipe name 
         GENERIC_READ |  // read and write access 
         GENERIC_WRITE, 
         0,              // no sharing 
         NULL,           // default security attributes
         OPEN_EXISTING,  // opens existing pipe 
         0,              // default attributes 
         NULL);          // no template file 
 
      // Break if the pipe handle is valid. 
      if (hPipe != INVALID_HANDLE_VALUE) 
         break; 
 
      // Exit if an error other than ERROR_PIPE_BUSY occurs. 
      if (GetLastError() != ERROR_PIPE_BUSY) 
      {
         printf("Could not open pipe\n"); 
         return 0;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
      if (! WaitNamedPipe(lpszPipename, 20000) ) 
      {
         printf("Could not open pipe\n"); 
         return 0;
      }
  } 
 
   // The pipe connected; change to message-read mode. 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if (!fSuccess) 
   {
      printf("SetNamedPipeHandleState failed.\n"); 
      return 0;
   }
 
   // Send a message to the pipe server and read the response. 
   fSuccess = TransactNamedPipe( 
      hPipe,                  // pipe handle 
      lpszWrite,              // message to server
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply
      BUFSIZE*sizeof(TCHAR),  // size of read buffer
      &cbRead,                // bytes read
      NULL);                  // not overlapped 

   if (!fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
   {
      printf("TransactNamedPipe failed.\n"); 
      return 0;
   }
 
   while(1)
   { 
      _tprintf(TEXT("%s\n"), chReadBuf);

      // Break if TransactNamedPipe or ReadFile is successful
      if(fSuccess)
         break;

      // Read from the pipe if there is more data in the message.
      fSuccess = ReadFile( 
         hPipe,      // pipe handle 
         chReadBuf,  // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 

      // Exit if an error other than ERROR_MORE_DATA occurs.
      if( !fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
         break;
      else _tprintf( TEXT("%s\n"), chReadBuf); 
   }

   _getch(); 

   CloseHandle(hPipe); 
 
   return 0; 
}
```



<span data-ttu-id="5342b-117">Un client pipe USA [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) per combinare le chiamate di funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (se necessario), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)e [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) in un'unica chiamata.</span><span class="sxs-lookup"><span data-stu-id="5342b-117">A pipe client uses [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) to combine the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (if necessary), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe), and [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function calls into a single call.</span></span> <span data-ttu-id="5342b-118">Poiché l'handle della pipe viene chiuso prima della restituzione della funzione, eventuali byte aggiuntivi nel messaggio andranno perduti se il messaggio supera la dimensione specificata del buffer di lettura.</span><span class="sxs-lookup"><span data-stu-id="5342b-118">Because the pipe handle is closed before the function returns, any additional bytes in the message are lost if the message is larger than the specified size of the read buffer.</span></span> <span data-ttu-id="5342b-119">L'esempio seguente è l'esempio precedente riscritto in modo da usare **CallNamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="5342b-119">The following example is the previous example rewritten to use **CallNamedPipe**.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
   fSuccess = CallNamedPipe( 
      lpszPipename,        // pipe name 
      lpszWrite,           // message to server 
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply 
      BUFSIZE*sizeof(TCHAR),  // size of read buffer 
      &cbRead,                // number of bytes read 
      20000);                 // waits for 20 seconds 
 
   if (fSuccess || GetLastError() == ERROR_MORE_DATA) 
   { 
      _tprintf( TEXT("%s\n"), chReadBuf ); 
    
      // The pipe is closed; no more data can be read. 
 
      if (! fSuccess) 
      {
         printf("\nExtra data in message was lost\n"); 
      }
   }
 
   _getch(); 

   return 0; 
}
```



## <a name="related-topics"></a><span data-ttu-id="5342b-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5342b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5342b-121">Server pipe multithreading</span><span class="sxs-lookup"><span data-stu-id="5342b-121">Multithreaded pipe server</span></span>](multithreaded-pipe-server.md)
</dt> <dt>

[<span data-ttu-id="5342b-122">Server named pipe con I/O sovrapposti</span><span class="sxs-lookup"><span data-stu-id="5342b-122">Named pipe server using overlapped I/O</span></span>](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[<span data-ttu-id="5342b-123">Server named pipe con routine di completamento</span><span class="sxs-lookup"><span data-stu-id="5342b-123">Named pipe server using completion routines</span></span>](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
