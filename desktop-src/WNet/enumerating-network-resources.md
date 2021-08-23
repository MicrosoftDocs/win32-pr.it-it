---
title: Enumerazione delle risorse di rete
description: L'esempio seguente illustra una funzione definita dall'applicazione (EnumerateFunc) che enumera tutte le risorse in una rete.
ms.assetid: f5872ee7-483d-406a-b7d8-4ce93613fd29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633a8b03dd538853a0b339ee727c18fb05b2231b7690d89dea0a83264f7faf8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053330"
---
# <a name="enumerating-network-resources"></a>Enumerazione delle risorse di rete

L'esempio seguente illustra una funzione definita dall'applicazione (EnumerateFunc) che enumera tutte le risorse in una rete. L'esempio specifica **NULL** per il puntatore alla struttura [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) perché quando [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) riceve un **puntatore NULL,** recupera un handle per la radice della rete.

Per iniziare l'enumerazione di una risorsa contenitore di rete, l'applicazione deve seguire questa procedura:

1.  Passare l'indirizzo di [**una struttura NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) che rappresenta la risorsa alla [**funzione WNetOpenEnum.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)
2.  Allocare un buffer sufficientemente grande da contenere la matrice di strutture [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) restituita dalla [**funzione WNetEnumResource,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) oltre alle stringhe a cui puntano i membri.
3.  Passare l'handle di risorsa [**restituito da WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) alla [**funzione WNetEnumResource.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)
4.  Chiudere l'handle di risorsa quando non è più necessario chiamando la [**funzione WNetCloseEnum.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)

È possibile continuare a enumerare una risorsa contenitore descritta nella matrice di strutture [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) recuperate [**da WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea). Se il membro **dwUsage** della struttura **NETRESOURCE** è uguale a RESOURCEUSAGE CONTAINER, passare l'indirizzo della struttura alla funzione \_ [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) per aprire il contenitore e continuare l'enumerazione. Se **dwUsage** è uguale a RESOURCEUSAGE CONNECTABLE, l'applicazione può passare l'indirizzo della struttura alla funzione \_ [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) o alla funzione [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) per connettersi alla risorsa.

