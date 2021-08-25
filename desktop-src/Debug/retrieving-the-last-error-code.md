---
description: Quando molte funzioni di sistema hanno esito negativo, impostano il codice dell'ultimo errore.
ms.assetid: 4cc626ac-7574-44ce-8377-e0bdd8e74b7e
title: Recupero del codice Last-Error dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853fb6991bab5ad761dacaf18a2ec086dbf8fc4176964888bd0ededc548fbeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912451"
---
# <a name="retrieving-the-last-error-code"></a>Recupero del codice Last-Error dati

Quando molte funzioni di sistema hanno esito negativo, impostano il codice dell'ultimo errore. Se l'applicazione necessita di altri dettagli su un errore, può recuperare il codice dell'ultimo errore usando la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) e visualizzare una descrizione dell'errore usando la [**funzione FormatMessage.**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)

Nell'esempio seguente è inclusa una funzione di gestione degli errori che stampa il messaggio di errore e termina il processo. Il *parametro lpszFunction* è il nome della funzione che imposta il codice dell'ultimo errore.


```C++
#include <windows.h>
#include <strsafe.h>

void ErrorExit(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code

    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    // Display the error message and exit the process

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR)lpMsgBuf) + lstrlen((LPCTSTR)lpszFunction) + 40) * sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR)lpDisplayBuf, TEXT("Error"), MB_OK); 

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
    ExitProcess(dw); 
}

void main()
{
    // Generate an error

    if(!GetProcessId(NULL))
        ErrorExit(TEXT("GetProcessId"));
}
```



 

 
