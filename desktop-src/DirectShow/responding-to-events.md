---
description: Questo articolo descrive come rispondere agli eventi che si verificano in un grafico di filtro.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Risposta agli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb0325af2e216a3679d3e15a293aa6bfe1c100f2271d089e982b295df791130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050561"
---
# <a name="responding-to-events"></a>Risposta agli eventi

Questo articolo descrive come rispondere agli eventi che si verificano in un grafico di filtro.

## <a name="how-event-notification-works"></a>Funzionamento della notifica degli eventi

Mentre un'DirectShow è in esecuzione, gli eventi possono verificarsi all'interno del grafico dei filtri. Ad esempio, un filtro potrebbe riscontrare un errore di streaming. I filtri generano un avviso Graph Gestione eventi inviando eventi costituiti da un codice evento e da due parametri dell'evento. Il codice evento indica il tipo di evento e i parametri dell'evento forniscono informazioni aggiuntive. Il significato dei parametri dipende dal codice evento. Per un elenco completo dei codici evento, vedere [Codici di notifica degli eventi.](event-notification-codes.md)

Alcuni eventi vengono gestiti automaticamente da Filter Graph Manager, senza che l'applicazione venga notificata. Altri eventi vengono inseriti in una coda per l'applicazione. A seconda dell'applicazione, potrebbe essere necessario gestire vari eventi. Questo articolo è incentrato su tre eventi molto comuni:

-   [**\_ L'evento EC COMPLETE**](ec-complete.md) indica che la riproduzione è stata completata normalmente.
-   [**\_ L'evento EC USERABORT**](ec-userabort.md) indica che l'utente ha interrotto la riproduzione. I renderer video inviano questo evento se l'utente chiude la finestra video.
-   [**\_ L'evento EC ERRORABORT**](ec-errorabort.md) indica che un errore ha causato l'interruzione della riproduzione.

## <a name="using-event-notification"></a>Uso della notifica degli eventi

Un'applicazione può indicare a Filter Graph Manager di inviare un messaggio Windows a una finestra designata ogni volta che si verifica un nuovo evento. In questo modo l'applicazione può rispondere all'interno del ciclo di messaggi della finestra. Definire prima di tutto il messaggio che verrà inviato alla finestra dell'applicazione. Le applicazioni possono usare i numeri di messaggio nell'intervallo da WM \_ APP 0xBFFF messaggi privati:


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



Eseguire quindi una query su Filter Graph Manager per [**l'interfaccia IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) e chiamare il [**metodo IMediaEventEx::SetNotifyWindow:**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Questo metodo designa la finestra specificata (g \_ hwnd) come destinatario del messaggio. Chiamare il metodo dopo aver creato il grafico del filtro, ma prima di eseguire il grafico.

WM \_ GRAPHNOTIFY è un messaggio Windows normale. Ogni volta che Filter Graph Manager inserisce un nuovo evento nella coda degli eventi, invia un messaggio WM \_ GRAPHNOTIFY alla finestra dell'applicazione designata. Il parametro *lParam del* messaggio è uguale al terzo parametro in [**SetNotifyWindow.**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) Questo parametro consente di inviare i dati dell'istanza con il messaggio. Il parametro *wParam del messaggio della* finestra è sempre zero.

Nella funzione **WindowProc** dell'applicazione aggiungere un'istruzione case per il messaggio \_ WM GRAPHNOTIFY:


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



Nella funzione del gestore eventi chiamare il [**metodo IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) per recuperare gli eventi dalla coda:


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



Il [**metodo GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) recupera il codice evento e i due parametri dell'evento. Il quarto **parametro GetEvent** specifica il tempo di attesa di un evento, espresso in millisecondi. Poiché l'applicazione chiama questo metodo in risposta a un messaggio \_ GRAPHNOTIFY di WM, l'evento è già in coda. Il valore di timeout viene quindi impostato su zero.

La notifica degli eventi e il ciclo di messaggi sono entrambi asincroni, quindi la coda potrebbe contenere più di un evento nel momento in cui l'applicazione risponde al messaggio. Inoltre, l'Graph filtro può rimuovere determinati eventi dalla coda, se diventano non validi. Pertanto, è necessario chiamare [**GetEvent finché**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) non restituisce un codice di errore, che indica che la coda è vuota.

In questo esempio l'applicazione risponde a [**EC \_ COMPLETE, EC**](ec-complete.md) [**\_ USERABORT**](ec-userabort.md)e [**EC \_ ERRORABORT**](ec-errorabort.md) richiamando la funzione CleanUp definita dall'applicazione, che causa la chiusura dell'applicazione normalmente. Nell'esempio vengono ignorati i due parametri dell'evento . Dopo aver recuperato un evento, chiamare [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) per tutte le risorse gratuite associate ai parametri dell'evento.

Si noti che un [**evento EC \_ COMPLETE**](ec-complete.md) non causa l'arresto del grafico del filtro. L'applicazione può arrestare o sospendere il grafico. Se si arresta il grafico, i filtri rilasciano tutte le risorse in essi presenti. Se si sospende il grafico, i filtri continuano a contenere le risorse. Inoltre, quando un renderer video viene sospeso, visualizza un'immagine statica del fotogramma più recente.

Prima di rilasciare il [**puntatore IMediaEventEx,**](/windows/desktop/api/Control/nn-control-imediaeventex) annullare la notifica degli eventi chiamando [**SetNotifyWindow con**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) un handle di finestra **NULL:**


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



Nel gestore di messaggi WM \_ GRAPHNOTIFY controllare il puntatore [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) prima di chiamare [**GetEvent:**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)


```C++
if (g_pEvent == NULL) return;
```



In questo modo si evita un possibile errore che può verificarsi se l'applicazione riceve la notifica degli eventi dopo il rilascio del puntatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività DirectShow base](basic-directshow-tasks.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



