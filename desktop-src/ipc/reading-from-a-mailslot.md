---
description: Come leggere da un inserimento/espulsione. Il processo che crea un inserimento/espulsione può leggere i messaggi tramite l'handle inserimento/espulsione in una chiamata alla funzione ReadFile.
ms.assetid: e193dca9-3b77-4e41-be6d-90992e1a8fe3
title: Lettura da un inserimento/espulsione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35458f90ca381689275417e0e525c2d5a31ac9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305704"
---
# <a name="reading-from-a-mailslot"></a>Lettura da un inserimento/espulsione

Il processo che crea un inserimento/espulsione può leggere i messaggi tramite l'handle inserimento/espulsione in una chiamata alla funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) . Nell'esempio seguente viene chiamata la funzione [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) per determinare se sono presenti messaggi in inserimento/espulsione. Se i messaggi sono in attesa, ogni viene visualizzato insieme al numero di messaggi rimanenti da leggere.

Un inserimento/espulsione esiste fino a quando non viene chiamata la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) per tutti gli handle server aperti o fino a quando non vengono chiusi tutti i processi server che possiedono un handle inserimento/espulsione. In entrambi i casi, tutti i messaggi non letti vengono eliminati da inserimento/espulsione, tutti gli handle client per il inserimento/espulsione vengono chiusi e il inserimento/espulsione stesso viene eliminato dalla memoria.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

HANDLE hSlot;
LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL ReadSlot() 
{ 
    DWORD cbMessage, cMessage, cbRead; 
    BOOL fResult; 
    LPTSTR lpszBuffer; 
    TCHAR achID[80]; 
    DWORD cAllMessages; 
    HANDLE hEvent;
    OVERLAPPED ov;
 
    cbMessage = cMessage = cbRead = 0; 

    hEvent = CreateEvent(NULL, FALSE, FALSE, TEXT("ExampleSlot"));
    if( NULL == hEvent )
        return FALSE;
    ov.Offset = 0;
    ov.OffsetHigh = 0;
    ov.hEvent = hEvent;
 
    fResult = GetMailslotInfo( hSlot, // mailslot handle 
        (LPDWORD) NULL,               // no maximum message size 
        &cbMessage,                   // size of next message 
        &cMessage,                    // number of messages 
        (LPDWORD) NULL);              // no read time-out 
 
    if (!fResult) 
    { 
        printf("GetMailslotInfo failed with %d.\n", GetLastError()); 
        return FALSE; 
    } 
 
    if (cbMessage == MAILSLOT_NO_MESSAGE) 
    { 
        printf("Waiting for a message...\n"); 
        return TRUE; 
    } 
 
    cAllMessages = cMessage; 
 
    while (cMessage != 0)  // retrieve all messages
    { 
        // Create a message-number string. 
 
        StringCchPrintf((LPTSTR) achID, 
            80,
            TEXT("\nMessage #%d of %d\n"), 
            cAllMessages - cMessage + 1, 
            cAllMessages); 

        // Allocate memory for the message. 
 
        lpszBuffer = (LPTSTR) GlobalAlloc(GPTR, 
            lstrlen((LPTSTR) achID)*sizeof(TCHAR) + cbMessage); 
        if( NULL == lpszBuffer )
            return FALSE;
        lpszBuffer[0] = '\0'; 
 
        fResult = ReadFile(hSlot, 
            lpszBuffer, 
            cbMessage, 
            &cbRead, 
            &ov); 
 
        if (!fResult) 
        { 
            printf("ReadFile failed with %d.\n", GetLastError()); 
            GlobalFree((HGLOBAL) lpszBuffer); 
            return FALSE; 
        } 
 
        // Concatenate the message and the message-number string. 
 
        StringCbCat(lpszBuffer, 
                    lstrlen((LPTSTR) achID)*sizeof(TCHAR)+cbMessage, 
                    (LPTSTR) achID); 
 
        // Display the message. 
 
        _tprintf(TEXT("Contents of the mailslot: %s\n"), lpszBuffer); 
 
        GlobalFree((HGLOBAL) lpszBuffer); 
 
        fResult = GetMailslotInfo(hSlot,  // mailslot handle 
            (LPDWORD) NULL,               // no maximum message size 
            &cbMessage,                   // size of next message 
            &cMessage,                    // number of messages 
            (LPDWORD) NULL);              // no read time-out 
 
        if (!fResult) 
        { 
            printf("GetMailslotInfo failed (%d)\n", GetLastError());
            return FALSE; 
        } 
    } 
    CloseHandle(hEvent);
    return TRUE; 
}

BOOL WINAPI MakeSlot(LPCTSTR lpszSlotName) 
{ 
    hSlot = CreateMailslot(lpszSlotName, 
        0,                             // no maximum message size 
        MAILSLOT_WAIT_FOREVER,         // no time-out for operations 
        (LPSECURITY_ATTRIBUTES) NULL); // default security
 
    if (hSlot == INVALID_HANDLE_VALUE) 
    { 
        printf("CreateMailslot failed with %d\n", GetLastError());
        return FALSE; 
    } 
    return TRUE; 
}

void main()
{
   MakeSlot(SlotName);

   while(TRUE)
   {
      ReadSlot();
      Sleep(3000);
   }
}
```



Di seguito è riportato l'output visualizzato quando questo esempio viene eseguito con il client inserimento/espulsione illustrato in [scrittura in un inserimento/espulsione](writing-to-a-mailslot.md).

``` syntax
Waiting for a message...
Waiting for a message...
Contents of the mailslot: Message one for mailslot.
Message #1 of 2

Contents of the mailslot: Message two for mailslot.
Message #2 of 2

Waiting for a message...
Contents of the mailslot: Message three for mailslot.
Message #1 of 1

Waiting for a message...
Waiting for a message...
Waiting for a message...
^C
```

 

 
