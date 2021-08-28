---
title: Come creare un controllo tasto di scelta rapida
description: In questo argomento viene illustrato come creare un controllo tasto di scelta rapida. È possibile creare un controllo tasto di scelta rapida usando la funzione CreateWindowEx, specificando la classe della finestra HOTKEY \_ CLASS.
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081db39f07e8d80fcbb5a437bc8cbe83473b4299282c8b2437d95acda02b2db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577042"
---
# <a name="how-to-create-a-hot-key-control"></a>Come creare un controllo tasto di scelta rapida

In questo argomento viene illustrato come creare un controllo tasto di scelta rapida. È possibile creare un controllo tasto di scelta rapida [**usando la funzione CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) specificando la classe della finestra HOTKEY \_ CLASS.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Prima di creare il controllo tasto di scelta rapida, assicurarsi che la DLL dei controlli comuni sia caricata.

Nell'esempio di codice C++ seguente la funzione definita dall'applicazione chiama la [**funzione InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) per caricare la DLL del controllo comune. Chiama quindi la funzione [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) specificando la classe della finestra **HOTKEY \_ CLASS,** per creare un controllo tasto di scelta rapida. Usa i [**messaggi HKM \_ SETRULES**](hkm-setrules.md) e [**HKM \_ SETHOTKEY**](hkm-sethotkey.md) per inizializzare il controllo e restituisce un handle al controllo.

Questo controllo del tasto di scelta non consente all'utente di scegliere un tasto di scelta rapida che è un singolo tasto non modificato, né consente all'utente di scegliere solo MAIUSC e un tasto. Queste regole impediscono in effetti all'utente di scegliere un tasto di scelta rapida che potrebbe essere immesso accidentalmente durante la digitazione di testo.



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

[Informazioni di riferimento sul controllo tasto di scelta rapida](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Informazioni sui controlli dei tasti di scelta rapida](hot-key-controls.md)
</dt> <dt>

[Uso dei controlli tasto di scelta rapida](using-hot-key-controls.md)
</dt> </dl>

 

 