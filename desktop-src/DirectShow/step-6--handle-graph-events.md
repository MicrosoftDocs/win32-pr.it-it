---
description: Questo argomento è il passaggio 6 della riproduzione audio/video dell'esercitazione in DirectShow.
ms.assetid: febfe7fa-e5f1-4b37-942a-ed9f8c7c60c1
title: 'Passaggio 6: gestire gli eventi del grafo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3660e270a542a060ed5e5eee79d5c78c107fea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316317"
---
# <a name="step-6-handle-graph-events"></a>Passaggio 6: gestire gli eventi del grafo

Questo argomento è il passaggio 6 della [riproduzione audio/video dell'esercitazione in DirectShow](audio-video-playback-in-directshow.md). Il codice completo è illustrato nell'esempio relativo alla [riproduzione DirectShow](directshow-playback-example.md).

Quando l'applicazione crea una nuova istanza di Filter Graph Manager, l'applicazione chiama [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Questo metodo registra la finestra dell'applicazione per la ricezione di eventi dal grafico dei filtri.


```C++
    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }
```



Il valore `WM_GRAPH_EVENT` è un messaggio di finestra privata. Ogni volta che l'applicazione riceve questo messaggio, chiama il `DShowPlayer::HandleGraphEvent` metodo.


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



Il metodo `DShowPlayer::HandleGraphEvent` esegue le operazioni seguenti:

1.  Chiama [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in un ciclo per ottenere tutti gli eventi in coda.
2.  Richiama una funzione di callback (*pfnOnGraphEvent*).
3.  Chiama [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) per liberare i dati associati a ogni evento.


```C++
// Respond to a graph event.
//
// The owning window should call this method when it receives the window
// message that the application specified when it called SetEventWindow.
//
// Caution: Do not tear down the graph from inside the callback.

HRESULT DShowPlayer::HandleGraphEvent(GraphEventFN pfnOnGraphEvent)
{
    if (!m_pEvent)
    {
        return E_UNEXPECTED;
    }

    long evCode = 0;
    LONG_PTR param1 = 0, param2 = 0;

    HRESULT hr = S_OK;

    // Get the events from the queue.
    while (SUCCEEDED(m_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        // Invoke the callback.
        pfnOnGraphEvent(m_hwnd, evCode, param1, param2);

        // Free the event data.
        hr = m_pEvent->FreeEventParams(evCode, param1, param2);
        if (FAILED(hr))
        {
            break;
        }
    }
    return hr;
}
```



Nel codice seguente viene illustrata la funzione di callback passata a `DShowPlayer::HandleGraphEvent` . La funzione gestisce il numero minimo di eventi del grafo ([**EC \_ completa**](ec-complete.md), [**EC \_ ERRORABORT**](ec-errorabort.md)e [**EC \_ USERABORT**](ec-userabort.md)). è possibile espandere la funzione per gestire eventi aggiuntivi.


```C++
void CALLBACK OnGraphEvent(HWND hwnd, long evCode, LONG_PTR param1, LONG_PTR param2)
{
    switch (evCode)
    {
    case EC_COMPLETE:
    case EC_USERABORT:
        g_pPlayer->Stop();
        break;

    case EC_ERRORABORT:
        NotifyError(hwnd, L"Playback error.");
        g_pPlayer->Stop();
        break;
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione audio/video in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Esempio di riproduzione DirectShow](directshow-playback-example.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Risposta agli eventi](responding-to-events.md)
</dt> </dl>

 

 



