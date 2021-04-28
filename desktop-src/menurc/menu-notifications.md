---
title: Notifiche di menu
description: Notifiche di menu
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593e3007dff82241dc9e917a6cfa140cc443679
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112529"
---
# <a name="menu-notifications"></a>Notifiche di menu

## <a name="in-this-section"></a>Contenuto della sezione

-   [**COMANDO \_ WM**](wm-command.md)
-   [**WM \_ CONTEXTMENU**](wm-contextmenu.md)
-   [**WM \_ ENTERMENULOOP**](wm-entermenuloop.md)
-   [**WM \_ EXITMENULOOP**](wm-exitmenuloop.md)
-   [**WM \_ GETTITLEBARINFOEX**](wm-gettitlebarinfoex.md)
-   [**WM \_ MENUCOMMAND**](wm-menucommand.md)
-   [**WM \_ MENUDRAG**](wm-menudrag.md)
-   [**WM \_ MENUGETOBJECT**](wm-menugetobject.md)
-   [**WM \_ MENURBUTTONUP**](wm-menurbuttonup.md)
-   [**WM \_ NEXTMENU**](wm-nextmenu.md)
-   [**WM \_ UNINITMENUPOPUP**](wm-uninitmenupopup.md)


## <a name="example"></a>Esempio

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
Esempio tratto da [esempi classici di Windows](https://github.com/microsoft/Windows-classic-samples) su GitHub.

 




