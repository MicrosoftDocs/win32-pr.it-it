---
title: Come recuperare e impostare un tasto di scelta rapida
description: In questo argomento viene illustrato come recuperare o impostare la combinazione di tasti per un controllo tasto di scelta rapida.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac5d0bab71fea11fe3d2aba23405f6d7ee7fb1ed8c78f2578f034ae9c84cad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079495"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a>Come recuperare e impostare un tasto di scelta rapida

In questo argomento viene illustrato come recuperare o impostare la combinazione di tasti per un controllo tasto di scelta rapida. Il [**messaggio HKM \_ SETHOTKEY**](hkm-sethotkey.md) consente a un'applicazione di impostare la combinazione di tasti di scelta rapida per un controllo tasto di scelta rapida. Le applicazioni usano [**il messaggio \_ HKM GETHOTKEY**](hkm-gethotkey.md) per recuperare il codice del tasto virtuale e i flag di modifica del tasto di scelta rapida scelto dall'utente.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Usare il [**messaggio HKM \_ GETHOTKEY**](hkm-gethotkey.md) per recuperare il codice del tasto virtuale e i tasti di modifica che descrivono un tasto di scelta rapida scelto dall'utente. Usare il [**messaggio HKM \_ SETHOTKEY**](hkm-sethotkey.md) per impostare tali valori per un tasto di scelta rapida.

Nell'esempio di codice C++ seguente la funzione definita dall'applicazione usa il messaggio [**\_ HKM GETHOTKEY**](hkm-gethotkey.md) per recuperare una combinazione di tasti da un controllo tasto di scelta rapida e quindi usa il messaggio [**WM \_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) per impostare un tasto di scelta rapida globale. Si noti che non è possibile impostare un tasto di scelta rapida globale per una finestra con lo stile di finestra [**\_ WS CHILD.**](/windows/desktop/winmsg/window-styles)



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
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

 

 