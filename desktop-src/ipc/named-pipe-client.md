---
description: Nell'esempio di codice viene illustrato un client pipe che apre una named pipe, imposta l'handle della pipe sulla modalità di lettura del messaggio, utilizza la funzione WriteFile per inviare una richiesta al server e utilizza la funzione ReadFile per leggere la risposta dei server.
ms.assetid: 0779242c-45f4-4cd9-9c9f-36cff54c8dee
title: Client named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6318edd7d5b41c701e3112188a896c0529338805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878566"
---
# <a name="named-pipe-client"></a><span data-ttu-id="70168-103">Client named pipe</span><span class="sxs-lookup"><span data-stu-id="70168-103">Named Pipe Client</span></span>

<span data-ttu-id="70168-104">Un client named pipe utilizza la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un handle per un named pipe.</span><span class="sxs-lookup"><span data-stu-id="70168-104">A named pipe client uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a named pipe.</span></span> <span data-ttu-id="70168-105">Se la pipe esiste ma tutte le relative istanze sono occupate, **CreateFile** restituisce un **\_ \_ valore di handle non valido** e la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce la pipe degli errori \_ \_ occupata.</span><span class="sxs-lookup"><span data-stu-id="70168-105">If the pipe exists but all of its instances are busy, **CreateFile** returns **INVALID\_HANDLE\_VALUE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_PIPE\_BUSY.</span></span> <span data-ttu-id="70168-106">Quando ciò si verifica, il client named pipe utilizza la funzione [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) per attendere che un'istanza del named pipe diventi disponibile.</span><span class="sxs-lookup"><span data-stu-id="70168-106">When this happens, the named pipe client uses the [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) function to wait for an instance of the named pipe to become available.</span></span>

<span data-ttu-id="70168-107">La funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ha esito negativo se l'accesso specificato non è compatibile con l'accesso specificato (duplex, in uscita o in ingresso) quando il server ha creato la pipe.</span><span class="sxs-lookup"><span data-stu-id="70168-107">The [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function fails if the access specified is incompatible with the access specified (duplex, outbound, or inbound) when the server created the pipe.</span></span> <span data-ttu-id="70168-108">Per una pipe duplex, il client può specificare l'accesso in lettura, scrittura o lettura/scrittura; per una pipe in uscita (server di sola scrittura), il client deve specificare l'accesso in sola lettura. per una pipe in ingresso (server di sola lettura), il client deve specificare l'accesso in sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="70168-108">For a duplex pipe, the client can specify read, write, or read/write access; for an outbound pipe (write-only server), the client must specify read-only access; and for an inbound pipe (read-only server), the client must specify write-only access.</span></span>

<span data-ttu-id="70168-109">Per impostazione predefinita, l'handle restituito da [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) viene impostato sulla modalità di lettura byte, sulla modalità di attesa blocco, sulla modalità sovrapposta disabilitata e sulla modalità Write-through disabilitata.</span><span class="sxs-lookup"><span data-stu-id="70168-109">The handle returned by [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) defaults to byte-read mode, blocking-wait mode, overlapped mode disabled, and write-through mode disabled.</span></span> <span data-ttu-id="70168-110">Il client pipe può utilizzare **CreateFile** per abilitare la modalità sovrapposta specificando il flag di file \_ \_ sovrapposto o abilitare la modalità Write-through specificando la scrittura del flag di file \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="70168-110">The pipe client can use **CreateFile** to enable overlapped mode by specifying FILE\_FLAG\_OVERLAPPED or to enable write-through mode by specifying FILE\_FLAG\_WRITE\_THROUGH.</span></span> <span data-ttu-id="70168-111">Il client può usare la funzione [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) per abilitare la modalità non di blocco SPECIFICAndo pipe \_ nowait o per abilitare la modalità di lettura del messaggio specificando pipe \_ READMODE \_ Message.</span><span class="sxs-lookup"><span data-stu-id="70168-111">The client can use the [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) function to enable nonblocking mode by specifying PIPE\_NOWAIT or to enable message-read mode by specifying PIPE\_READMODE\_MESSAGE.</span></span>

<span data-ttu-id="70168-112">Nell'esempio seguente viene illustrato un client pipe che apre una named pipe, imposta l'handle della pipe sulla modalità di lettura del messaggio, usa la funzione [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) per inviare una richiesta al server e usa la funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) per leggere la risposta del server.</span><span class="sxs-lookup"><span data-stu-id="70168-112">The following example shows a pipe client that opens a named pipe, sets the pipe handle to message-read mode, uses the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to send a request to the server, and uses the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function to read the server's reply.</span></span> <span data-ttu-id="70168-113">Questo client pipe può essere utilizzato con qualsiasi server di tipo messaggio elencato nella parte inferiore di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="70168-113">This pipe client can be used with any of the message-type servers listed at the bottom of this topic.</span></span> <span data-ttu-id="70168-114">Con un server di tipo byte, tuttavia, questo client pipe ha esito negativo quando chiama [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) per passare alla modalità di lettura del messaggio.</span><span class="sxs-lookup"><span data-stu-id="70168-114">With a byte-type server, however, this pipe client fails when it calls [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) to change to message-read mode.</span></span> <span data-ttu-id="70168-115">Poiché il client sta leggendo dalla pipe in modalità di lettura del messaggio, è possibile che l'operazione **ReadFile** restituisca zero dopo la lettura di un messaggio parziale.</span><span class="sxs-lookup"><span data-stu-id="70168-115">Because the client is reading from the pipe in message-read mode, it is possible for the **ReadFile** operation to return zero after reading a partial message.</span></span> <span data-ttu-id="70168-116">Ciò si verifica quando il messaggio è più grande del buffer di lettura.</span><span class="sxs-lookup"><span data-stu-id="70168-116">This happens when the message is larger than the read buffer.</span></span> <span data-ttu-id="70168-117">In questa situazione, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ più \_ dati e il client può leggere il resto del messaggio usando chiamate aggiuntive a **ReadFile**.</span><span class="sxs-lookup"><span data-stu-id="70168-117">In this situation, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_MORE\_DATA, and the client can read the remainder of the message using additional calls to **ReadFile**.</span></span>

