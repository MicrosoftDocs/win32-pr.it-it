---
title: Come visualizzare le descrizioni comando per i pulsanti
description: Quando si specifica lo stile TBSTYLE TOOLTIPS, la barra degli strumenti \_ crea e gestisce un controllo descrizione comando. Il controllo descrizione comando è nascosto e viene visualizzato solo quando gli utenti spostano il puntatore su un pulsante della barra degli strumenti e lo lasciano per circa un secondo.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f169c6cc9324c98ed085b38f14802fcaa3c5cfbc8bd7ee9aa29af62ef41a6adc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320001"
---
# <a name="how-to-display-tooltips-for-buttons"></a>Come visualizzare le descrizioni comando per i pulsanti

Quando si specifica lo stile [**TBSTYLE \_ TOOLTIPS,**](toolbar-control-and-button-styles.md) la barra degli strumenti crea e gestisce un controllo descrizione comando. Il controllo descrizione comando è nascosto e viene visualizzato solo quando gli utenti spostano il puntatore su un pulsante della barra degli strumenti e lo lasciano per circa un secondo.

L'applicazione può fornire testo al controllo descrizione comando in uno dei modi seguenti:

-   Impostare il testo della descrizione comando **come membro iString** della [**struttura TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) per ogni pulsante. È anche necessario inviare un messaggio [**\_ TB SETMAXTEXTROWS**](tb-setmaxtextrows.md) e impostare il numero massimo di righe di testo su 0, in modo che il testo non venga visualizzato come etichetta del pulsante anziché come descrizione comando.
-   Creare la barra degli strumenti con lo stile [**TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) e quindi impostare lo stile [**esteso TBSTYLE \_ EX \_ MIXEDBUTTONS.**](toolbar-extended-styles.md) Le etichette vengono visualizzate solo per i pulsanti con [**lo stile \_ BTNS SHOWTEXT.**](toolbar-control-and-button-styles.md) Per i pulsanti che non hanno questo stile, viene visualizzata una descrizione comando che contiene il testo del pulsante.
-   Rispondere al codice [di notifica TTN \_ GETDISPINFO.](ttn-getdispinfo.md)
-   Rispondere al [codice di notifica TBN \_ GETINFOTIP.](tbn-getinfotip.md)

Un'applicazione che deve inviare messaggi direttamente al controllo descrizione comando può recuperare l'handle al controllo usando il messaggio [**\_ TB GETTOOLTIPS.**](tb-gettooltips.md) Un'applicazione può sostituire il controllo descrizione comando di una barra degli strumenti con un altro controllo descrizione comando usando il messaggio [**\_ TB SETTOOLTIPS.**](tb-settooltips.md)

Il modo più flessibile per fornire il testo della descrizione comando è rispondere al codice di notifica [TTN \_ GETDISPINFO](ttn-getdispinfo.md) o [TBN \_ GETINFOTIP](tbn-getinfotip.md) inviato dal controllo barra degli strumenti al relativo elemento padre sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) Per [TTN \_ GETDISPINFO,](ttn-getdispinfo.md)il *parametro lParam* include un puntatore a una struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (definita anche **come LPTOOLTIPTEXT**) che specifica l'identificatore di comando del pulsante per cui è necessario il testo della Guida. Questo identificatore si trova nel **membro NMTTDISPINFO.hdr.idFrom.** Un'applicazione può copiare il testo della Guida nella struttura , specificare l'indirizzo di una stringa contenente il testo della Guida oppure specificare l'handle di istanza e l'identificatore di risorsa di una risorsa stringa.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="display-a-tooltip-for-a-button"></a>Visualizzare una descrizione comando per un pulsante

Il codice di esempio seguente gestisce il codice di notifica della descrizione comando [ \_ GETDISPINFO TTN](ttn-getdispinfo.md) fornendo testo dagli identificatori di risorsa.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli barra degli strumenti](using-toolbar-controls.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




