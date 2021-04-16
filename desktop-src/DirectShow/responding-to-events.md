---
description: Questo articolo descrive come rispondere agli eventi che si verificano in un grafico di filtro.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Risposta agli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521401"
---
# <a name="responding-to-events"></a>Risposta agli eventi

Questo articolo descrive come rispondere agli eventi che si verificano in un grafico di filtro.

## <a name="how-event-notification-works"></a>Funzionamento della notifica degli eventi

Durante l'esecuzione di un'applicazione DirectShow, è possibile che si verifichino eventi nel grafico dei filtri. Ad esempio, un filtro potrebbe rilevare un errore di streaming. I filtri inviano avvisi al gestore del grafico dei filtri inviando eventi, che sono costituiti da un codice evento e due parametri di evento. Il codice evento indica il tipo di evento e i parametri dell'evento forniscono informazioni aggiuntive. Il significato dei parametri dipende dal codice evento. Per un elenco completo dei codici evento, vedere [codici di notifica degli eventi](event-notification-codes.md).

Alcuni eventi vengono gestiti automaticamente da Filter Graph Manager, senza che l'applicazione venga inviata una notifica. Altri eventi vengono inseriti in una coda per l'applicazione. A seconda dell'applicazione, è possibile che sia necessario gestire vari eventi. Questo articolo è incentrato su tre eventi molto comuni:

-   L'evento [**EC \_ complete**](ec-complete.md) indica che la riproduzione è stata completata normalmente.
-   L'evento [**EC \_ USERABORT**](ec-userabort.md) indica che l'utente ha interrotto la riproduzione. I renderer video inviano questo evento se l'utente chiude la finestra del video.
-   L'evento [**EC \_ ERRORABORT**](ec-errorabort.md) indica che un errore ha causato l'interruzione della riproduzione.

## <a name="using-event-notification"></a>Uso della notifica degli eventi

Un'applicazione può indicare a Filter Graph Manager di inviare un messaggio di Windows a una finestra specificata ogni volta che si verifica un nuovo evento. Ciò consente all'applicazione di rispondere all'interno del ciclo di messaggi della finestra. In primo luogo, definire il messaggio che verrà inviato alla finestra dell'applicazione. Le applicazioni possono usare i numeri dei messaggi nell'intervallo dall' \_ app WM tramite 0xBFFF come messaggi privati:


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



Successivamente, eseguire una query su Filter Graph Manager per l'interfaccia [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) e chiamare il metodo [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) :


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Questo metodo definisce la finestra specificata (g \_ HWND) come destinatario del messaggio. Chiamare il metodo dopo aver creato il grafico del filtro, ma prima di eseguire il grafo.

WM \_ GRAPHNOTIFY è un normale messaggio di Windows. Ogni volta che il gestore del grafico dei filtri inserisce un nuovo evento nella coda degli eventi, invia un \_ messaggio GRAPHNOTIFY WM alla finestra dell'applicazione designata. Il parametro *lParam* del messaggio è uguale al terzo parametro in [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Questo parametro consente di inviare i dati dell'istanza con il messaggio. Il parametro *wParam* del messaggio della finestra è sempre zero.

Nella funzione **WindowProc** dell'applicazione aggiungere un'istruzione case per il \_ messaggio WM GRAPHNOTIFY:


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



Nella funzione del gestore eventi chiamare il metodo [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) per recuperare gli eventi dalla coda:


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



Il metodo [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) Recupera il codice evento e i due parametri dell'evento. Il quarto parametro **GetEvent** specifica l'intervallo di tempo di attesa di un evento, in millisecondi. Poiché l'applicazione chiama questo metodo in risposta a un \_ messaggio WM GRAPHNOTIFY, l'evento è già in coda. Pertanto, il valore di timeout viene impostato su zero.

La notifica degli eventi e il ciclo di messaggi sono entrambi asincroni, quindi la coda potrebbe avere più di un evento nel momento in cui l'applicazione risponde al messaggio. Inoltre, il gestore del grafo del filtro può rimuovere determinati eventi dalla coda, se diventano non validi. Pertanto, è necessario chiamare [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) fino a quando non viene restituito un codice di errore, che indica che la coda è vuota.

In questo esempio, l'applicazione risponde a [**EC \_ complete**](ec-complete.md), [**EC \_ USERABORT**](ec-userabort.md)e [**EC \_ ERRORABORT**](ec-errorabort.md) richiamando la funzione di pulizia definita dall'applicazione, che causa la chiusura normale dell'applicazione. Nell'esempio vengono ignorati i due parametri dell'evento. Dopo aver recuperato un evento, chiamare [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) in tutte le risorse gratuite associate ai parametri dell'evento.

Si noti che un evento [**EC \_ complete**](ec-complete.md) non determina l'arresto del grafico del filtro. L'applicazione può arrestare o sospendere il grafo. Se si arresta il grafo, i filtri rilasciano tutte le risorse che contengono. Se si sospende il grafo, i filtri continuano a mantenere le risorse. Inoltre, quando un renderer video viene sospeso, viene visualizzata un'immagine statica del frame più recente.

Prima di rilasciare il puntatore [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , annullare la notifica degli eventi chiamando [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) con un handle di finestra **null** :


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



Nel gestore di \_ messaggi WM GRAPHNOTIFY controllare il puntatore [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) prima di chiamare [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):


```C++
if (g_pEvent == NULL) return;
```



In questo modo si evita un possibile errore che può verificarsi se l'applicazione riceve la notifica degli eventi dopo aver rilasciato il puntatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività DirectShow di base](basic-directshow-tasks.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



