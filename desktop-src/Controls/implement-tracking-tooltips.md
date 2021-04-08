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
# <a name="how-to-implement-tracking-tooltips"></a>Come implementare le descrizioni comandi di rilevamento

Le descrizioni comandi di rilevamento rimangono visibili fino a quando non vengono chiuse in modo esplicito dall'applicazione e possono modificare la posizione sullo schermo in modo dinamico. Sono supportati dalla [versione 4,70](common-control-versions.md) e successive dei controlli comuni.

Per creare una descrizione comando di rilevamento, includere il \_ flag di traccia ttf nel membro **uFlags** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) quando si invia il messaggio [**TTM \_ ADDTOOL**](ttm-addtool.md) .

L'applicazione deve attivare manualmente (mostrare) e disattivare (nascondere) una descrizione comando di rilevamento inviando un messaggio [**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md) . Mentre una descrizione comando di rilevamento è attiva, l'applicazione deve specificare il percorso della descrizione comando inviando messaggi [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) al controllo ToolTip. Poiché l'applicazione gestisce le attività, ad esempio il posizionamento della descrizione comando, le descrizioni comandi di rilevamento non usano il flag della **\_ sottoclasse ttf** o il messaggio [**TTM \_ RELAYEVENT**](ttm-relayevent.md) .

Il messaggio [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) fa sì che il controllo ToolTip visualizzi la finestra usando uno dei due stili di selezione host:

-   Per impostazione predefinita, la descrizione comando viene visualizzata accanto allo strumento corrispondente in una posizione scelta dal controllo. Il percorso scelto è relativo alle coordinate fornite mediante questo messaggio.
-   Se si include il **valore \_ assoluto ttf** nel membro della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , la descrizione comando viene visualizzata in corrispondenza della posizione in pixel specificata nel messaggio. In questo caso, il controllo non tenta di modificare la posizione della finestra della descrizione comando dalle coordinate fornite.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="implement-in-place-tooltips"></a>Implementare descrizioni comando In-Place

Il membro **uFlags** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) utilizzata nell'esempio include il flag **\_ assoluto ttf** . Senza questo flag, il controllo ToolTip sceglie dove visualizzare la descrizione comando e la relativa posizione rispetto alla finestra di dialogo può cambiare improvvisamente quando il puntatore del mouse viene spostato.

> [!Note]  
> `g_toolItem` è una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) globale.

 

Nell'esempio seguente viene illustrato come creare un controllo ToolTip di rilevamento. Nell'esempio viene specificata l'intera area client della finestra principale come strumento.


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



### <a name="window-procedure-implementation"></a>Implementazione della routine della finestra

Quando il puntatore del mouse si trova all'interno dell'area client, la descrizione comando è attiva e visualizza le coordinate del cursore, come illustrato nella figura seguente.

![Screenshot di una finestra di dialogo; una descrizione comando Visualizza le coordinate x e y del puntatore del mouse](images/tt-tracking.png)

Il codice di esempio seguente è riportato nella procedura della finestra per una finestra di dialogo in cui viene visualizzata la descrizione comando di rilevamento creata nell'esempio precedente. La variabile booleana globale *g \_ TrackingMouse* viene utilizzata per determinare se è necessario riattivare la descrizione comando e reimpostare il rilevamento del mouse in modo che l'applicazione riceva una notifica quando il puntatore del mouse esce dall'area client della finestra di dialogo.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 




