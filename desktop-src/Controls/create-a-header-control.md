---
title: Come creare un controllo Header
description: Questo argomento illustra come creare un controllo intestazione e posizionarlo all'interno dell'area client della finestra padre.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae5bb3ae9c323d30384f5d058a61393bf6425c2a27dfe67faa9cbedd4b3289e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063201"
---
# <a name="how-to-create-a-header-control"></a>Come creare un controllo Header

Questo argomento illustra come creare un controllo intestazione e posizionarlo all'interno dell'area client della finestra padre. È possibile creare un controllo intestazione usando la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificando la classe della finestra [**WC \_ HEADER**](common-control-window-classes.md) e gli stili [del controllo intestazione appropriati.](header-control-styles.md) Questa classe della finestra viene registrata quando viene caricata la DLL del controllo comune. Per assicurarsi che questa DLL sia caricata, usare la [**funzione InitCommonControlsEx.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Nell'esempio di codice C++ seguente viene innanzitutto chiamata la [**funzione InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) per caricare la DLL del controllo comune. Chiama quindi la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo intestazione. Il controllo è inizialmente nascosto. Il [**messaggio \_ LAYOUT HDM**](hdm-layout.md) viene usato per calcolare le dimensioni e la posizione del controllo all'interno della finestra padre. Il controllo viene quindi riposizionato e reso visibile.



```C++
// DoCreateHeader - creates a header control that is positioned along 
//     the top of the parent window's client area. 
// Returns the handle to the header control. 
// hwndParent - handle to the parent window. 
// 
// Global variable 
//    g_hinst - handle to the application instance 
extern HINSTANCE g_hinst; 
//
// child-window identifier
int ID_HEADER;
//
HWND DoCreateHeader(HWND hwndParent) 
{ 
        HWND hwndHeader; 
        RECT rcParent; 
        HDLAYOUT hdl; 
        WINDOWPOS wp; 
 
        // Ensure that the common control DLL is loaded, and then create 
        // the header control. 
        INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
        icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
        icex.dwICC = ICC_LISTVIEW_CLASSES;   //set dwICC member to ICC_LISTVIEW_CLASSES    
                                             // this loads list-view and header control classes.
    InitCommonControlsEx(&icex); 
 
        if ((hwndHeader = CreateWindowEx(0, WC_HEADER, (LPCTSTR) NULL, 
                WS_CHILD | WS_BORDER | HDS_BUTTONS | HDS_HORZ, 
                0, 0, 0, 0, hwndParent, (HMENU) ID_HEADER, g_hinst, 
                (LPVOID) NULL)) == NULL) 
            return (HWND) NULL; 
 
        // Retrieve the bounding rectangle of the parent window's 
        // client area, and then request size and position values 
        // from the header control. 
        GetClientRect(hwndParent, &rcParent); 
 
        hdl.prc = &rcParent; 
        hdl.pwpos = &wp; 
        if (!SendMessage(hwndHeader, HDM_LAYOUT, 0, (LPARAM) &hdl)) 
            return (HWND) NULL; 
 
        // Set the size, position, and visibility of the header control. 
        SetWindowPos(hwndHeader, wp.hwndInsertAfter, wp.x, wp.y, 
            wp.cx, wp.cy, wp.flags | SWP_SHOWWINDOW); 
 
        return hwndHeader; 
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli intestazione](header-controls.md)
</dt> <dt>

[Informazioni di riferimento sul controllo Header](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Uso dei controlli intestazione](using-header-controls.md)
</dt> </dl>

 

 