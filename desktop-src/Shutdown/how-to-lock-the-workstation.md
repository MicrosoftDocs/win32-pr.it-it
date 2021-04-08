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
# <a name="how-to-lock-the-workstation"></a>Come bloccare la workstation

L'esempio seguente blocca la workstation usando la funzione [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) . Il sistema Visualizza la finestra di dialogo **blocca workstation** . Il testo della finestra di dialogo indica che la workstation è in uso e che è stata bloccata dall'utente.


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

La workstation può essere sbloccata dall'utente o da un amministratore. Per sbloccare il sistema, premere CTRL + ALT + CANC e accedere. Per ricevere una notifica quando l'utente esegue l'accesso, usare la funzione [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) per eseguire la registrazione per ricevere i messaggi di [**modifica di WM \_ WTSSESSION \_**](../termserv/wm-wtssession-change.md) . Quando viene ricevuto questo messaggio, controllare se il parametro *wParam* è uguale a WTS \_ Session \_ Lock.

 

 
