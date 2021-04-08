---
title: Come incorporare controlli non Button nelle barre degli strumenti
description: Le barre degli strumenti supportano solo i pulsanti; Pertanto, se l'applicazione richiede un tipo di controllo diverso, è necessario creare una finestra figlio. Nella figura seguente è illustrata una barra degli strumenti con un controllo di modifica incorporato.
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ae2189350b9ea2f4aaa0c3ea0b49727bd3415
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103872219"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a>Come incorporare controlli non Button nelle barre degli strumenti

Le barre degli strumenti supportano solo i pulsanti; Pertanto, se l'applicazione richiede un tipo di controllo diverso, è necessario creare una finestra figlio. Nella figura seguente è illustrata una barra degli strumenti con un controllo di modifica incorporato.

![Screenshot di una finestra di dialogo con un controllo di modifica nella barra degli strumenti, che precede tre icone della barra degli strumenti](images/tb-withedit.png)

> [!Note]  
> Si consiglia di usare i [controlli Rebar](rebar-controls.md) anziché posizionare i controlli nelle barre degli strumenti.

 

Qualsiasi tipo di finestra può essere posizionata su una barra degli strumenti. Il codice di esempio seguente aggiunge un controllo di modifica come figlio della finestra di controllo della barra degli strumenti. Poiché la barra degli strumenti è stata creata e quindi il controllo di modifica è stato aggiunto, è necessario fornire spazio per il controllo di modifica. Un modo per eseguire questa operazione consiste nell'aggiungere un separatore come segnaposto nella barra degli strumenti, impostando la larghezza del separatore sul numero di pixel che si desidera riservare.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a>Incorporare un controllo non Button in una barra degli strumenti

Il frammento di codice seguente crea la barra degli strumenti nella figura precedente.


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



In questo esempio vengono hardcoded i codici delle dimensioni della finestra figlio; Tuttavia, per creare un'applicazione più affidabile, determinare la dimensione della barra degli strumenti e fare in modo che la finestra di controllo di modifica si adatti.

È possibile che le notifiche dei controlli di modifica passino a un'altra finestra, ad esempio l'elemento padre della barra degli strumenti. A tale scopo, creare il controllo di modifica come figlio della finestra padre della barra degli strumenti. Modificare quindi l'elemento padre del controllo di modifica sulla barra degli strumenti come indicato di seguito.


```
SetParent (hWndEdit, hWndToolbar);
```



Le notifiche vengono inviate all'elemento padre originale. Pertanto, i messaggi di controllo di modifica passano all'elemento padre della barra degli strumenti anche se la finestra di modifica risiede nella finestra della barra degli strumenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di controlli Toolbar](using-toolbar-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




