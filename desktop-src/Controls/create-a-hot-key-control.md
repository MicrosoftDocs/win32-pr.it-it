---
title: Come creare un controllo tasto di scelta
description: In questo argomento viene illustrato come creare un controllo tasto di scelta. Per creare un controllo del tasto di scelta rapida, utilizzare la funzione CreateWindowEx, specificando la classe della finestra di scelta rapida \_ .
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498005efcdfbbf001283551bbeea4906ebc854cf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103873141"
---
# <a name="how-to-create-a-hot-key-control"></a>Come creare un controllo tasto di scelta

In questo argomento viene illustrato come creare un controllo tasto di scelta. Per creare un controllo del tasto di scelta rapida, utilizzare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra di scelta rapida \_ .

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Prima di creare il controllo tasto di scelta, verificare che la DLL dei controlli comuni sia caricata.

Nell'esempio di codice C++ riportato di seguito, la funzione definita dall'applicazione chiama la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) per caricare la dll del controllo comune. Chiama quindi la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra della **\_ classe hotkey** , per creare un controllo tasto di scelta. USA i messaggi [**HKM \_**](hkm-setrules.md) e [**HKM \_ sehotkey**](hkm-sethotkey.md) per inizializzare il controllo e restituisce un handle per il controllo.

Questo controllo tasto di scelta non consente all'utente di scegliere un tasto di scelta che è una singola chiave non modificata, né consente all'utente di scegliere solo MAIUSC e una chiave. Queste regole impediscono efficacemente all'utente di scegliere un tasto di scelta che potrebbe essere immesso accidentalmente durante la digitazione del testo.



```C++
// Creates a hot key control and sets rules and default settings for it.
// 
// Returns the handle of the hot key control. 
//
// Parameter
//     hwndDlg - Handle of the parent window (dialog box). 
// 
// Global variable 
//     g_hinst - Handle of the application instance. 

extern HINSTANCE g_hinst; 

HWND WINAPI InitializeHotkey(HWND hwndDlg) 
{ 
    HWND hwndHot = NULL;
    
    // Ensure that the common control DLL is loaded. 
    INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_HOTKEY_CLASS;   //set dwICC member to ICC_HOTKEY_CLASS    
                                     // this loads the Hot Key control class.
    InitCommonControlsEx(&icex);  
 
    hwndHot = CreateWindowEx(0,                        // no extended styles 
                             HOTKEY_CLASS,             // class name 
                             TEXT(""),                 // no title (caption) 
                             WS_CHILD | WS_VISIBLE,    // style 
                             15, 10,                   // position 
                             200, 20,                  // size 
                             hwndDlg,                  // parent window 
                             NULL,                     // uses class menu 
                             g_hinst,                  // instance 
                             NULL);                    // no WM_CREATE parameter 
 
    SetFocus(hwndHot); 
 
    // Set rules for invalid key combinations. If the user does not supply a
    // modifier key, use ALT as a modifier. If the user supplies SHIFT as a 
    // modifier key, use SHIFT + ALT instead.
    SendMessage(hwndHot, 
                HKM_SETRULES, 
                (WPARAM) HKCOMB_NONE | HKCOMB_S,   // invalid key combinations 
                MAKELPARAM(HOTKEYF_ALT, 0));       // add ALT to invalid entries 
 
    // Set CTRL + ALT + A as the default hot key for this window. 
    // 0x41 is the virtual key code for 'A'. 
    SendMessage(hwndHot, 
                HKM_SETHOTKEY, 
                MAKEWORD(0x41, HOTKEYF_CONTROL | HOTKEYF_ALT), 
                0); 
 
    return hwndHot; 
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo del tasto di scelta](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Informazioni sui controlli tasto di scelta](hot-key-controls.md)
</dt> <dt>

[Uso di controlli tasto di scelta](using-hot-key-controls.md)
</dt> </dl>

 

 