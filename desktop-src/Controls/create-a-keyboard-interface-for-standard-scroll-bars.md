---
title: Come creare un'interfaccia della tastiera per le barre di scorrimento standard
description: Anche se un controllo barra di scorrimento fornisce un'interfaccia della tastiera incorporata, una barra di scorrimento standard non lo fa.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25994639a40a6380bbf2f9cc0075e8a78b9e15787dbdf1babf0e6a15550faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698741"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a>Come creare un'interfaccia della tastiera per le barre di scorrimento standard

Anche se un controllo barra di scorrimento fornisce un'interfaccia della tastiera incorporata, una barra di scorrimento standard non lo fa. Per implementare un'interfaccia della tastiera per una barra di scorrimento standard, una routine della finestra deve elaborare il [**messaggio WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) ed esaminare il codice del tasto virtuale specificato dal *parametro wParam.* Se il codice del tasto virtuale corrisponde a un tasto di direzione, la routine della finestra invia a se stessa un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con la parola di ordine basso del *parametro wParam* impostata sul codice di richiesta della barra di scorrimento appropriato.

Ad esempio, quando l'utente preme il tasto freccia SU, la routine della finestra riceve un messaggio [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) con *wParam* uguale a VK \_ UP. In risposta, la routine della finestra invia a se stessa un messaggio [**WM \_ VSCROLL**](wm-vscroll.md) con la parola di ordine basso *di wParam* impostata sul codice della richiesta SB \_ LINEUP.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a>Creare un'interfaccia da tastiera per una barra di scorrimento standard

Nell'esempio di codice seguente viene illustrato come includere un'interfaccia della tastiera per una barra di scorrimento standard.


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle barre di scorrimento](using-scroll-bars.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 