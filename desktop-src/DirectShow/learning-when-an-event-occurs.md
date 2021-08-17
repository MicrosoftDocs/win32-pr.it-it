---
description: Learning Quando si verifica un evento
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Learning Quando si verifica un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58696055bdf1e3cbf3cf36c4db4ae2258bda334956fcaa14f33eda96db249773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397217"
---
# <a name="learning-when-an-event-occurs"></a>Learning Quando si verifica un evento

Per elaborare DirectShow eventi, un'applicazione deve individuare quando gli eventi sono in attesa nella coda. Gestione filtri Graph offre due modi per eseguire questa operazione:

-   **Notifica finestra:** Filter Graph Manager invia un messaggio di Windows definito dall'utente a una finestra dell'applicazione ogni volta che è presente un nuovo evento.
-   **Segnalazione di eventi:** Filter Graph Manager segnala un evento Windows se sono presenti eventi DirectShow nella coda e reimposta l'evento se la coda è vuota.

Un'applicazione può usare entrambe le tecniche. La notifica della finestra è in genere più semplice.

**Notifica finestra**

Per configurare la notifica della finestra, chiamare il [**metodo IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) e specificare un messaggio privato. Le applicazioni possono usare i numeri di messaggio nell'intervallo da WM \_ APP 0xBFFF messaggi privati. Ogni volta che il Graph filtro inserisce una nuova notifica degli eventi nella coda, inserisce questo messaggio nella finestra designata. L'applicazione risponde al messaggio dall'interno del ciclo di messaggi della finestra.

Nell'esempio di codice seguente viene illustrato come impostare la finestra di notifica.


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Il messaggio è un normale Windows e viene pubblicato separatamente dalla coda di notifica DirectShow eventi. Il vantaggio di questo approccio è che la maggior parte delle applicazioni implementa già un ciclo di messaggi. Pertanto, è possibile incorporare DirectShow gestione degli eventi senza molto lavoro aggiuntivo.

Nell'esempio di codice seguente viene illustrato come rispondere al messaggio di notifica. Per un esempio completo, vedere [Risposta agli eventi](responding-to-events.md).


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



Poiché la notifica degli eventi e il ciclo di messaggi sono entrambi asincroni, la coda potrebbe contenere più eventi nel momento in cui l'applicazione risponde al messaggio. Inoltre, gli eventi possono talvolta essere cancellati dalla coda se diventano non validi. Pertanto, nel codice di gestione degli eventi chiamare [**IAMMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) finché non restituisce un codice di errore, a indicare che la coda è vuota.

Prima di rilasciare il [**puntatore IMediaEventEx,**](/windows/desktop/api/Control/nn-control-imediaeventex) annullare la notifica dell'evento chiamando [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) con un **puntatore NULL.** Nel codice di elaborazione degli eventi controllare se il puntatore **IMediaEventEx** è valido prima di [**chiamare GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent). Questi passaggi impediscono un possibile errore, in cui l'applicazione riceve la notifica degli eventi dopo il rilascio del puntatore **IMediaEventEx.**

**Segnalazione di eventi**

L'Graph Gestione filtri mantiene un evento di reimpostazione manuale che riflette lo stato della coda di eventi. Se la coda contiene notifiche di eventi in sospeso, gestione filtri Graph segnala l'evento di reimpostazione manuale. Se la coda è vuota, una chiamata al metodo [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) reimposta l'evento. Un'applicazione può usare questo evento per determinare lo stato della coda.

> [!Note]  
> La terminologia può generare confusione in questo caso. L'evento di reimpostazione manuale è il tipo di evento creato dalla Windows [**CreateEvent.**](/windows/win32/api/synchapi/nf-synchapi-createeventa) non ha nulla a che fare con gli eventi definiti da DirectShow.

 

Chiamare il [**metodo IMediaEvent::GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) per ottenere un handle per l'evento di reimpostazione manuale. Attendere che l'evento sia segnalato chiamando una funzione, ad esempio [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects). Dopo aver segnalato l'evento, chiamare [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) per ottenere l'DirectShow evento.

Il seguente esempio di codice illustra questo approccio. Ottiene l'handle dell'evento, quindi attende a intervalli di 100 millisecondi che l'evento venga segnalato. Se l'evento viene segnalato, chiama **GetEvent** e stampa il codice dell'evento e i parametri dell'evento nella finestra della console. Il ciclo termina quando si verifica [**l'evento EC \_ COMPLETE,**](ec-complete.md) a indicare che la riproduzione è stata completata.


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



Poiché il grafico dei filtri imposta o reimposta automaticamente l'evento quando appropriato, l'applicazione non deve eseguire questa operazione. Inoltre, quando si rilascia il grafico dei filtri, il grafo dei filtri chiude l'handle dell'evento, quindi non usare l'handle dell'evento dopo tale punto.

 

 
