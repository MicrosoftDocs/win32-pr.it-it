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
# <a name="how-to-handle-drop-down-buttons"></a>Come gestire i pulsanti a discesa

Un pulsante a discesa può presentare agli utenti un elenco di opzioni. Per creare questo stile di pulsante, specificare lo stile dell' [**\_ elenco a discesa BTNS**](toolbar-control-and-button-styles.md) (detto anche [**elenco a \_ discesa TBSTYLE**](toolbar-control-and-button-styles.md) per la compatibilità con le versioni precedenti dei controlli comuni). Per visualizzare un pulsante a discesa con una freccia, è necessario impostare anche lo stile della barra degli strumenti [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) inviando un messaggio [**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md) .

Nella figura seguente viene mostrato un pulsante a discesa "Apri" con il menu di scelta rapida aperto e viene visualizzato un elenco di file. In questo esempio, la barra degli strumenti ha lo stile [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .

![Screenshot di una finestra di dialogo con tre elementi della barra degli strumenti rappresentati da icone; uno ha una freccia a discesa espansa e un menu di scelta rapida di tre elementi](images/tb-dropdown.png)

La figura seguente mostra la stessa barra degli strumenti, questa volta senza lo stile [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) .

![Screenshot di una finestra di dialogo precedente, ma l'icona con il menu di scelta rapida non dispone di una freccia a discesa](images/tb-dropdown2.png)

Quando gli utenti fanno clic su un pulsante della barra degli strumenti che usa lo stile a [**\_ discesa BTNS**](toolbar-control-and-button-styles.md) , il controllo Toolbar invia la finestra padre a un codice di notifica a [ \_ discesa TBN](tbn-dropdown.md) .

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="handle-a-drop-down-button"></a>Gestire un pulsante a discesa

Nell'esempio di codice seguente viene illustrato come un'applicazione può supportare un pulsante a discesa in un controllo Toolbar.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di controlli Toolbar](using-toolbar-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




