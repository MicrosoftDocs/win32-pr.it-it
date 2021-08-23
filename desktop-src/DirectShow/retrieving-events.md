---
description: Recupero di eventi
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Recupero di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1132b2b0140c86c2be1e7916e8d1de28e231b2eca50596714aaa82346aaf83eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072725"
---
# <a name="retrieving-events"></a>Recupero di eventi

Filter Graph Manager espone tre interfacce che supportano la notifica degli eventi.

-   [**IMediaEventSink contiene**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) il metodo per i filtri per la pubblicazione di eventi.
-   [**IMediaEvent contiene**](/windows/desktop/api/Control/nn-control-imediaevent) metodi che consentono alle applicazioni di recuperare gli eventi.
-   [**IMediaEventEx eredita**](/windows/desktop/api/Control/nn-control-imediaeventex) da ed estende [**l'interfaccia IMediaEvent.**](/windows/desktop/api/Control/nn-control-imediaevent)

Filtra le notifiche post-evento chiamando [**il metodo IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) in Filter Graph Manager. Una notifica degli eventi è costituita da un codice evento, che definisce il tipo di evento, e da due parametri che forniscono informazioni aggiuntive. A seconda del codice evento, i parametri possono contenere puntatori, codici restituiti, tempi di riferimento o altre informazioni. Per un elenco completo dei codici evento e dei parametri, vedere [Codici di notifica degli eventi.](event-notification-codes.md)

Per recuperare un evento dalla coda, l'applicazione chiama il metodo [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in Filter Graph Manager. Questo metodo si blocca fino a quando non è presente un evento da restituire o fino a quando non è trascorso un tempo specificato. Supponendo che sia presente un evento in coda, il metodo restituisce con il codice dell'evento e i due parametri dell'evento. Dopo aver **chiamato GetEvent**, un'applicazione deve sempre chiamare il metodo [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) per rilasciare tutte le risorse associate ai parametri dell'evento. Ad esempio, un parametro potrebbe essere un **valore BSTR** allocato dal grafico dei filtri.

Nell'esempio di codice seguente viene illustrato come recuperare gli eventi dalla coda.


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



Per eseguire l'override della gestione predefinita di Filter Graph Manager per un evento, chiamare il metodo [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con il codice dell'evento come parametro. È possibile ripristinare la gestione predefinita chiamando il [**metodo IMediaEvent::RestoreDefaultHandling.**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) Se il grafico dei filtri non esegue alcuna gestione predefinita per il codice evento specificato, la chiamata di questi metodi non ha alcun effetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