Prima di tutto, [**l'esempio chiama la funzione WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) per iniziare l'enumerazione. L'esempio chiama la [**funzione GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) per allocare il buffer richiesto e quindi chiama la [**funzione ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) per impostare il contenuto del buffer su zero. L'esempio chiama quindi la [**funzione WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) per continuare l'enumerazione. Ogni volta che il membro **dwUsage** di una struttura [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) recuperata da **WNetEnumResource** è uguale a RESOURCEUSAGE CONTAINER, la funzione EnumerateFunc chiama se stessa in modo ricorsivo e usa un puntatore a tale struttura nella chiamata \_ a **WNetOpenEnum**. Infine, l'esempio chiama [**la funzione GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) per liberare la memoria allocata e [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) per terminare l'enumerazione.


```C++
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "mpr.lib")

#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr);
void DisplayStruct(int i, LPNETRESOURCE lpnrLocal);

int main()
{

    LPNETRESOURCE lpnr = NULL;

    if (EnumerateFunc(lpnr) == FALSE) {
        printf("Call to EnumerateFunc failed\n");
        return 1;
    } else
        return 0;

}

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr)
{
    DWORD dwResult, dwResultEnum;
    HANDLE hEnum;
    DWORD cbBuffer = 16384;     // 16K is a good size
    DWORD cEntries = -1;        // enumerate all possible entries
    LPNETRESOURCE lpnrLocal;    // pointer to enumerated structures
    DWORD i;
    //
    // Call the WNetOpenEnum function to begin the enumeration.
    //
    dwResult = WNetOpenEnum(RESOURCE_GLOBALNET, // all network resources
                            RESOURCETYPE_ANY,   // all resources
                            0,  // enumerate all resources
                            lpnr,       // NULL first time the function is called
                            &hEnum);    // handle to the resource

    if (dwResult != NO_ERROR) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
        return FALSE;
    }
    //
    // Call the GlobalAlloc function to allocate resources.
    //
    lpnrLocal = (LPNETRESOURCE) GlobalAlloc(GPTR, cbBuffer);
    if (lpnrLocal == NULL) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
//      NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetOpenEnum");
        return FALSE;
    }

    do {
        //
        // Initialize the buffer.
        //
        ZeroMemory(lpnrLocal, cbBuffer);
        //
        // Call the WNetEnumResource function to continue
        //  the enumeration.
        //
        dwResultEnum = WNetEnumResource(hEnum,  // resource handle
                                        &cEntries,      // defined locally as -1
                                        lpnrLocal,      // LPNETRESOURCE
                                        &cbBuffer);     // buffer size
        //
        // If the call succeeds, loop through the structures.
        //
        if (dwResultEnum == NO_ERROR) {
            for (i = 0; i < cEntries; i++) {
                // Call an application-defined function to
                //  display the contents of the NETRESOURCE structures.
                //
                DisplayStruct(i, &lpnrLocal[i]);

                // If the NETRESOURCE structure represents a container resource, 
                //  call the EnumerateFunc function recursively.

                if (RESOURCEUSAGE_CONTAINER == (lpnrLocal[i].dwUsage
                                                & RESOURCEUSAGE_CONTAINER))
//          if(!EnumerateFunc(hwnd, hdc, &lpnrLocal[i]))
                    if (!EnumerateFunc(&lpnrLocal[i]))
                        printf("EnumerateFunc returned FALSE\n");
//            TextOut(hdc, 10, 10, "EnumerateFunc returned FALSE.", 29);
            }
        }
        // Process errors.
        //
        else if (dwResultEnum != ERROR_NO_MORE_ITEMS) {
            printf("WNetEnumResource failed with error %d\n", dwResultEnum);

//      NetErrorHandler(hwnd, dwResultEnum, (LPSTR)"WNetEnumResource");
            break;
        }
    }
    //
    // End do.
    //
    while (dwResultEnum != ERROR_NO_MORE_ITEMS);
    //
    // Call the GlobalFree function to free the memory.
    //
    GlobalFree((HGLOBAL) lpnrLocal);
    //
    // Call WNetCloseEnum to end the enumeration.
    //
    dwResult = WNetCloseEnum(hEnum);

    if (dwResult != NO_ERROR) {
        //
        // Process errors.
        //
        printf("WNetCloseEnum failed with error %d\n", dwResult);
//    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetCloseEnum");
        return FALSE;
    }

    return TRUE;
}

void DisplayStruct(int i, LPNETRESOURCE lpnrLocal)
{
    printf("NETRESOURCE[%d] Scope: ", i);
    switch (lpnrLocal->dwScope) {
    case (RESOURCE_CONNECTED):
        printf("connected\n");
        break;
    case (RESOURCE_GLOBALNET):
        printf("all resources\n");
        break;
    case (RESOURCE_REMEMBERED):
        printf("remembered\n");
        break;
    default:
        printf("unknown scope %d\n", lpnrLocal->dwScope);
        break;
    }

    printf("NETRESOURCE[%d] Type: ", i);
    switch (lpnrLocal->dwType) {
    case (RESOURCETYPE_ANY):
        printf("any\n");
        break;
    case (RESOURCETYPE_DISK):
        printf("disk\n");
        break;
    case (RESOURCETYPE_PRINT):
        printf("print\n");
        break;
    default:
        printf("unknown type %d\n", lpnrLocal->dwType);
        break;
    }

    printf("NETRESOURCE[%d] DisplayType: ", i);
    switch (lpnrLocal->dwDisplayType) {
    case (RESOURCEDISPLAYTYPE_GENERIC):
        printf("generic\n");
        break;
    case (RESOURCEDISPLAYTYPE_DOMAIN):
        printf("domain\n");
        break;
    case (RESOURCEDISPLAYTYPE_SERVER):
        printf("server\n");
        break;
    case (RESOURCEDISPLAYTYPE_SHARE):
        printf("share\n");
        break;
    case (RESOURCEDISPLAYTYPE_FILE):
        printf("file\n");
        break;
    case (RESOURCEDISPLAYTYPE_GROUP):
        printf("group\n");
        break;
    case (RESOURCEDISPLAYTYPE_NETWORK):
        printf("network\n");
        break;
    default:
        printf("unknown display type %d\n", lpnrLocal->dwDisplayType);
        break;
    }

    printf("NETRESOURCE[%d] Usage: 0x%x = ", i, lpnrLocal->dwUsage);
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONNECTABLE)
        printf("connectable ");
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONTAINER)
        printf("container ");
    printf("\n");

    printf("NETRESOURCE[%d] Localname: %S\n", i, lpnrLocal->lpLocalName);
    printf("NETRESOURCE[%d] Remotename: %S\n", i, lpnrLocal->lpRemoteName);
    printf("NETRESOURCE[%d] Comment: %S\n", i, lpnrLocal->lpComment);
    printf("NETRESOURCE[%d] Provider: %S\n", i, lpnrLocal->lpProvider);
    printf("\n");
}

```



Per altre informazioni sull'uso di un gestore degli errori definito dall'applicazione, vedere [Recupero di errori di rete](retrieving-network-errors.md).

 

 