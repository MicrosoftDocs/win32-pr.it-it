---
title: Come visualizzare le descrizioni comandi per i pulsanti
description: Quando si specifica lo \_ stile delle descrizioni comandi di TBSTYLE, la barra degli strumenti crea e gestisce un controllo ToolTip. Il controllo ToolTip è nascosto e viene visualizzato solo quando gli utenti spostano il puntatore del mouse su un pulsante della barra degli strumenti e lo lasciano per circa un secondo.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb37de7c21c904673a1f656533497130d50bd8f7
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103872220"
---
# <a name="how-to-display-tooltips-for-buttons"></a><span data-ttu-id="54c3d-104">Come visualizzare le descrizioni comandi per i pulsanti</span><span class="sxs-lookup"><span data-stu-id="54c3d-104">How to Display Tooltips for Buttons</span></span>

<span data-ttu-id="54c3d-105">Quando si specifica lo stile delle [**\_ descrizioni comandi di TBSTYLE**](toolbar-control-and-button-styles.md) , la barra degli strumenti crea e gestisce un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="54c3d-105">When you specify the [**TBSTYLE\_TOOLTIPS**](toolbar-control-and-button-styles.md) style, the toolbar creates and manages a tooltip control.</span></span> <span data-ttu-id="54c3d-106">Il controllo ToolTip è nascosto e viene visualizzato solo quando gli utenti spostano il puntatore del mouse su un pulsante della barra degli strumenti e lo lasciano per circa un secondo.</span><span class="sxs-lookup"><span data-stu-id="54c3d-106">The tooltip control is hidden and appears only when users move the pointer over a toolbar button and leave it there for approximately one second.</span></span>

<span data-ttu-id="54c3d-107">L'applicazione può fornire testo al controllo ToolTip in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="54c3d-107">Your application can supply text to the tooltip control in any one of the following ways:</span></span>

