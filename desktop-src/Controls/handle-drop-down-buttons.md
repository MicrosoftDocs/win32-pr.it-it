---
title: Come gestire i pulsanti a discesa
description: Un pulsante a discesa può presentare agli utenti un elenco di opzioni.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74443b0d29b3ab39255d7417fd13677769f6a762ebe176e8301a76029db0c37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544952"
---
# <a name="how-to-handle-drop-down-buttons"></a>Come gestire i pulsanti a discesa

Un pulsante a discesa può presentare agli utenti un elenco di opzioni. Per creare questo stile di pulsante, specificare lo stile [**BTNS \_ DROPDOWN**](toolbar-control-and-button-styles.md) (denominato [**anche TBSTYLE \_ DROPDOWN**](toolbar-control-and-button-styles.md) per la compatibilità con le versioni precedenti dei controlli comuni). Per visualizzare un pulsante a discesa con una freccia, è necessario impostare anche lo stile della barra degli strumenti [**TBSTYLE \_ EX \_ DRAWDDARROWS**](toolbar-extended-styles.md) inviando un messaggio [**TB \_ SETEXTENDEDSTYLE.**](tb-setextendedstyle.md)

La figura seguente mostra un pulsante "Apri" a discesa con il menu di scelta rapida aperto e un elenco di file. In questo esempio la barra degli strumenti ha lo stile [**TBSTYLE \_ EX \_ DRAWDDARROWS.**](toolbar-extended-styles.md)

![screenshot di una finestra di dialogo con tre elementi della barra degli strumenti rappresentati da icone; uno ha una freccia a discesa espansa e un menu di scelta rapida a tre elementi](images/tb-dropdown.png)

La figura seguente mostra la stessa barra degli strumenti, questa volta senza lo stile [**TBSTYLE \_ EX \_ DRAWDDARROWS.**](toolbar-extended-styles.md)

![Screenshot di una finestra di dialogo precedente, ma l'icona con il menu di scelta rapida non ha una freccia a discesa](images/tb-dropdown2.png)

Quando gli utenti fa clic su un pulsante della barra degli strumenti che usa lo stile [**BTNS \_ DROPDOWN,**](toolbar-control-and-button-styles.md) il controllo della barra degli strumenti invia alla finestra padre un codice di notifica [TBN \_ DROPDOWN.](tbn-dropdown.md)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="handle-a-drop-down-button"></a>Gestire un pulsante a discesa

Nell'esempio di codice seguente viene illustrato come un'applicazione può supportare un pulsante a discesa in un controllo barra degli strumenti.


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

[Uso dei controlli barra degli strumenti](using-toolbar-controls.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




