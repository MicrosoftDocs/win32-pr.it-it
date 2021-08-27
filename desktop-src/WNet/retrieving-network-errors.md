---
title: Recupero degli errori di rete
description: Le funzioni WNet restituiscono codici di errore per la compatibilità con Windows per i gruppi di lavoro. Ogni funzione WNet imposta anche il valore del codice di errore restituito da GetLastError.
ms.assetid: 8188304a-8ab3-4c43-a6d6-2806043cc195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92f02a05ab93d50b9c448ae280e5de7ddbed1260cf1df8b8b3e56aa33aaeff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072021"
---
# <a name="retrieving-network-errors"></a>Recupero degli errori di rete

Le funzioni WNet restituiscono codici di errore per la compatibilità con Windows per i gruppi di lavoro. Ogni funzione WNet imposta anche il valore del codice di errore [**restituito da GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Quando una delle funzioni WNet restituisce ERROR EXTENDED ERROR, un'applicazione può chiamare la funzione \_ \_ [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) per recuperare informazioni aggiuntive sull'errore. Queste informazioni sono in genere specifiche del provider di rete.

L'esempio seguente illustra una funzione di gestione degli errori definita dall'applicazione (NetErrorHandler). La funzione accetta tre argomenti: un handle di finestra, il codice di errore restituito da una delle funzioni WNet e il nome della funzione che ha generato l'errore. Se il codice di errore è ERROR \_ EXTENDED \_ ERROR, NetErrorHandler chiama **WNetGetLastError per** ottenere informazioni estese sull'errore e stampa le informazioni. L'esempio chiama la [**funzione MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) per elaborare i messaggi.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")
#pragma comment(lib, "user32.lib")

BOOL WINAPI NetErrorHandler(HWND hwnd, 
                            DWORD dwErrorCode, 
                            LPSTR lpszFunction) 
{ 
    DWORD dwWNetResult, dwLastError; 
    CHAR szError[256]; 
    CHAR szCaption[256]; 
    CHAR szDescription[256]; 
    CHAR szProvider[256]; 
 
    // The following code performs standard error-handling. 
 
    if (dwErrorCode != ERROR_EXTENDED_ERROR) 
    { 
        sprintf_s((LPSTR) szError, sizeof(szError), "%s failed; \nResult is %ld", 
            lpszFunction, dwErrorCode); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
 
    // The following code performs error-handling when the 
    //  ERROR_EXTENDED_ERROR return value indicates that the 
    //  WNetGetLastError function can retrieve additional information.
 
    else 
    { 
        dwWNetResult = WNetGetLastError(&dwLastError, // error code
            (LPSTR) szDescription,  // buffer for error description 
            sizeof(szDescription),  // size of error buffer
            (LPSTR) szProvider,     // buffer for provider name 
            sizeof(szProvider));    // size of name buffer
 
        //
        // Process errors.
        //
        if(dwWNetResult != NO_ERROR) { 
            sprintf_s((LPSTR) szError, sizeof(szError), 
                "WNetGetLastError failed; error %ld", dwWNetResult); 
            MessageBox(hwnd, (LPSTR) szError, "WNetGetLastError", MB_OK); 
            return FALSE; 
        } 
 
        //
        // Otherwise, print the additional error information.
        //
        sprintf_s((LPSTR) szError, sizeof(szError), 
            "%s failed with code %ld;\n%s", 
            (LPSTR) szProvider, dwLastError, (LPSTR) szDescription); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
}
```



 

 