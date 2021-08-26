---
description: Una named pipe transazione è una comunicazione client/server che combina un'operazione di scrittura e un'operazione di lettura in una singola operazione di rete. Le transazioni migliorano le prestazioni delle comunicazioni di rete tra un client e un server remoto.
ms.assetid: aedce207-7dea-4670-b6dd-0c61b3f6f690
title: Transazioni in named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524f9ae453eb958efd59d8ef6ee5adfda12dd2701e4c719be51299e2873913dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963901"
---
# <a name="transactions-on-named-pipes"></a>Transazioni in named pipe

Una named pipe transazione è una comunicazione client/server che combina un'operazione di scrittura e un'operazione di lettura in una singola operazione di rete. Una transazione può essere usata solo su una pipe duplex di tipo messaggio. Le transazioni migliorano le prestazioni delle comunicazioni di rete tra un client e un server remoto. I processi possono usare le [**funzioni TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) e [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) per eseguire named pipe transazioni.

La [**funzione TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) viene in genere usata da un client pipe per scrivere un messaggio di richiesta nel server named pipe e leggere il messaggio di risposta del server. Il client pipe deve specificare l'accesso GENERIC READ GENERIC WRITE quando apre \_ l'handle della pipe chiamando la funzione \| \_ [**CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Il client pipe imposta quindi l'handle della pipe sulla modalità di lettura messaggi chiamando la [**funzione SetNamedPipeHandleState.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) Se il buffer di lettura specificato nella chiamata a **TransactNamedPipe** non è sufficientemente grande da contenere l'intero messaggio scritto dal server, la funzione restituisce zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ MORE \_ DATA. Il client può leggere il resto del messaggio chiamando la [**funzione ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)o [**PeekNamedPipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)

[**TransactNamedPipe viene**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) in genere chiamato dai client pipe, ma può essere usato anche da un server pipe.

Nell'esempio seguente viene illustrato un client pipe che [**usa TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe). Questo client pipe può essere usato con uno dei server pipe elencati in Vedere anche.


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



Un client pipe usa [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) per combinare le chiamate di funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (se necessario), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)e [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) in una singola chiamata. Poiché l'handle della pipe viene chiuso prima che la funzione restituisca , eventuali byte aggiuntivi nel messaggio vengono persi se il messaggio è maggiore delle dimensioni specificate del buffer di lettura. L'esempio seguente è l'esempio precedente riscritto per usare **CallNamedPipe**.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Server pipe multithreading](multithreaded-pipe-server.md)
</dt> <dt>

[Server named pipe con I/O sovrapposto](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[Server named pipe con routine di completamento](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
