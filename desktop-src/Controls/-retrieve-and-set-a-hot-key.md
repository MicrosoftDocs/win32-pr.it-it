---
title: Come recuperare e impostare un tasto di scelta
description: In questo argomento viene illustrato come recuperare o impostare la combinazione di tasti per un controllo tasto di scelta.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300696"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a>Come recuperare e impostare un tasto di scelta

In questo argomento viene illustrato come recuperare o impostare la combinazione di tasti per un controllo tasto di scelta. Il [**messaggio \_ sehotkey HKM**](hkm-sethotkey.md) consente a un'applicazione di impostare la combinazione di tasti di scelta rapida per un controllo tasto di scelta. Le applicazioni utilizzano il messaggio [**\_ GetHotKey HKM**](hkm-gethotkey.md) per recuperare il codice della chiave virtuale e i flag di modifica del tasto di scelta rapida scelto dall'utente.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Usare il [**messaggio \_ GetHotKey HKM**](hkm-gethotkey.md) per recuperare il codice della chiave virtuale e i tasti di modifica che descrivono un tasto di scelta rapida scelto dall'utente. Usare il messaggio [**HKM \_ sehotkey**](hkm-sethotkey.md) per impostare i valori per un tasto di scelta.

Nell'esempio di codice C++ riportato di seguito, la funzione definita dall'applicazione usa il messaggio [**\_ GetHotKey HKM**](hkm-gethotkey.md) per recuperare una combinazione di tasti da un controllo tasto di scelta rapida e quindi usa il messaggio per impostare un tasto di [**scelta rapida globale \_**](/windows/desktop/inputdev/wm-sethotkey) . Si noti che non è possibile impostare un tasto di scelta rapida globale per una finestra con lo stile della finestra [**\_ figlio WS**](/windows/desktop/winmsg/window-styles) .



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

[Riferimento al controllo del tasto di scelta](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Informazioni sui controlli tasto di scelta](hot-key-controls.md)
</dt> <dt>

[Uso di controlli tasto di scelta](using-hot-key-controls.md)
</dt> </dl>

 

 