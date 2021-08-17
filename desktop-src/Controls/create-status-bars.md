---
title: Come creare barre di stato
description: È possibile creare una barra di stato usando la funzione CreateStatusWindow o la funzione CreateWindowEx e specificando la classe di finestra STATUSCLASSNAME.
ms.assetid: 4ED4BFD3-904D-4198-8152-5DD13CA7C189
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7075c8d8896d59a5711d5ee80be4af90948ee4ee99a441fbbf1140cd7452c4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413189"
---
# <a name="how-to-create-status-bars"></a>Come creare barre di stato

È possibile creare una barra di stato usando la [**funzione CreateStatusWindow**](/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa) o la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificando la classe di finestra [**STATUSCLASSNAME.**](common-control-window-classes.md)

Dopo aver creato la barra di stato, è possibile dividerla in parti, impostare il testo per ogni parte e controllare l'aspetto della finestra usando i messaggi della barra di stato.

> [!Note]  
> Per assicurarsi che la DLL del controllo comune sia caricata, usare [**prima la funzione InitCommonControls.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)

 

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="create-a-status-bar"></a>Creare una barra di stato

Nell'esempio seguente viene illustrato come creare una barra di stato con un ridimensionamento e dividere la finestra in quattro parti uguali in base alla larghezza dell'area client della finestra padre.


```C++
// Description: 
//   Creates a status bar and divides it into the specified number of parts.
// Parameters:
//   hwndParent - parent window for the status bar.
//   idStatus - child window identifier of the status bar.
//   hinst - handle to the application instance.
//   cParts - number of parts into which to divide the status bar.
// Returns:
//   The handle to the status bar.
//
HWND DoCreateStatusBar(HWND hwndParent, int idStatus, HINSTANCE
                      hinst, int cParts)
{
    HWND hwndStatus;
    RECT rcClient;
    HLOCAL hloc;
    PINT paParts;
    int i, nWidth;

    // Ensure that the common control DLL is loaded.
    InitCommonControls();

    // Create the status bar.
    hwndStatus = CreateWindowEx(
        0,                       // no extended styles
        STATUSCLASSNAME,         // name of status bar class
        (PCTSTR) NULL,           // no text when first created
        SBARS_SIZEGRIP |         // includes a sizing grip
        WS_CHILD | WS_VISIBLE,   // creates a visible child window
        0, 0, 0, 0,              // ignores size and position
        hwndParent,              // handle to parent window
        (HMENU) idStatus,       // child window identifier
        hinst,                   // handle to application instance
        NULL);                   // no window creation data

    // Get the coordinates of the parent window's client area.
    GetClientRect(hwndParent, &rcClient);

    // Allocate an array for holding the right edge coordinates.
    hloc = LocalAlloc(LHND, sizeof(int) * cParts);
    paParts = (PINT) LocalLock(hloc);

    // Calculate the right edge coordinate for each part, and
    // copy the coordinates to the array.
    nWidth = rcClient.right / cParts;
    int rightEdge = nWidth;
    for (i = 0; i < cParts; i++) { 
       paParts[i] = rightEdge;
       rightEdge += nWidth;
    }

    // Tell the status bar to create the window parts.
    SendMessage(hwndStatus, SB_SETPARTS, (WPARAM) cParts, (LPARAM)
               paParts);

    // Free the array, and return.
    LocalUnlock(hloc);
    LocalFree(hloc);
    return hwndStatus;
}  
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle barre di stato](using-status-bars.md)
</dt> <dt>

[Windows demo di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 