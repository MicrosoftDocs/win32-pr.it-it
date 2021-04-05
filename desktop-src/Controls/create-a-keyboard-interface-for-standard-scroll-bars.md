---
title: Come creare un'interfaccia della tastiera per le barre di scorrimento standard
description: Anche se un controllo barra di scorrimento fornisce un'interfaccia di tastiera incorporata, non è presente una barra di scorrimento standard.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103873005"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a>Come creare un'interfaccia della tastiera per le barre di scorrimento standard

Anche se un controllo barra di scorrimento fornisce un'interfaccia di tastiera incorporata, non è presente una barra di scorrimento standard. Per implementare un'interfaccia della tastiera per una barra di scorrimento standard, una routine della finestra deve elaborare il messaggio di [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) ed esaminare il codice della chiave virtuale specificato dal parametro *wParam* . Se il codice della chiave virtuale corrisponde a un tasto di direzione, la routine della finestra Invia a se stessa un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con la parola meno ordinata del parametro *wParam* impostato sul codice di richiesta della barra di scorrimento appropriato.

Ad esempio, quando l'utente preme il tasto freccia su, la routine della finestra riceve un messaggio [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) con *wParam* uguale a VK \_ . In risposta, la routine della finestra Invia a se stessa un messaggio [**WM \_ VSCROLL**](wm-vscroll.md) con la parola di ordine inferiore di *wParam* impostata sul \_ codice della richiesta di lineup SB.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a>Creare un'interfaccia di tastiera per una barra di scorrimento standard

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

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 