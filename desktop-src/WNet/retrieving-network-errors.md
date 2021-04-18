---
title: Recupero degli errori di rete
description: Le funzioni WNet restituiscono i codici di errore per la compatibilità con Windows per gruppi di lavoro. Ogni funzione WNet imposta anche il valore del codice di errore restituito da GetLastError.
ms.assetid: 8188304a-8ab3-4c43-a6d6-2806043cc195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436d63b51d0f57698403d206774710450eee1c8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300131"
---
# <a name="retrieving-network-errors"></a><span data-ttu-id="b0699-104">Recupero degli errori di rete</span><span class="sxs-lookup"><span data-stu-id="b0699-104">Retrieving Network Errors</span></span>

<span data-ttu-id="b0699-105">Le funzioni WNet restituiscono i codici di errore per la compatibilità con Windows per gruppi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b0699-105">The WNet functions return error codes for compatibility with Windows for Workgroups.</span></span> <span data-ttu-id="b0699-106">Ogni funzione WNet imposta anche il valore del codice di errore restituito da [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b0699-106">Each WNet function also sets the error code value returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="b0699-107">Quando una delle funzioni WNet restituisce un errore \_ esteso Error \_ , un'applicazione può chiamare la funzione [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) per recuperare informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="b0699-107">When one of the WNet functions returns ERROR\_EXTENDED\_ERROR, an application can call the [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) function to retrieve additional information about the error.</span></span> <span data-ttu-id="b0699-108">Queste informazioni sono in genere specifiche del provider di rete.</span><span class="sxs-lookup"><span data-stu-id="b0699-108">This information is usually specific to the network provider.</span></span>

<span data-ttu-id="b0699-109">Nell'esempio seguente viene illustrata una funzione di gestione degli errori definita dall'applicazione (NetErrorHandler).</span><span class="sxs-lookup"><span data-stu-id="b0699-109">The following example illustrates an application-defined error-handling function (NetErrorHandler).</span></span> <span data-ttu-id="b0699-110">La funzione accetta tre argomenti: un handle di finestra, il codice di errore restituito da una delle funzioni WNet e il nome della funzione che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="b0699-110">The function takes three arguments: a window handle, the error code returned by one of the WNet functions, and the name of the function that produced the error.</span></span> <span data-ttu-id="b0699-111">Se il codice di errore è Error \_ Extended Error \_ , NetErrorHandler chiama **WNetGetLastError** per ottenere informazioni estese sull'errore e stampa le informazioni.</span><span class="sxs-lookup"><span data-stu-id="b0699-111">If the error code is ERROR\_EXTENDED\_ERROR, NetErrorHandler calls **WNetGetLastError** to get extended error information and prints the information.</span></span> <span data-ttu-id="b0699-112">Nell'esempio viene chiamata la funzione [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) per elaborare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="b0699-112">The sample calls the [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) function to process messages.</span></span>


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



 

 