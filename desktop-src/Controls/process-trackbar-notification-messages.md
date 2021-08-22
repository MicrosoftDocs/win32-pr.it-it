---
title: Come elaborare i messaggi di notifica trackbar
description: I trackbar notificano alla finestra padre le azioni dell'utente inviando all'elemento padre un messaggio WM \_ HSCROLL o WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211a468c5c107a96fc6b28d12feed219799450828db07be87cd8887b5816bd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540321"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Come elaborare i messaggi di notifica trackbar

I trackbar notificano alla finestra padre le azioni dell'utente inviando all'elemento padre un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="process-trackbar-notification-messages"></a>Elaborare i messaggi di notifica di Trackbar

L'esempio di codice seguente è una funzione che viene chiamata quando la finestra padre del trackbar riceve un [**messaggio WM \_ HSCROLL.**](wm-hscroll.md) Il trackbar in questo esempio ha lo [**stile \_ TBS ENABLESELRANGE.**](trackbar-control-styles.md) La posizione del dispositivo di scorrimento viene confrontata con l'intervallo di selezione e il dispositivo di scorrimento viene spostato nella posizione iniziale o finale dell'intervallo di selezione quando necessario.


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

Una finestra di dialogo che contiene un trackbar in stile [**TBS \_ VERT**](trackbar-control-styles.md) può usare questa funzione quando riceve un [**messaggio WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli Trackbar](using-trackbar-controls.md)
</dt> </dl>

 

 




