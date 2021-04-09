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
# <a name="named-pipe-client"></a>Client named pipe

Un client named pipe utilizza la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un handle per un named pipe. Se la pipe esiste ma tutte le relative istanze sono occupate, **CreateFile** restituisce un **\_ \_ valore di handle non valido** e la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce la pipe degli errori \_ \_ occupata. Quando ciò si verifica, il client named pipe utilizza la funzione [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) per attendere che un'istanza del named pipe diventi disponibile.

La funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ha esito negativo se l'accesso specificato non è compatibile con l'accesso specificato (duplex, in uscita o in ingresso) quando il server ha creato la pipe. Per una pipe duplex, il client può specificare l'accesso in lettura, scrittura o lettura/scrittura; per una pipe in uscita (server di sola scrittura), il client deve specificare l'accesso in sola lettura. per una pipe in ingresso (server di sola lettura), il client deve specificare l'accesso in sola scrittura.

Per impostazione predefinita, l'handle restituito da [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) viene impostato sulla modalità di lettura byte, sulla modalità di attesa blocco, sulla modalità sovrapposta disabilitata e sulla modalità Write-through disabilitata. Il client pipe può utilizzare **CreateFile** per abilitare la modalità sovrapposta specificando il flag di file \_ \_ sovrapposto o abilitare la modalità Write-through specificando la scrittura del flag di file \_ \_ \_ . Il client può usare la funzione [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) per abilitare la modalità non di blocco SPECIFICAndo pipe \_ nowait o per abilitare la modalità di lettura del messaggio specificando pipe \_ READMODE \_ Message.

Nell'esempio seguente viene illustrato un client pipe che apre una named pipe, imposta l'handle della pipe sulla modalità di lettura del messaggio, usa la funzione [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) per inviare una richiesta al server e usa la funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) per leggere la risposta del server. Questo client pipe può essere utilizzato con qualsiasi server di tipo messaggio elencato nella parte inferiore di questo argomento. Con un server di tipo byte, tuttavia, questo client pipe ha esito negativo quando chiama [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) per passare alla modalità di lettura del messaggio. Poiché il client sta leggendo dalla pipe in modalità di lettura del messaggio, è possibile che l'operazione **ReadFile** restituisca zero dopo la lettura di un messaggio parziale. Ciò si verifica quando il messaggio è più grande del buffer di lettura. In questa situazione, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ più \_ dati e il client può leggere il resto del messaggio usando chiamate aggiuntive a **ReadFile**.

Questo client pipe può essere usato con uno qualsiasi dei server pipe elencati in vedere anche.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Server pipe multithreading](multithreaded-pipe-server.md)
</dt> <dt>

[Server named pipe con I/O sovrapposti](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[Server named pipe con routine di completamento](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
