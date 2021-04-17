---
title: Metodo OnPaint
description: Metodo OnPaint
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Plug-in di Windows Media Player, metodo OnPaint
- plug-in, metodo OnPaint
- plug-in dell'interfaccia utente, metodo OnPaint
- Plug-in dell'interfaccia utente, metodo OnPaint
- Metodo OnPaint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22641c34bb2edab30c1bf97011e893bc1d9d44a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471627"
---
# <a name="the-onpaint-method"></a>Metodo OnPaint

Il metodo OnPaint viene chiamato ogni volta che la finestra del plug-in deve essere disegnata automaticamente. Questo errore si verifica quando la finestra del plug-in riceve un \_ messaggio di disegno WM, mappato al metodo OnPaint nella mappa messaggi descritta in precedenza. La procedura guidata fornisce un'implementazione di questo metodo che dipinge il nero di sfondo e inserisce il nome del plug-in nella finestra del plug-in. L'unica modifica necessaria per il plug-in di ricerca dell'interfaccia utente è la rimozione del codice che Visualizza il testo.

Il codice seguente viene usato per implementare questo metodo:


```C++
LRESULT OnPaint(UINT nMsg, WPARAM wParam, 
                         LPARAM lParam, BOOL& bHandled)
{
    PAINTSTRUCT ps;

    HDC hDC = BeginPaint(&ps);

    RECT rc;
    GetClientRect(&rc);

    HBRUSH hNewBrush = ::CreateSolidBrush( RGB(0, 0, 0) );

    if (hNewBrush)
    {
        ::FillRect(hDC, &rc, hNewBrush );
        ::DeleteObject( hNewBrush );
    }

    EndPaint(&ps);
    return 0;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




