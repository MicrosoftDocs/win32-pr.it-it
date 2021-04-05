---
title: Come creare controlli Rebar
description: Un'applicazione crea un controllo Rebar chiamando la funzione CreateWindowEx, specificando REBARCLASSNAME come classe Window.
ms.assetid: F17CC2A4-BDC6-48A6-9AF5-19FCF65CC39A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b38cd49e8e6016dafad5ec07c77be570a5a430
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730442"
---
# <a name="how-to-create-rebar-controls"></a>Come creare controlli Rebar

Un'applicazione crea un controllo Rebar chiamando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando [**REBARCLASSNAME**](common-control-window-classes.md) come classe Window. Per prima cosa, l'applicazione deve registrare la classe della finestra chiamando la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , specificando il bit per le classi di accesso sporadico di ICC \_ \_ nella struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) associata.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="create-a-rebar-control"></a>Creare un controllo Rebar

Nell'esempio seguente viene creato un controllo Rebar con due bande, una contenente una casella combinata e un'altra contenente una barra degli strumenti. Vedere l'illustrazione in [informazioni sui controlli Rebar](rebar-controls.md). Questi controlli vengono creati separatamente e vengono passati alla funzione di esempio come parametri.


```C++
#define NUMBUTTONS 3

HWND CreateRebar(HWND hwndOwner, HWND hwndToolbar, HWND hwndCombo)
{
    // Check parameters.
    if ((hwndToolbar == NULL) || (hwndCombo == NULL))
    {
        return NULL;
    }

    // Initialize common controls.
    INITCOMMONCONTROLSEX icex;
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC   = ICC_COOL_CLASSES | ICC_BAR_CLASSES;
    InitCommonControlsEx(&icex);

    // Create the rebar.
    HWND hwndRebar = CreateWindowEx(WS_EX_TOOLWINDOW,
        REBARCLASSNAME,
        NULL,
        WS_CHILD | WS_VISIBLE | WS_CLIPSIBLINGS |
        WS_CLIPCHILDREN | RBS_VARHEIGHT |
        CCS_NODIVIDER | RBS_BANDBORDERS,
        0,0,0,0,
        hwndOwner,
        NULL,
        g_hInst, // global instance handle
        NULL);

    if(!hwndRebar)
    {
        return NULL;
    }

    // Initialize band info used by both bands.
    REBARBANDINFO rbBand = { sizeof(REBARBANDINFO) };
    rbBand.fMask  = 
          RBBIM_STYLE       // fStyle is valid.
        | RBBIM_TEXT        // lpText is valid.
        | RBBIM_CHILD       // hwndChild is valid.
        | RBBIM_CHILDSIZE   // child size members are valid.
        | RBBIM_SIZE;       // cx is valid
    rbBand.fStyle = RBBS_CHILDEDGE | RBBS_GRIPPERALWAYS;  

    // Get the height of the toolbar.
    DWORD dwBtnSize = (DWORD)SendMessage(hwndToolbar, TB_GETBUTTONSIZE, 0,0);

    // Set values unique to the band with the toolbar.
    rbBand.lpText = TEXT("");
    rbBand.hwndChild = hwndToolbar;
    rbBand.cyChild = LOWORD(dwBtnSize);
    rbBand.cxMinChild = NUMBUTTONS * HIWORD(dwBtnSize);
    rbBand.cyMinChild = LOWORD(dwBtnSize);
    // The default width is the width of the buttons.
    rbBand.cx = 0;

    // Add the band that has the toolbar.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);

    // Set values unique to the band with the combo box.
    RECT rc;
    GetWindowRect(hwndCombo, &rc);
    rbBand.lpText = TEXT("Font");
    rbBand.hwndChild = hwndCombo;
    rbBand.cxMinChild = 0;
    rbBand.cyMinChild = rc.bottom - rc.top;
    // The default width should be set to some value wider than the text. The combo 
    // box itself will expand to fill the band.
    rbBand.cx = 100;

    // Add the band that has the combo box.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);
    
    return (hwndRebar);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rebar](using-rebar-controls.md)
</dt> <dt>

[Informazioni sui controlli Rebar](rebar-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 