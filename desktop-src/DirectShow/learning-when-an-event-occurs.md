---
description: Apprendimento quando si verifica un evento
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Apprendimento quando si verifica un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed537430fd66818687b142f059399292c923e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522066"
---
# <a name="learning-when-an-event-occurs"></a>Apprendimento quando si verifica un evento

Per elaborare gli eventi DirectShow, un'applicazione necessita di un modo per individuare quando gli eventi sono in attesa nella coda. Per eseguire questa operazione, il gestore del grafo del filtro offre due modi:

-   **Notifica finestra:** Filter Graph Manager invia un messaggio di Windows definito dall'utente a una finestra dell'applicazione ogni volta che viene eseguito un nuovo evento.
-   **Segnalazione evento:** Filter Graph Manager segnala un evento Windows se sono presenti eventi DirectShow nella coda e Reimposta l'evento se la coda è vuota.

Un'applicazione può utilizzare una delle due tecniche. La notifica della finestra è in genere più semplice.

**Notifica finestra**

Per impostare la notifica della finestra, chiamare il metodo [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) e specificare un messaggio privato. Le applicazioni possono usare i numeri dei messaggi nell'intervallo dall' \_ app WM tramite 0xBFFF come messaggi privati. Ogni volta che il gestore del grafico dei filtri inserisce una nuova notifica degli eventi nella coda, invia questo messaggio alla finestra designata. L'applicazione risponde al messaggio dall'interno del ciclo di messaggi della finestra.

Nell'esempio di codice riportato di seguito viene illustrato come impostare la finestra di notifica.


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Il messaggio è un normale messaggio di Windows e viene pubblicato separatamente dalla coda di notifiche degli eventi DirectShow. Il vantaggio di questo approccio è che la maggior parte delle applicazioni implementa già un ciclo di messaggi. Pertanto, è possibile incorporare la gestione degli eventi DirectShow senza molto lavoro aggiuntivo.

Nell'esempio di codice seguente viene illustrata la modalità di risposta al messaggio di notifica. Per un esempio completo, vedere [rispondere agli eventi](responding-to-events.md).


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



Poiché la notifica degli eventi e il ciclo di messaggi sono entrambi asincroni, la coda potrebbe contenere più di un evento nel momento in cui l'applicazione risponde al messaggio. Inoltre, gli eventi possono a volte essere cancellati dalla coda se diventano non validi. Nel codice di gestione degli eventi, quindi, chiamare [**IAMMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) fino a quando non viene restituito un codice di errore, a indicare che la coda è vuota.

Prima di rilasciare il puntatore [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , annullare la notifica degli eventi chiamando [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) con un puntatore **null** . Nel codice di elaborazione degli eventi controllare se il puntatore **IMediaEventEx** è valido prima di chiamare [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent). Questa procedura impedisce un possibile errore, in cui l'applicazione riceve la notifica degli eventi dopo aver rilasciato il puntatore **IMediaEventEx** .

**Segnalazione di eventi**

Filter Graph Manager mantiene un evento di reimpostazione manuale che riflette lo stato della coda degli eventi. Se la coda contiene notifiche di eventi in sospeso, il gestore del grafico del filtro segnala l'evento di reimpostazione manuale. Se la coda è vuota, una chiamata al metodo [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) Reimposta l'evento. Un'applicazione può utilizzare questo evento per determinare lo stato della coda.

> [!Note]  
> La terminologia può creare confusione. L'evento di reimpostazione manuale è il tipo di evento creato dalla funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) di Windows. non ha nulla a che fare con gli eventi definiti da DirectShow.

 

Chiamare il metodo [**IMediaEvent:: GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) per ottenere un handle per l'evento di reimpostazione manuale. Attendere che l'evento venga segnalato chiamando una funzione come [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects). Una volta segnalato l'evento, chiamare [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) per ottenere l'evento DirectShow.

Il seguente esempio di codice illustra questo approccio. Ottiene l'handle dell'evento, quindi attende in intervalli di 100 millisecondi che l'evento venga segnalato. Se l'evento viene segnalato, chiama **GetEvent** e stampa il codice evento e i parametri dell'evento nella finestra della console. Il ciclo termina quando si verifica l'evento di [**\_ completamento dell'EC**](ec-complete.md) , a indicare che la riproduzione è stata completata.


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



Poiché il grafico di filtro imposta o reimposta automaticamente l'evento quando appropriato, l'applicazione non deve eseguire questa operazione. Inoltre, quando si rilascia il grafico del filtro, il grafico di filtro chiude l'handle di evento, quindi non usare l'handle di evento dopo tale punto.

 

 
