---
description: Scrittura del file
ms.assetid: d3dbe6ab-810c-4798-a769-c3f00c52a93a
title: Scrittura del file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cabb5575f371c6525e58cc8ede7d05c2701acc31be325af46e3b00e6e2d8d20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051400"
---
# <a name="writing-the-file"></a>Scrittura del file

Per scrivere il file, è sufficiente eseguire il grafico dei filtri chiamando il [**metodo IMediaControl::Run.**](/windows/desktop/api/Control/nf-control-imediacontrol-run) Attendere il completamento della riproduzione e arrestare in modo esplicito il grafo chiamando [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); in caso contrario, il file non viene scritto correttamente.

Per visualizzare lo stato dell'operazione di scrittura di file, eseguire una query sul filtro Mux per [**l'interfaccia IMediaSeeking.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) Chiamare il [**metodo IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) per recuperare la durata del file. Periodicamente mentre il grafo è in esecuzione, chiamare il metodo [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) per recuperare la posizione corrente del grafo nel flusso. La posizione corrente divisa per durata indica la percentuale di completamento.

> [!Note]  
> Un'applicazione esegue in genere una query su Filter Graph Manager per **IMediaSeeking,** ma la scrittura di file è un'eccezione a questa regola. Filter Graph Manager calcola la posizione corrente dalla posizione iniziale e la durata dell'esecuzione del grafo, che è accurata per la riproduzione di file ma non per la scrittura di file. Pertanto, per ottenere un risultato accurato, è necessario recuperare la posizione dal filtro MUX.

 

Il codice seguente ottiene la durata del file, avvia un timer per aggiornare l'interfaccia utente dell'applicazione ed esegue il grafico dei filtri. Il controllo degli errori viene omesso per maggiore chiarezza.


```C++
IMediaSeeking *pSeek = NULL;
IMediaEventEx *pEvent = NULL;
IMediaControl *pControl = NULL;
REFERENCE_TIME rtTotal;

// Query for interfaces. Remember to release them later.
hr = pMux->QueryInterface(IID_IMediaSeeking, (void**)&pSeek);
hr = pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEvent);
hr = pGraph->QueryInterface(IID_IMediaControl, (void**)&pControl);

// Error checking is omitted for clarity.

// Set the DirectShow event notification window.
hr = pEvent->SetNotifyWindow((OAHWND)hwnd, WM_GRAPHNOTIFY, 0);

// Set the range of the progress bar to the file length (in seconds).
hr = pSeek->GetDuration(&rtTotal);
SendDlgItemMessage(hwnd, IDC_PROGRESS1, PBM_SETRANGE, 0, 
   MAKELPARAM(0, rtTotal / 10000000));
// Start the timer.
UINT_PTR res = SetTimer(hwnd, nIDEvent, 100, NULL);
// Run the graph.
pControl->Run();
```



Quando l'applicazione riceve un evento timer, può aggiornare l'interfaccia utente con la posizione corrente:


```C++
void OnTimer(HWND hDlg, IMediaSeeking *pSeek)
{
    REFERENCE_TIME rtNow;
    HRESULT hr = pSeek->GetCurrentPosition(&rtNow);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(hDlg, IDC_PROGRESS1, PBM_SETPOS, rtNow/10000000, 0);
    }
}
```



Quando l'applicazione riceve un DirectShow di completamento, deve arrestare il grafo, come illustrato nel codice seguente:


```C++
// Application window procedure
LRESULT CALLBACK WndProc(HWND hDlg, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch (msg)
    {
    /*  ...  */
    case WM_GRAPHNOTIFY:
        DoHandleEvent();
        break;
    /*  ...  */
    }
}

void DoHandleEvent()
{
    long evCode, param1, param2;
    bool bComplete = false;
    if (!pEvent) return;

    // Get all the events, and see we're done.
    while (SUCCEEDED(pEvent->GetEvent(&evCode, &param1, &param2, 0))
    {
        pEvent->FreeEventParams(evCode, param1, param2);
        switch(evCode)
        {
            case EC_USERABORT:
            case EC_ERRORABORT:
            case EC_COMPLETE:
                bComplete = true;
                break;
        }
    }
    if (bComplete)
    {
        pControl->Stop(); // Important! You must stop the graph!

        // Turn off event notification.
        pEvent->SetNotifyWindow(NULL, 0, 0);
        pEvent->Release();
        pEvent = NULL;
        // Reset the progress bar to zero and get rid of the timer.
        SendDlgItemMessage(IDC_PROGRESS1, PBM_SETPOS, 0, 0);
        KillTimer(hwnd, nIDEvent);
    }
}
```



 

 