-   <span data-ttu-id="54c3d-108">Impostare il testo della descrizione comando **come membro della** struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) per ogni pulsante.</span><span class="sxs-lookup"><span data-stu-id="54c3d-108">Set the tooltip text as the **iString** member of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure for each button.</span></span> <span data-ttu-id="54c3d-109">È inoltre necessario inviare un messaggio [**TB \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md) e impostare le righe di testo massime su 0, in modo che il testo non venga visualizzato come etichetta del pulsante anziché come descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="54c3d-109">You must also send a [**TB\_SETMAXTEXTROWS**](tb-setmaxtextrows.md) message and set the maximum text rows to 0, so that the text does not appear as the button label rather than as a tooltip.</span></span>
-   <span data-ttu-id="54c3d-110">Creare la barra degli strumenti con lo stile [**\_ elenco TBSTYLE**](toolbar-control-and-button-styles.md) , quindi impostare lo stile esteso [**TBSTYLE \_ ex \_ MIXEDBUTTONS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="54c3d-110">Create the toolbar with the [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style and then set the [**TBSTYLE\_EX\_MIXEDBUTTONS**](toolbar-extended-styles.md) extended style.</span></span> <span data-ttu-id="54c3d-111">Le etichette vengono visualizzate solo per i pulsanti con lo stile di [**\_ SHOWTEXT BTNS**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="54c3d-111">Labels are shown only for buttons that have the [**BTNS\_SHOWTEXT**](toolbar-control-and-button-styles.md) style.</span></span> <span data-ttu-id="54c3d-112">Per i pulsanti che non hanno questo stile, viene visualizzata una descrizione comando che contiene il testo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="54c3d-112">For buttons that do not have this style, a tooltip is shown that contains the button text.</span></span>
-   <span data-ttu-id="54c3d-113">Rispondere al codice di notifica di [TTN \_ GETDISPINFO](ttn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="54c3d-113">Respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification code.</span></span>
-   <span data-ttu-id="54c3d-114">Rispondere al codice di notifica di [TBN \_ GETINFOTIP](tbn-getinfotip.md) .</span><span class="sxs-lookup"><span data-stu-id="54c3d-114">Respond to the [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code.</span></span>

<span data-ttu-id="54c3d-115">Un'applicazione che deve inviare messaggi direttamente al controllo ToolTip può recuperare l'handle per il controllo usando il messaggio [**TB \_ GetToolTips**](tb-gettooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="54c3d-115">An application that needs to send messages directly to the tooltip control can retrieve the handle to the control by using the [**TB\_GETTOOLTIPS**](tb-gettooltips.md) message.</span></span> <span data-ttu-id="54c3d-116">Un'applicazione può sostituire il controllo ToolTip di una barra degli strumenti con un altro controllo ToolTip usando il messaggio [**TB \_ setooltips**](tb-settooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="54c3d-116">An application can replace the tooltip control of a toolbar with another tooltip control by using the [**TB\_SETTOOLTIPS**](tb-settooltips.md) message.</span></span>

<span data-ttu-id="54c3d-117">Il modo più flessibile per fornire il testo della descrizione comando consiste nel rispondere al codice di notifica [TTN \_ GETDISPINFO](ttn-getdispinfo.md) o [TBN \_ GETINFOTIP](tbn-getinfotip.md) inviato dal controllo Toolbar al relativo elemento padre sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="54c3d-117">The most flexible way of supplying tooltip text is to respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) or [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code sent by the toolbar control to its parent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="54c3d-118">Per [TTN \_ GETDISPINFO](ttn-getdispinfo.md), il parametro *lParam* include un puntatore a una struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (definita anche **LPTOOLTIPTEXT**) che specifica l'identificatore di comando del pulsante per il quale è necessario il testo della guida.</span><span class="sxs-lookup"><span data-stu-id="54c3d-118">For [TTN\_GETDISPINFO](ttn-getdispinfo.md), the *lParam* parameter includes a pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure (also defined as **LPTOOLTIPTEXT**) that specifies the command identifier of the button for which Help text is needed.</span></span> <span data-ttu-id="54c3d-119">Questo identificatore si trova nel membro **NMTTDISPINFO. HDR. idFrom** .</span><span class="sxs-lookup"><span data-stu-id="54c3d-119">This identifier is in the **NMTTDISPINFO.hdr.idFrom** member.</span></span> <span data-ttu-id="54c3d-120">Un'applicazione può copiare il testo della guida nella struttura, specificare l'indirizzo di una stringa contenente il testo della guida o specificare l'handle dell'istanza e l'identificatore di risorsa di una risorsa di stringa.</span><span class="sxs-lookup"><span data-stu-id="54c3d-120">An application can copy the Help text to the structure, specify the address of a string containing the Help text, or specify the instance handle and resource identifier of a string resource.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="54c3d-121">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="54c3d-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="54c3d-122">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="54c3d-122">Technologies</span></span>

-   [<span data-ttu-id="54c3d-123">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="54c3d-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="54c3d-124">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="54c3d-124">Prerequisites</span></span>

-   <span data-ttu-id="54c3d-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="54c3d-125">C/C++</span></span>
-   <span data-ttu-id="54c3d-126">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="54c3d-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="54c3d-127">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="54c3d-127">Instructions</span></span>

### <a name="display-a-tooltip-for-a-button"></a><span data-ttu-id="54c3d-128">Visualizzare una descrizione comando per un pulsante</span><span class="sxs-lookup"><span data-stu-id="54c3d-128">Display a Tooltip for a Button</span></span>

<span data-ttu-id="54c3d-129">Il codice di esempio seguente gestisce il codice di notifica della descrizione comando [TTN \_ GETDISPINFO](ttn-getdispinfo.md) fornendo testo da identificatori di risorsa.</span><span class="sxs-lookup"><span data-stu-id="54c3d-129">The following example code handles the [TTN\_GETDISPINFO](ttn-getdispinfo.md) tooltip notification code by providing text from resource identifiers.</span></span>


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a><span data-ttu-id="54c3d-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54c3d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54c3d-131">Utilizzo di controlli Toolbar</span><span class="sxs-lookup"><span data-stu-id="54c3d-131">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="54c3d-132">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="54c3d-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




