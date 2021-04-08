---
title: Come implementare le descrizioni comandi di rilevamento
description: Le descrizioni comandi di rilevamento rimangono visibili fino a quando non vengono chiuse in modo esplicito dall'applicazione e possono modificare la posizione sullo schermo in modo dinamico. Sono supportati dalla versione 4,70 e successive dei controlli comuni.
ms.assetid: 4BE1F9E6-92B6-4CA7-B89A-F2162BC86366
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a614fef7ed69cd8c2763f9370ce0011d51eb0c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044284"
---
# <a name="how-to-implement-tracking-tooltips"></a><span data-ttu-id="64a3a-104">Come implementare le descrizioni comandi di rilevamento</span><span class="sxs-lookup"><span data-stu-id="64a3a-104">How to Implement Tracking Tooltips</span></span>

<span data-ttu-id="64a3a-105">Le descrizioni comandi di rilevamento rimangono visibili fino a quando non vengono chiuse in modo esplicito dall'applicazione e possono modificare la posizione sullo schermo in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="64a3a-105">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="64a3a-106">Sono supportati dalla [versione 4,70](common-control-versions.md) e successive dei controlli comuni.</span><span class="sxs-lookup"><span data-stu-id="64a3a-106">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span>

<span data-ttu-id="64a3a-107">Per creare una descrizione comando di rilevamento, includere il \_ flag di traccia ttf nel membro **uFlags** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) quando si invia il messaggio [**TTM \_ ADDTOOL**](ttm-addtool.md) .</span><span class="sxs-lookup"><span data-stu-id="64a3a-107">To create a tracking tooltip, include the TTF\_TRACK flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when sending the [**TTM\_ADDTOOL**](ttm-addtool.md) message.</span></span>

<span data-ttu-id="64a3a-108">L'applicazione deve attivare manualmente (mostrare) e disattivare (nascondere) una descrizione comando di rilevamento inviando un messaggio [**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md) .</span><span class="sxs-lookup"><span data-stu-id="64a3a-108">Your application must manually activate (show) and deactivate (hide) a tracking tooltip by sending a [**TTM\_TRACKACTIVATE**](ttm-trackactivate.md) message.</span></span> <span data-ttu-id="64a3a-109">Mentre una descrizione comando di rilevamento è attiva, l'applicazione deve specificare il percorso della descrizione comando inviando messaggi [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) al controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="64a3a-109">While a tracking tooltip is active, your application must specify the location of the tooltip by sending [**TTM\_TRACKPOSITION**](ttm-trackposition.md) messages to the tooltip control.</span></span> <span data-ttu-id="64a3a-110">Poiché l'applicazione gestisce le attività, ad esempio il posizionamento della descrizione comando, le descrizioni comandi di rilevamento non usano il flag della **\_ sottoclasse ttf** o il messaggio [**TTM \_ RELAYEVENT**](ttm-relayevent.md) .</span><span class="sxs-lookup"><span data-stu-id="64a3a-110">Because the application handles tasks such as positioning the tooltip, tracking tooltips do not use the **TTF\_SUBCLASS** flag or the [**TTM\_RELAYEVENT**](ttm-relayevent.md) message.</span></span>

