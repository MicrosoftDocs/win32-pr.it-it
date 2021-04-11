---
title: Notifiche di menu
description: .
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61f5303253fd3201fd9a4510ecf90fa76c10524
ms.sourcegitcommit: e98f40bef170ae9ce30d91ba96b90600b0446a24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/28/2020
ms.locfileid: "104336727"
---
# <a name="menu-notifications"></a>Notifiche di menu

## <a name="in-this-section"></a>Contenuto della sezione

-   [**\_comando WM**](wm-command.md)
-   [**ContextMenu di WM \_**](wm-contextmenu.md)
-   [**\_ENTERMENULOOP WM**](wm-entermenuloop.md)
-   [**\_EXITMENULOOP WM**](wm-exitmenuloop.md)
-   [**\_GETTITLEBARINFOEX WM**](wm-gettitlebarinfoex.md)
-   [**MENUCOMMAND di WM \_**](wm-menucommand.md)
-   [**\_MENUDRAG WM**](wm-menudrag.md)
-   [**\_MENUGETOBJECT WM**](wm-menugetobject.md)
-   [**\_MENURBUTTONUP WM**](wm-menurbuttonup.md)
-   [**\_NEXTMENU WM**](wm-nextmenu.md)
-   [**\_UNINITMENUPOPUP WM**](wm-uninitmenupopup.md)


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
Esempio tratto da [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples) in GitHub.

 




