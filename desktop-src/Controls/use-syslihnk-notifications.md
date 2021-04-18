---
title: Come usare le notifiche SysLink
description: Sono presenti due messaggi di notifica associati al controllo SysLink \ 8212; uno per il mouse (NM \_ clic (Syslink)) e uno per la tastiera (Nm \_ Return).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "106299542"
---
# <a name="how-to-use-syslink-notifications"></a><span data-ttu-id="a3e8f-103">Come usare le notifiche SysLink</span><span class="sxs-lookup"><span data-stu-id="a3e8f-103">How to Use SysLink Notifications</span></span>

<span data-ttu-id="a3e8f-104">Al controllo SysLink sono associati due messaggi di notifica: uno per il mouse ([nm \_ clic (Syslink)](nm-click-syslink.md)) e uno per la tastiera ([nm \_ return](nm-return.md)).</span><span class="sxs-lookup"><span data-stu-id="a3e8f-104">There are two notification messages associated with the SysLink control—one for the mouse ([NM\_CLICK (syslink)](nm-click-syslink.md)), and one for the keyboard ([NM\_RETURN](nm-return.md)).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a3e8f-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="a3e8f-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a3e8f-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="a3e8f-106">Technologies</span></span>

-   [<span data-ttu-id="a3e8f-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="a3e8f-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a3e8f-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a3e8f-108">Prerequisites</span></span>

-   <span data-ttu-id="a3e8f-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="a3e8f-109">C/C++</span></span>
-   <span data-ttu-id="a3e8f-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="a3e8f-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a3e8f-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="a3e8f-111">Instructions</span></span>

### <a name="use-syslink-notifications"></a><span data-ttu-id="a3e8f-112">Usare le notifiche di SysLink</span><span class="sxs-lookup"><span data-stu-id="a3e8f-112">Use SysLink Notifications</span></span>

<span data-ttu-id="a3e8f-113">Nell'esempio di codice seguente viene illustrato come elaborare le notifiche SysLink generate quando l'utente fa clic su uno dei due collegamenti nell' [esempio precedente](create-syslink-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a3e8f-113">The following example code shows how to process the SysLink notifications that are generated when the user clicks either of the two links in the [previous example](create-syslink-controls.md).</span></span> <span data-ttu-id="a3e8f-114">Quando l'utente fa clic sull'URL Internet, la pagina Web associata viene aperta nel browser predefinito.</span><span class="sxs-lookup"><span data-stu-id="a3e8f-114">When the user clicks the Internet URL, the associated webpage opens in the default browser.</span></span> <span data-ttu-id="a3e8f-115">Quando l'utente fa clic sul collegamento ipertestuale definito dall'applicazione, viene visualizzata una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="a3e8f-115">When the user clicks the application-defined hyperlink, a message box is displayed.</span></span>


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a><span data-ttu-id="a3e8f-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3e8f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3e8f-117">Uso di controlli SysLink</span><span class="sxs-lookup"><span data-stu-id="a3e8f-117">Using SysLink Controls</span></span>](using-syslink-controls.md)
</dt> <dt>

<span data-ttu-id="a3e8f-118">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="a3e8f-118">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




