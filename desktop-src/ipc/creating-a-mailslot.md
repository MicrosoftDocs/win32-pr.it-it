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
# <a name="creating-a-mailslot"></a><span data-ttu-id="ecb9d-105">Creazione di un inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="ecb9d-105">Creating a Mailslot</span></span>

<span data-ttu-id="ecb9d-106">Mailslot sono supportati da tre funzioni specializzate: [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)e [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo).</span><span class="sxs-lookup"><span data-stu-id="ecb9d-106">Mailslots are supported by three specialized functions: [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo), and [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo).</span></span> <span data-ttu-id="ecb9d-107">Queste funzioni vengono usate dal server inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="ecb9d-107">These functions are used by the mailslot server.</span></span>

<span data-ttu-id="ecb9d-108">Nell'esempio di codice seguente viene usata la funzione [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) per recuperare l'handle a un inserimento/espulsione denominato "Sample \_ inserimento/espulsione".</span><span class="sxs-lookup"><span data-stu-id="ecb9d-108">The following code sample uses the [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) function to retrieve the handle to a mailslot named "sample\_mailslot".</span></span> <span data-ttu-id="ecb9d-109">L'esempio di codice in [scrittura in un inserimento/espulsione](writing-to-a-mailslot.md) Mostra in che modo l'applicazione client può scrivere in questo inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="ecb9d-109">The code sample in [Writing to a Mailslot](writing-to-a-mailslot.md) shows how client application can write to this mailslot.</span></span>


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



<span data-ttu-id="ecb9d-110">Per creare un inserimento/espulsione che può essere ereditato dai processi figlio, un'applicazione deve modificare la struttura degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) passata come ultimo parametro di [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota).</span><span class="sxs-lookup"><span data-stu-id="ecb9d-110">To create a mailslot that can be inherited by child processes, an application should change the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure passed as the last parameter of [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota).</span></span> <span data-ttu-id="ecb9d-111">A tale scopo, l'applicazione imposta il membro **bInheritHandle** della struttura su **true** (l'impostazione predefinita è **false**).</span><span class="sxs-lookup"><span data-stu-id="ecb9d-111">To do this, the application sets the **bInheritHandle** member of this structure to **TRUE** (the default setting is **FALSE**).</span></span>

 

 