<span data-ttu-id="70168-118">Questo client pipe può essere usato con uno qualsiasi dei server pipe elencati in vedere anche.</span><span class="sxs-lookup"><span data-stu-id="70168-118">This pipe client can be used with any of the pipe servers listed under See Also.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpvMessage=TEXT("Default message from client."); 
   TCHAR  chBuf[BUFSIZE]; 
   BOOL   fSuccess = FALSE; 
   DWORD  cbRead, cbToWrite, cbWritten, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1 )
      lpvMessage = argv[1];
 
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
         _tprintf( TEXT("Could not open pipe. GLE=%d\n"), GetLastError() ); 
         return -1;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
 
      if ( ! WaitNamedPipe(lpszPipename, 20000)) 
      { 
         printf("Could not open pipe: 20 second wait timed out."); 
         return -1;
      } 
   } 
 
// The pipe connected; change to message-read mode. 
 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if ( ! fSuccess) 
   {
      _tprintf( TEXT("SetNamedPipeHandleState failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }
 
// Send a message to the pipe server. 
 
   cbToWrite = (lstrlen(lpvMessage)+1)*sizeof(TCHAR);
   _tprintf( TEXT("Sending %d byte message: \"%s\"\n"), cbToWrite, lpvMessage); 

   fSuccess = WriteFile( 
      hPipe,                  // pipe handle 
      lpvMessage,             // message 
      cbToWrite,              // message length 
      &cbWritten,             // bytes written 
      NULL);                  // not overlapped 

   if ( ! fSuccess) 
   {
      _tprintf( TEXT("WriteFile to pipe failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }

   printf("\nMessage sent to server, receiving reply as follows:\n");
 
   do 
   { 
   // Read from the pipe. 
 
      fSuccess = ReadFile( 
         hPipe,    // pipe handle 
         chBuf,    // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 
 
      if ( ! fSuccess && GetLastError() != ERROR_MORE_DATA )
         break; 
 
      _tprintf( TEXT("\"%s\"\n"), chBuf ); 
   } while ( ! fSuccess);  // repeat loop if ERROR_MORE_DATA 

   if ( ! fSuccess)
   {
      _tprintf( TEXT("ReadFile from pipe failed. GLE=%d\n"), GetLastError() );
      return -1;
   }

   printf("\n<End of message, press ENTER to terminate connection and exit>");
   _getch();
 
   CloseHandle(hPipe); 
 
   return 0; 
}
```



## <a name="related-topics"></a><span data-ttu-id="70168-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70168-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70168-120">Server pipe multithreading</span><span class="sxs-lookup"><span data-stu-id="70168-120">Multithreaded pipe server</span></span>](multithreaded-pipe-server.md)
</dt> <dt>

[<span data-ttu-id="70168-121">Server named pipe con I/O sovrapposti</span><span class="sxs-lookup"><span data-stu-id="70168-121">Named pipe server using overlapped I/O</span></span>](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[<span data-ttu-id="70168-122">Server named pipe con routine di completamento</span><span class="sxs-lookup"><span data-stu-id="70168-122">Named pipe server using completion routines</span></span>](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
