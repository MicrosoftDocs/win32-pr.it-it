---
description: L'esempio seguente blocca la workstation usando la funzione LockWorkStation. Il sistema Visualizza la finestra di dialogo blocca workstation. Il testo della finestra di dialogo indica che la workstation è in uso e che è stata bloccata dall'utente.
ms.assetid: 7cbf9a0a-dfab-42e6-9a71-bb240121f59f
title: Come bloccare la workstation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6c198816613a13914c44a5a51f5317e2019f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882357"
---
# <a name="how-to-lock-the-workstation"></a><span data-ttu-id="e52aa-105">Come bloccare la workstation</span><span class="sxs-lookup"><span data-stu-id="e52aa-105">How to Lock the Workstation</span></span>

<span data-ttu-id="e52aa-106">L'esempio seguente blocca la workstation usando la funzione [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) .</span><span class="sxs-lookup"><span data-stu-id="e52aa-106">The following example locks the workstation using the [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) function.</span></span> <span data-ttu-id="e52aa-107">Il sistema Visualizza la finestra di dialogo **blocca workstation** .</span><span class="sxs-lookup"><span data-stu-id="e52aa-107">The system displays the **Lock Workstation** dialog box.</span></span> <span data-ttu-id="e52aa-108">Il testo della finestra di dialogo indica che la workstation è in uso e che è stata bloccata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e52aa-108">The dialog box text says that the workstation is in use and has been locked by the user.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment( lib, "user32.lib" )

void main()
{
    // Lock the workstation.

    if( !LockWorkStation() )
        printf ("LockWorkStation failed with %d\n", GetLastError());
}
```



<span data-ttu-id="e52aa-109">Per determinare se la workstation è bloccata, verificare se la finestra è visibile.</span><span class="sxs-lookup"><span data-stu-id="e52aa-109">To determine whether the workstation is locked, test whether your window is visible.</span></span>

<span data-ttu-id="e52aa-110">La workstation può essere sbloccata dall'utente o da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="e52aa-110">The workstation can be unlocked by the user or an administrator.</span></span> <span data-ttu-id="e52aa-111">Per sbloccare il sistema, premere CTRL + ALT + CANC e accedere.</span><span class="sxs-lookup"><span data-stu-id="e52aa-111">To unlock the system, press Ctrl+Alt+Del and log in.</span></span> <span data-ttu-id="e52aa-112">Per ricevere una notifica quando l'utente esegue l'accesso, usare la funzione [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) per eseguire la registrazione per ricevere i messaggi di [**modifica di WM \_ WTSSESSION \_**](../termserv/wm-wtssession-change.md) .</span><span class="sxs-lookup"><span data-stu-id="e52aa-112">To receive notification when the user logs in, use the [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) function to register to receive [**WM\_WTSSESSION\_CHANGE**](../termserv/wm-wtssession-change.md) messages.</span></span> <span data-ttu-id="e52aa-113">Quando viene ricevuto questo messaggio, controllare se il parametro *wParam* è uguale a WTS \_ Session \_ Lock.</span><span class="sxs-lookup"><span data-stu-id="e52aa-113">When this message is received, check whether the *wParam* parameter is equal to WTS\_SESSION\_LOCK.</span></span>

 

 
