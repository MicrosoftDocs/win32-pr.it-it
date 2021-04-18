---
description: Scrittura del file
ms.assetid: d3dbe6ab-810c-4798-a769-c3f00c52a93a
title: Scrittura del file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda23b144956ab5afca9dd733b29a6f9d639cddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308929"
---
# <a name="writing-the-file"></a><span data-ttu-id="3fbb2-103">Scrittura del file</span><span class="sxs-lookup"><span data-stu-id="3fbb2-103">Writing the File</span></span>

<span data-ttu-id="3fbb2-104">Per scrivere il file, è sufficiente eseguire il grafico del filtro chiamando il metodo [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) .</span><span class="sxs-lookup"><span data-stu-id="3fbb2-104">To write the file, simply run the filter graph by calling the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method.</span></span> <span data-ttu-id="3fbb2-105">Attendere il completamento della riproduzione e arrestare in modo esplicito il grafo chiamando [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); in caso contrario, il file non viene scritto correttamente.</span><span class="sxs-lookup"><span data-stu-id="3fbb2-105">Wait for playback to complete and explicitly stop the graph by calling [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); otherwise the file is not written correctly.</span></span>

<span data-ttu-id="3fbb2-106">Per visualizzare lo stato di avanzamento dell'operazione di scrittura di file, eseguire una query sul filtro MUX per l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="3fbb2-106">To display the progress of the file-writing operation, query the Mux filter for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="3fbb2-107">Chiamare il metodo [**IMediaSeeking:: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) per recuperare la durata del file.</span><span class="sxs-lookup"><span data-stu-id="3fbb2-107">Call the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method to retrieve the duration of the file.</span></span> <span data-ttu-id="3fbb2-108">Periodicamente durante l'esecuzione del grafo, chiamare il metodo [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) per recuperare la posizione corrente del grafico nel flusso.</span><span class="sxs-lookup"><span data-stu-id="3fbb2-108">Periodically while the graph is running, call the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method to retrieve the graph's current position in the stream.</span></span> <span data-ttu-id="3fbb2-109">La posizione corrente divisa per durata consente di completare la percentuale.</span><span class="sxs-lookup"><span data-stu-id="3fbb2-109">Current position divided by duration gives the percentage complete.</span></span>

> [!Note]  
> <span data-ttu-id="3fbb2-110">Un'applicazione in genere esegue una query su Filter Graph Manager per **IMediaSeeking**, ma la scrittura di file è un'eccezione a questa regola.</span><span class="sxs-lookup"><span data-stu-id="3fbb2-110">An application usually queries the Filter Graph Manager for **IMediaSeeking**, but file writing is an exception to this rule.</span></span> <span data-ttu-id="3fbb2-111">Filter Graph Manager calcola la posizione corrente dalla posizione iniziale e la durata dell'esecuzione del grafo, che risulta accurata per la riproduzione di file ma non per la scrittura di file.</span><span class="sxs-lookup"><span data-stu-id="3fbb2-111">The Filter Graph Manager calculates the current position from the starting position and how long the graph has been running, which is accurate for file playback but not for file writing.</span></span> <span data-ttu-id="3fbb2-112">Pertanto, per ottenere un risultato accurato, è necessario recuperare la posizione dal filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="3fbb2-112">Therefore, to get an accurate result, you should retrieve the position from the MUX filter.</span></span>

 

<span data-ttu-id="3fbb2-113">Il codice seguente ottiene la durata del file, avvia un timer per aggiornare l'interfaccia utente dell'applicazione ed esegue il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="3fbb2-113">The following code gets the duration of the file, starts a timer to update the application UI, and runs the filter graph.</span></span> <span data-ttu-id="3fbb2-114">Per maggiore chiarezza, viene omesso il controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="3fbb2-114">(Error checking is omitted for clarity.)</span></span>


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



<span data-ttu-id="3fbb2-115">Quando l'applicazione riceve un evento timer, può aggiornare l'interfaccia utente con la posizione corrente:</span><span class="sxs-lookup"><span data-stu-id="3fbb2-115">When the application receives a timer event, it can update the UI with the current position:</span></span>


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



<span data-ttu-id="3fbb2-116">Quando l'applicazione riceve un evento di completamento DirectShow, deve arrestare il grafo, come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="3fbb2-116">When the application receives a DirectShow completion event, it should stop the graph, as shown in the following code:</span></span>


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



 

 



