---
description: Recupero di eventi
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Recupero di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d23cf4f8060c15db564e718ba3a2fa4a660022
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401047"
---
# <a name="retrieving-events"></a>Recupero di eventi

Il gestore del grafo del filtro espone tre interfacce che supportano la notifica degli eventi.

-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contiene il metodo per i filtri per la pubblicazione di eventi.
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contiene metodi che consentono alle applicazioni di recuperare gli eventi.
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) eredita da ed estende l'interfaccia [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .

Filtra le notifiche degli eventi post chiamando il metodo [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) in gestione grafico dei filtri. Una notifica degli eventi è costituita da un codice evento, che definisce il tipo di evento e due parametri che forniscono informazioni aggiuntive. A seconda del codice evento, i parametri possono contenere puntatori, codici restituiti, tempi di riferimento o altre informazioni. Per un elenco completo dei parametri e dei codici evento, vedere [codici di notifica degli eventi](event-notification-codes.md).

Per recuperare un evento dalla coda, l'applicazione chiama il metodo [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in gestione grafico dei filtri. Questo metodo si blocca fino a quando non si verifica un evento da restituire o fino a quando non trascorre un intervallo di tempo specificato. Supponendo che sia presente un evento in coda, il metodo restituisce con il codice evento e i due parametri dell'evento. Dopo la chiamata a **GetEvent**, un'applicazione deve sempre chiamare il metodo [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) per rilasciare tutte le risorse associate ai parametri dell'evento. Un parametro, ad esempio, può essere un valore **BSTR** allocato dal grafico dei filtri.

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



Per eseguire l'override della gestione predefinita di Filter Graph Manager per un evento, chiamare il metodo [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con il codice evento come parametro. È possibile ripristinare la gestione predefinita chiamando il metodo [**IMediaEvent:: RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) . Se il grafico del filtro non esegue alcuna gestione predefinita per il codice evento specificato, la chiamata a questi metodi non ha alcun effetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



