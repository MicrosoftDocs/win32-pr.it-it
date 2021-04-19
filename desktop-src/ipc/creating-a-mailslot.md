---
description: 'Come creare mailslot. Mailslot sono supportati da tre funzioni specializzate: CreateMailslot, GetMailslotInfo e SetMailslotInfo. Queste funzioni vengono usate dal server inserimento/espulsione.'
ms.assetid: 7f5a3b36-9583-43fc-a977-321c00a48edb
title: Creazione di un inserimento/espulsione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4cfbcf990162347d1e45da01c815002f39299e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318074"
---
# <a name="creating-a-mailslot"></a>Creazione di un inserimento/espulsione

Mailslot sono supportati da tre funzioni specializzate: [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)e [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo). Queste funzioni vengono usate dal server inserimento/espulsione.

Nell'esempio di codice seguente viene usata la funzione [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) per recuperare l'handle a un inserimento/espulsione denominato "Sample \_ inserimento/espulsione". L'esempio di codice in [scrittura in un inserimento/espulsione](writing-to-a-mailslot.md) Mostra in che modo l'applicazione client può scrivere in questo inserimento/espulsione.


```C++
#include <windows.h>
#include <stdio.h>

HANDLE hSlot;
LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

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
    else printf("Mailslot created successfully.\n"); 
    return TRUE; 
}

void main()
{ 
   MakeSlot(SlotName);
}
```



Per creare un inserimento/espulsione che può essere ereditato dai processi figlio, un'applicazione deve modificare la struttura degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) passata come ultimo parametro di [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota). A tale scopo, l'applicazione imposta il membro **bInheritHandle** della struttura su **true** (l'impostazione predefinita è **false**).

 

 
