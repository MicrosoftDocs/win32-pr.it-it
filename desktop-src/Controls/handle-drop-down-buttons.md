---
title: Come gestire i pulsanti a discesa
description: Un pulsante a discesa può presentare agli utenti un elenco di opzioni.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d6f59bfa888d346e196e13ce030d1473a07f0f
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724274"
---
# <a name="how-to-handle-drop-down-buttons"></a><span data-ttu-id="0fb7c-103">Come gestire i pulsanti a discesa</span><span class="sxs-lookup"><span data-stu-id="0fb7c-103">How to Handle Drop-down Buttons</span></span>

<span data-ttu-id="0fb7c-104">Un pulsante a discesa può presentare agli utenti un elenco di opzioni.</span><span class="sxs-lookup"><span data-stu-id="0fb7c-104">A drop-down button can present users with a list of options.</span></span> <span data-ttu-id="0fb7c-105">Per creare questo stile di pulsante, specificare lo stile dell' [**\_ elenco a discesa BTNS**](toolbar-control-and-button-styles.md) (detto anche [**elenco a \_ discesa TBSTYLE**](toolbar-control-and-button-styles.md) per la compatibilità con le versioni precedenti dei controlli comuni).</span><span class="sxs-lookup"><span data-stu-id="0fb7c-105">To create this style of button, specify the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style (also called [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) for compatibility with previous versions of the common controls).</span></span> <span data-ttu-id="0fb7c-106">Per visualizzare un pulsante a discesa con una freccia, è necessario impostare anche lo stile della barra degli strumenti [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) inviando un messaggio [**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="0fb7c-106">To show a drop-down button with an arrow, you must also set the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) toolbar style by sending a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span>

<span data-ttu-id="0fb7c-107">Nella figura seguente viene mostrato un pulsante a discesa "Apri" con il menu di scelta rapida aperto e viene visualizzato un elenco di file.</span><span class="sxs-lookup"><span data-stu-id="0fb7c-107">The following illustration shows a drop-down "Open" button with the context menu open and showing a list of files.</span></span> <span data-ttu-id="0fb7c-108">In questo esempio, la barra degli strumenti ha lo stile [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0fb7c-108">In this example, the toolbar has the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![Screenshot di una finestra di dialogo con tre elementi della barra degli strumenti rappresentati da icone; uno ha una freccia a discesa espansa e un menu di scelta rapida di tre elementi](images/tb-dropdown.png)

<span data-ttu-id="0fb7c-110">La figura seguente mostra la stessa barra degli strumenti, questa volta senza lo stile [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0fb7c-110">The following illustration shows the same toolbar, this time without the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![Screenshot di una finestra di dialogo precedente, ma l'icona con il menu di scelta rapida non dispone di una freccia a discesa](images/tb-dropdown2.png)

<span data-ttu-id="0fb7c-112">Quando gli utenti fanno clic su un pulsante della barra degli strumenti che usa lo stile a [**\_ discesa BTNS**](toolbar-control-and-button-styles.md) , il controllo Toolbar invia la finestra padre a un codice di notifica a [ \_ discesa TBN](tbn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="0fb7c-112">When users click a toolbar button that uses the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style, the toolbar control sends its parent window a [TBN\_DROPDOWN](tbn-dropdown.md) notification code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0fb7c-113">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="0fb7c-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0fb7c-114">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="0fb7c-114">Technologies</span></span>

-   [<span data-ttu-id="0fb7c-115">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="0fb7c-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0fb7c-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="0fb7c-116">Prerequisites</span></span>

-   <span data-ttu-id="0fb7c-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="0fb7c-117">C/C++</span></span>
-   <span data-ttu-id="0fb7c-118">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="0fb7c-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0fb7c-119">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="0fb7c-119">Instructions</span></span>

### <a name="handle-a-drop-down-button"></a><span data-ttu-id="0fb7c-120">Gestire un pulsante a discesa</span><span class="sxs-lookup"><span data-stu-id="0fb7c-120">Handle a Drop-down Button</span></span>

<span data-ttu-id="0fb7c-121">Nell'esempio di codice seguente viene illustrato come un'applicazione può supportare un pulsante a discesa in un controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="0fb7c-121">The following code example demonstrates how an application can support a drop-down button in a toolbar control.</span></span>


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="0fb7c-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0fb7c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fb7c-123">Utilizzo di controlli Toolbar</span><span class="sxs-lookup"><span data-stu-id="0fb7c-123">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="0fb7c-124">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="0fb7c-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




