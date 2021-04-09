---
description: Nell'esempio seguente viene usata la funzione ExitWindows per disconnettere l'utente corrente.
ms.assetid: 74be3505-c4bd-4ae2-aaed-700382839006
title: Come disconnettere l'utente corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e59ce625ae7da8a2a4a901fbb1429ab0f9b638c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967473"
---
# <a name="how-to-log-off-the-current-user"></a>Come disconnettere l'utente corrente

Nell'esempio seguente viene usata la funzione [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) per disconnettere l'utente corrente.

``` syntax
// Log off the current user. 

ExitWindows(0, 0);
```

Nell'esempio seguente viene usata la funzione [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) per disconnettere l'utente corrente.

``` syntax
// Log off the current user. 

ExitWindowsEx(EWX_LOGOFF, 0);
```

L'applicazione riceve il messaggio [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) e visualizza una finestra di dialogo in cui viene chiesto se è OK terminare la sessione. Se l'utente fa clic su **Sì**, il sistema disconnette l'utente. Se l'utente fa clic su **No**, la disconnessione viene annullata.

``` syntax
// Process the message in the window procedure. 

case WM_QUERYENDSESSION:  
{ 
    int r; 
    r = MessageBox(NULL,(LPCWSTR)L"End the session?",(LPCWSTR)L"WM_QUERYENDSESSION",MB_YESNO);
 
    // Return TRUE to continue, FALSE to stop. 
 
    return r == IDYES; 
    break; 
}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Disconnessione](logging-off.md)
</dt> </dl>

 

 