<span data-ttu-id="64a3a-111">Il messaggio [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) fa sì che il controllo ToolTip visualizzi la finestra usando uno dei due stili di selezione host:</span><span class="sxs-lookup"><span data-stu-id="64a3a-111">The [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message causes the tooltip control to display the window using one of two placement styles:</span></span>

-   <span data-ttu-id="64a3a-112">Per impostazione predefinita, la descrizione comando viene visualizzata accanto allo strumento corrispondente in una posizione scelta dal controllo.</span><span class="sxs-lookup"><span data-stu-id="64a3a-112">By default, the tooltip is displayed next to the corresponding tool in a position that the control chooses.</span></span> <span data-ttu-id="64a3a-113">Il percorso scelto è relativo alle coordinate fornite mediante questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="64a3a-113">The location chosen is relative to the coordinates that you provide by using this message.</span></span>
-   <span data-ttu-id="64a3a-114">Se si include il **valore \_ assoluto ttf** nel membro della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , la descrizione comando viene visualizzata in corrispondenza della posizione in pixel specificata nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="64a3a-114">If you include the **TTF\_ABSOLUTE** value in the member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, the tooltip is displayed at the pixel location specified in the message.</span></span> <span data-ttu-id="64a3a-115">In questo caso, il controllo non tenta di modificare la posizione della finestra della descrizione comando dalle coordinate fornite.</span><span class="sxs-lookup"><span data-stu-id="64a3a-115">In this case, the control does not attempt to change the tooltip window's location from the coordinates you provide.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="64a3a-116">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="64a3a-116">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="64a3a-117">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="64a3a-117">Technologies</span></span>

-   [<span data-ttu-id="64a3a-118">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="64a3a-118">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="64a3a-119">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="64a3a-119">Prerequisites</span></span>

-   <span data-ttu-id="64a3a-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="64a3a-120">C/C++</span></span>
-   <span data-ttu-id="64a3a-121">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="64a3a-121">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="64a3a-122">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="64a3a-122">Instructions</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="64a3a-123">Implementare descrizioni comando In-Place</span><span class="sxs-lookup"><span data-stu-id="64a3a-123">Implement In-Place Tooltips</span></span>

<span data-ttu-id="64a3a-124">Il membro **uFlags** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) utilizzata nell'esempio include il flag **\_ assoluto ttf** .</span><span class="sxs-lookup"><span data-stu-id="64a3a-124">The **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that is used in the example includes the **TTF\_ABSOLUTE** flag.</span></span> <span data-ttu-id="64a3a-125">Senza questo flag, il controllo ToolTip sceglie dove visualizzare la descrizione comando e la relativa posizione rispetto alla finestra di dialogo può cambiare improvvisamente quando il puntatore del mouse viene spostato.</span><span class="sxs-lookup"><span data-stu-id="64a3a-125">Without this flag, the tooltip control chooses where to display the tooltip, and its position relative to the dialog box may change suddenly as the mouse pointer moves.</span></span>

> [!Note]  
> <span data-ttu-id="64a3a-126">`g_toolItem` è una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) globale.</span><span class="sxs-lookup"><span data-stu-id="64a3a-126">`g_toolItem` is a global [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

 

<span data-ttu-id="64a3a-127">Nell'esempio seguente viene illustrato come creare un controllo ToolTip di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="64a3a-127">The following example demonstrates how to create a tracking tooltip control.</span></span> <span data-ttu-id="64a3a-128">Nell'esempio viene specificata l'intera area client della finestra principale come strumento.</span><span class="sxs-lookup"><span data-stu-id="64a3a-128">The example specifies the main window's entire client area as the tool.</span></span>


```C++
HWND CreateTrackingToolTip(int toolID, HWND hDlg, WCHAR* pText)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hDlg, NULL, g_hInst,NULL);

    if (!hwndTT)
    {
      return NULL;
    }

    // Set up the tool information. In this case, the "tool" is the entire parent window.
    
    g_toolItem.cbSize   = sizeof(TOOLINFO);
    g_toolItem.uFlags   = TTF_IDISHWND | TTF_TRACK | TTF_ABSOLUTE;
    g_toolItem.hwnd     = hDlg;
    g_toolItem.hinst    = g_hInst;
    g_toolItem.lpszText = pText;
    g_toolItem.uId      = (UINT_PTR)hDlg;
    
    GetClientRect (hDlg, &g_toolItem.rect);

    // Associate the tooltip with the tool window.
    
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &g_toolItem); 
    
    return hwndTT;
}
            
```



### <a name="window-procedure-implementation"></a><span data-ttu-id="64a3a-129">Implementazione della routine della finestra</span><span class="sxs-lookup"><span data-stu-id="64a3a-129">Window Procedure Implementation</span></span>

<span data-ttu-id="64a3a-130">Quando il puntatore del mouse si trova all'interno dell'area client, la descrizione comando è attiva e visualizza le coordinate del cursore, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="64a3a-130">When the mouse pointer is within the client area, the tooltip is active and displays the cursor coordinates, as shown in the following illustration.</span></span>

![Screenshot di una finestra di dialogo; una descrizione comando Visualizza le coordinate x e y del puntatore del mouse](images/tt-tracking.png)

<span data-ttu-id="64a3a-132">Il codice di esempio seguente è riportato nella procedura della finestra per una finestra di dialogo in cui viene visualizzata la descrizione comando di rilevamento creata nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="64a3a-132">The following example code is from the window procedure for a dialog box that displays the tracking tooltip created in the preceding example.</span></span> <span data-ttu-id="64a3a-133">La variabile booleana globale *g \_ TrackingMouse* viene utilizzata per determinare se è necessario riattivare la descrizione comando e reimpostare il rilevamento del mouse in modo che l'applicazione riceva una notifica quando il puntatore del mouse esce dall'area client della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="64a3a-133">The global Boolean variable *g\_TrackingMouse* is used to determine whether it is necessary to reactivate the tooltip and reset mouse tracking so that the application is notified when the mouse pointer leaves the client area of the dialog box.</span></span>


```
//g_hwndTrackingTT is a global HWND variable

case WM_INITDIALOG:

        InitCommonControls();
        g_hwndTrackingTT = CreateTrackingToolTip(IDC_BUTTON1, hDlg, L"");
        return TRUE;

case WM_MOUSELEAVE: // The mouse pointer has left our window. Deactivate the tooltip.
    
    SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)FALSE, (LPARAM)&g_toolItem);
    g_TrackingMouse = FALSE;
    return FALSE;

case WM_MOUSEMOVE:

    static int oldX, oldY;
    int newX, newY;

    if (!g_TrackingMouse)   // The mouse has just entered the window.
    {                       // Request notification when the mouse leaves.
    
        TRACKMOUSEEVENT tme = { sizeof(TRACKMOUSEEVENT) };
        tme.hwndTrack       = hDlg;
        tme.dwFlags         = TME_LEAVE;
        
        TrackMouseEvent(&tme);

        // Activate the tooltip.
        SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)TRUE, (LPARAM)&g_toolItem);
        
        g_TrackingMouse = TRUE;
    }

    newX = GET_X_LPARAM(lParam);
    newY = GET_Y_LPARAM(lParam);

    // Make sure the mouse has actually moved. The presence of the tooltip 
    // causes Windows to send the message continuously.
    
    if ((newX != oldX) || (newY != oldY))
    {
        oldX = newX;
        oldY = newY;
            
        // Update the text.
        WCHAR coords[12];
        swprintf_s(coords, ARRAYSIZE(coords), L"%d, %d", newX, newY);
        
        g_toolItem.lpszText = coords;
        SendMessage(g_hwndTrackingTT, TTM_SETTOOLINFO, 0, (LPARAM)&g_toolItem);

        // Position the tooltip. The coordinates are adjusted so that the tooltip does not overlap the mouse pointer.
        
        POINT pt = { newX, newY }; 
        ClientToScreen(hDlg, &pt);
        SendMessage(g_hwndTrackingTT, TTM_TRACKPOSITION, 0, (LPARAM)MAKELONG(pt.x + 10, pt.y - 20));
    }
    return FALSE;
```



## <a name="related-topics"></a><span data-ttu-id="64a3a-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64a3a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64a3a-135">Uso di controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="64a3a-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




