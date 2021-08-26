---
title: Metodo OnPaint
description: Metodo OnPaint
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Windows Media Player plug-in, metodo OnPaint
- plug-in, metodo OnPaint
- plug-in dell'interfaccia utente, metodo OnPaint
- Plug-in dell'interfaccia utente, metodo OnPaint
- Metodo OnPaint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5e121cdaeac1c7589e58b1613a8d25bdff4f44f6db2375bcbdc34da20929e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001951"
---
# <a name="the-onpaint-method"></a>Metodo OnPaint

Il metodo OnPaint viene chiamato ogni volta che la finestra del plug-in deve disegnare se stessa. Ciò si verifica quando la finestra del plug-in riceve un messaggio WM PAINT, mappato al metodo OnPaint nella mappa messaggi \_ descritta in precedenza. La procedura guidata fornisce un'implementazione di questo metodo che dipinge lo sfondo nero e inserisce il nome del plug-in nella finestra del plug-in. L'unica modifica necessaria per il plug-in dell'interfaccia utente di ricerca è la rimozione del codice che visualizza il testo.

Per implementare questo metodo viene usato il codice seguente:


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

 

 




