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
# <a name="menu-notifications"></a><span data-ttu-id="27126-103">Notifiche di menu</span><span class="sxs-lookup"><span data-stu-id="27126-103">Menu Notifications</span></span>

## <a name="in-this-section"></a><span data-ttu-id="27126-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="27126-104">In This Section</span></span>

-   [<span data-ttu-id="27126-105">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="27126-105">**WM\_COMMAND**</span></span>](wm-command.md)
-   [<span data-ttu-id="27126-106">**ContextMenu di WM \_**</span><span class="sxs-lookup"><span data-stu-id="27126-106">**WM\_CONTEXTMENU**</span></span>](wm-contextmenu.md)
-   [<span data-ttu-id="27126-107">**\_ENTERMENULOOP WM**</span><span class="sxs-lookup"><span data-stu-id="27126-107">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
-   [<span data-ttu-id="27126-108">**\_EXITMENULOOP WM**</span><span class="sxs-lookup"><span data-stu-id="27126-108">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
-   [<span data-ttu-id="27126-109">**\_GETTITLEBARINFOEX WM**</span><span class="sxs-lookup"><span data-stu-id="27126-109">**WM\_GETTITLEBARINFOEX**</span></span>](wm-gettitlebarinfoex.md)
-   [<span data-ttu-id="27126-110">**MENUCOMMAND di WM \_**</span><span class="sxs-lookup"><span data-stu-id="27126-110">**WM\_MENUCOMMAND**</span></span>](wm-menucommand.md)
-   [<span data-ttu-id="27126-111">**\_MENUDRAG WM**</span><span class="sxs-lookup"><span data-stu-id="27126-111">**WM\_MENUDRAG**</span></span>](wm-menudrag.md)
-   [<span data-ttu-id="27126-112">**\_MENUGETOBJECT WM**</span><span class="sxs-lookup"><span data-stu-id="27126-112">**WM\_MENUGETOBJECT**</span></span>](wm-menugetobject.md)
-   [<span data-ttu-id="27126-113">**\_MENURBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="27126-113">**WM\_MENURBUTTONUP**</span></span>](wm-menurbuttonup.md)
-   [<span data-ttu-id="27126-114">**\_NEXTMENU WM**</span><span class="sxs-lookup"><span data-stu-id="27126-114">**WM\_NEXTMENU**</span></span>](wm-nextmenu.md)
-   [<span data-ttu-id="27126-115">**\_UNINITMENUPOPUP WM**</span><span class="sxs-lookup"><span data-stu-id="27126-115">**WM\_UNINITMENUPOPUP**</span></span>](wm-uninitmenupopup.md)


## <a name="example"></a><span data-ttu-id="27126-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="27126-116">Example</span></span>

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
<span data-ttu-id="27126-117">Esempio tratto da [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="27126-117">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

 




