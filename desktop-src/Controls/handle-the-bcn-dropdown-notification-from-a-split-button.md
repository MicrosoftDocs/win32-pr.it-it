---
title: Gestire BCN_DROPDOWN notifiche da SplitButtons
description: In questo argomento viene descritta una possibile modalità di risposta alla \_ notifica a discesa BCN in una procedura di dialogo.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118554"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a>Come gestire la notifica a \_ discesa BCN da un pulsante di menu combinato

In questo argomento viene descritta una possibile modalità di risposta alla notifica a [ \_ discesa BCN](bcn-dropdown.md) in una procedura di dialogo.

L'applicazione C++ recupera le coordinate client del pulsante dall'intestazione della notifica e le converte in coordinate dello schermo. Viene quindi creato un menu popup che viene visualizzato nella parte inferiore del pulsante. Per semplificare l'esempio, i tasti di scelta rapida non sono implementati per il menu.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a>Passaggio 1: attendere la notifica *a \_ discesa BCN* .


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a>Passaggio 2: ottenere le coordinate dello schermo del pulsante.

Usare la funzione [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) per convertire le coordinate della finestra del bordo inferiore sinistro del pulsante in coordinate dello schermo.


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a>Passaggio 3: creare un menu e aggiungere elementi.

Utilizzare la funzione [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) per creare un menu. Utilizzare la funzione [**AppendMenu**](/windows/desktop/menurc/u) per aggiungere elementi al menu. IDC \_ MENUCOMMAND1 e IDC \_ MENUCOMMAND2 sono costanti definite dall'applicazione per i comandi di menu.


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a>Passaggio 4: visualizzare il menu.

La funzione [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) Visualizza un menu di scelta rapida nella posizione specificata e tiene traccia della selezione degli elementi nel menu.


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a>Esempio completo


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_Codice di notifica a discesa BCN](bcn-dropdown.md)
</dt> <dt>

[Informazioni sui pulsanti](about-buttons.md)
</dt> <dt>

[Riferimento al controllo Button](bumper-button-button-control-reference.md)
</dt> <dt>

[Uso di pulsanti](using-buttons.md)
</dt> <dt>

[Button](buttons.md)
</dt> </dl>

 

 