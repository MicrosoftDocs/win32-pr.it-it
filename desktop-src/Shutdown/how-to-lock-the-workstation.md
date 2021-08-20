---
description: L'esempio seguente blocca la workstation usando la funzione LockWorkStation. Il sistema visualizza la finestra di dialogo Blocca workstation. Il testo della finestra di dialogo indica che la workstation è in uso ed è stata bloccata dall'utente.
ms.assetid: 7cbf9a0a-dfab-42e6-9a71-bb240121f59f
title: Come bloccare la workstation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b349a3e41cf7a8059cb24fc0c3ade66d179777e70fbd84bd21cac3d46502f1cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117963808"
---
# <a name="how-to-lock-the-workstation"></a>Come bloccare la workstation

L'esempio seguente blocca la workstation usando la [**funzione LockWorkStation.**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) Il sistema visualizza la **finestra di dialogo Blocca workstation.** Il testo della finestra di dialogo indica che la workstation è in uso ed è stata bloccata dall'utente.


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



Per determinare se la workstation è bloccata, verificare se la finestra è visibile.

La workstation può essere sbloccata dall'utente o da un amministratore. Per sbloccare il sistema, premere CTRL+ALT+CANC e accedere. Per ricevere una notifica quando l'utente accede, usare la [**funzione WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) per registrarsi per ricevere messaggi [**WM \_ WTSSESSION \_ CHANGE.**](../termserv/wm-wtssession-change.md) Quando viene ricevuto questo messaggio, verificare se il *parametro wParam* è uguale a WTS \_ SESSION \_ LOCK.

 

 
