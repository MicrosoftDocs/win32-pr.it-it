---
title: Come elaborare i messaggi di notifica TrackBar
description: I TrackBar inviano notifiche alla finestra padre delle azioni dell'utente inviando il messaggio padre a WM \_ HSCROLL o WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709007"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Come elaborare i messaggi di notifica TrackBar

I TrackBar inviano notifiche alla finestra padre delle azioni dell'utente inviando il messaggio padre a [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="process-trackbar-notification-messages"></a>Messaggi di notifica del processo TrackBar

L'esempio di codice seguente è una funzione che viene chiamata quando la finestra padre di TrackBar riceve un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) . Il TrackBar in questo esempio ha lo stile [**TBS \_ ENABLESELRANGE**](trackbar-control-styles.md) . La posizione del dispositivo di scorrimento viene confrontata con l'intervallo di selezione e il dispositivo di scorrimento viene spostato nella posizione iniziale o finale dell'intervallo di selezione, quando necessario.


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a>Commenti

Una finestra di dialogo che contiene un TrackBar di tipo con stile di visualizzazione di [**TBS \_**](trackbar-control-styles.md) può utilizzare questa funzione quando viene ricevuto un messaggio [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




