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
# <a name="how-to-display-tooltips-for-buttons"></a>Come visualizzare le descrizioni comandi per i pulsanti

Quando si specifica lo stile delle [**\_ descrizioni comandi di TBSTYLE**](toolbar-control-and-button-styles.md) , la barra degli strumenti crea e gestisce un controllo ToolTip. Il controllo ToolTip è nascosto e viene visualizzato solo quando gli utenti spostano il puntatore del mouse su un pulsante della barra degli strumenti e lo lasciano per circa un secondo.

L'applicazione può fornire testo al controllo ToolTip in uno dei modi seguenti:

-   Impostare il testo della descrizione comando **come membro della** struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) per ogni pulsante. È inoltre necessario inviare un messaggio [**TB \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md) e impostare le righe di testo massime su 0, in modo che il testo non venga visualizzato come etichetta del pulsante anziché come descrizione comando.
-   Creare la barra degli strumenti con lo stile [**\_ elenco TBSTYLE**](toolbar-control-and-button-styles.md) , quindi impostare lo stile esteso [**TBSTYLE \_ ex \_ MIXEDBUTTONS**](toolbar-extended-styles.md) . Le etichette vengono visualizzate solo per i pulsanti con lo stile di [**\_ SHOWTEXT BTNS**](toolbar-control-and-button-styles.md) . Per i pulsanti che non hanno questo stile, viene visualizzata una descrizione comando che contiene il testo del pulsante.
-   Rispondere al codice di notifica di [TTN \_ GETDISPINFO](ttn-getdispinfo.md) .
-   Rispondere al codice di notifica di [TBN \_ GETINFOTIP](tbn-getinfotip.md) .

Un'applicazione che deve inviare messaggi direttamente al controllo ToolTip può recuperare l'handle per il controllo usando il messaggio [**TB \_ GetToolTips**](tb-gettooltips.md) . Un'applicazione può sostituire il controllo ToolTip di una barra degli strumenti con un altro controllo ToolTip usando il messaggio [**TB \_ setooltips**](tb-settooltips.md) .

Il modo più flessibile per fornire il testo della descrizione comando consiste nel rispondere al codice di notifica [TTN \_ GETDISPINFO](ttn-getdispinfo.md) o [TBN \_ GETINFOTIP](tbn-getinfotip.md) inviato dal controllo Toolbar al relativo elemento padre sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . Per [TTN \_ GETDISPINFO](ttn-getdispinfo.md), il parametro *lParam* include un puntatore a una struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (definita anche **LPTOOLTIPTEXT**) che specifica l'identificatore di comando del pulsante per il quale è necessario il testo della guida. Questo identificatore si trova nel membro **NMTTDISPINFO. HDR. idFrom** . Un'applicazione può copiare il testo della guida nella struttura, specificare l'indirizzo di una stringa contenente il testo della guida o specificare l'handle dell'istanza e l'identificatore di risorsa di una risorsa di stringa.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="display-a-tooltip-for-a-button"></a>Visualizzare una descrizione comando per un pulsante

Il codice di esempio seguente gestisce il codice di notifica della descrizione comando [TTN \_ GETDISPINFO](ttn-getdispinfo.md) fornendo testo da identificatori di risorsa.


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

[Utilizzo di controlli Toolbar](using-toolbar-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




