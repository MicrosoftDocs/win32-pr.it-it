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
# <a name="how-to-log-off-the-current-user"></a><span data-ttu-id="4e789-103">Come disconnettere l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="4e789-103">How to Log Off the Current User</span></span>

<span data-ttu-id="4e789-104">Nell'esempio seguente viene usata la funzione [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) per disconnettere l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="4e789-104">The following example uses the [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindows(0, 0);
```

<span data-ttu-id="4e789-105">Nell'esempio seguente viene usata la funzione [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) per disconnettere l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="4e789-105">The following example uses the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindowsEx(EWX_LOGOFF, 0);
```

<span data-ttu-id="4e789-106">L'applicazione riceve il messaggio [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) e visualizza una finestra di dialogo in cui viene chiesto se è OK terminare la sessione.</span><span class="sxs-lookup"><span data-stu-id="4e789-106">The application receives the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message and displays a dialog box asking the whether it is OK to end the session.</span></span> <span data-ttu-id="4e789-107">Se l'utente fa clic su **Sì**, il sistema disconnette l'utente.</span><span class="sxs-lookup"><span data-stu-id="4e789-107">If the user clicks **Yes**, the system logs off the user.</span></span> <span data-ttu-id="4e789-108">Se l'utente fa clic su **No**, la disconnessione viene annullata.</span><span class="sxs-lookup"><span data-stu-id="4e789-108">If the user clicks **No**, the logoff is canceled.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4e789-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4e789-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e789-110">Disconnessione</span><span class="sxs-lookup"><span data-stu-id="4e789-110">Logging Off</span></span>](logging-off.md)
</dt> </dl>

 

 



