---
description: Quando molte funzioni di sistema hanno esito negativo, impostano il codice dell'ultimo errore.
ms.assetid: 4cc626ac-7574-44ce-8377-e0bdd8e74b7e
title: Recupero del codice Last-Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28ba096fae2bd38bb8dc9c291a677aa6fa161d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049147"
---
# <a name="retrieving-the-last-error-code"></a><span data-ttu-id="a8cf7-103">Recupero del codice Last-Error</span><span class="sxs-lookup"><span data-stu-id="a8cf7-103">Retrieving the Last-Error Code</span></span>

<span data-ttu-id="a8cf7-104">Quando molte funzioni di sistema hanno esito negativo, impostano il codice dell'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-104">When many system functions fail, they set the last-error code.</span></span> <span data-ttu-id="a8cf7-105">Se per l'applicazione sono necessari ulteriori dettagli su un errore, è possibile recuperare il codice dell'ultimo errore utilizzando la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) e visualizzare una descrizione dell'errore utilizzando la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="a8cf7-105">If your application needs more details about an error, it can retrieve the last-error code using the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function and display a description of the error using the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function.</span></span>

<span data-ttu-id="a8cf7-106">Nell'esempio seguente viene inclusa una funzione di gestione degli errori che stampa il messaggio di errore e termina il processo.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-106">The following example includes an error-handling function that prints the error message and terminates the process.</span></span> <span data-ttu-id="a8cf7-107">Il parametro *lpszFunction* è il nome della funzione che ha impostato il codice dell'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-107">The *lpszFunction* parameter is the name of the function that set the last-error code.</span></span>


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



 

 
