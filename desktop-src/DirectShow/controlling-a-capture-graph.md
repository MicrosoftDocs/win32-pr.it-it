---
description: Controllo di un'Graph
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Controllo di un'Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d678e00452fbf90591fbc187039ddbbc37cc4fde446e2e285c77fcaab415e815
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652141"
---
# <a name="controlling-a-capture-graph"></a>Controllo di un'Graph

L'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) di Filter Graph Manager include metodi per l'esecuzione, l'arresto e la sospensione dell'intero grafico. Se tuttavia il grafico dei filtri include flussi di acquisizione e anteprima, è probabile che si voglia controllare i due flussi in modo indipendente. Ad esempio, è possibile visualizzare in anteprima il video senza acquisirlo. È possibile eseguire questa operazione tramite il [**metodo ICaptureGraphBuilder2::ControlStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream)

> [!Note]  
> Questo metodo non funziona durante l'acquisizione in un file ASF (Advanced Systems Format).

 

Controllo del flusso di acquisizione

Il codice seguente imposta l'esecuzione del flusso di acquisizione video per quattro secondi, a partire da un secondo dopo l'esecuzione del grafico:


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



Il primo parametro specifica il flusso da controllare, come GUID della categoria pin. Il secondo parametro fornisce il tipo di supporto. Il terzo parametro è un puntatore al filtro di acquisizione. Per controllare tutti i flussi di acquisizione nel grafico, impostare il secondo e il terzo parametro su **NULL.**

I due parametri successivi definiscono gli orari di avvio e arresto del flusso, rispetto all'ora di inizio dell'esecuzione del grafico. Chiamare [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) per eseguire il grafo. Fino a quando non si esegue il grafico, **il metodo ControlStream** non ha alcun effetto. Se il grafico è già in esecuzione, le impostazioni vengono applicate immediatamente.

Gli ultimi due parametri vengono usati per ottenere notifiche degli eventi all'avvio e all'arresto del flusso. Per ogni flusso che si controlla usando questo metodo, il grafo dei filtri invia una coppia di eventi: [**EC \_ STREAM CONTROL \_ \_ STARTED**](ec-stream-control-started.md) all'avvio del flusso e [**EC STREAM CONTROL \_ \_ \_ STOPPED**](ec-stream-control-stopped.md) all'arresto del flusso. I valori **di wStartCookie** e **wStopCookie** vengono usati come secondo parametro dell'evento. Pertanto, *lParam2* nell'evento di avvio è uguale a **wStartCookie** e *lParam2* nell'evento di arresto è uguale **a wStopCookie**. Il codice seguente illustra come ottenere questi eventi:


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



Il **metodo ControlStream** definisce alcuni valori speciali per l'ora di inizio e di arresto.



| Valore | Inizia                                  | Stop                               |
|-------------|----------------------------------------|---------|
| MAXLONGLONG | Non avviare mai questo flusso.               | Non arrestarsi fino a quando il grafo non si arresta. |
| **NULL**    | Iniziare immediatamente quando viene eseguito il grafo. | Arrestarsi immediatamente.                  |



 

Ad esempio, il codice seguente arresta immediatamente il flusso di acquisizione:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



Anche se è possibile arrestare il flusso di acquisizione e riavviarlo in un secondo momento, verrà creato un gap nei timestamp. Durante la riproduzione, il video sembra bloccarsi durante il gap (a seconda del formato di file).

Controllo del flusso di anteprima

Per controllare il pin di anteprima, chiamare **ControlStream** ma impostare il primo parametro su PIN \_ CATEGORY \_ PREVIEW. Funziona esattamente come per PIN CATEGORY CAPTURE, ad eccezione del fatto che non è possibile usare orari di riferimento per specificare l'inizio e l'arresto, perché i fotogrammi di anteprima non hanno \_ \_ timestamp. Pertanto, è necessario usare **NULL** o MAXLONGLONG. Usare **NULL per** avviare il flusso di anteprima:


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



Usare MAXLONGLONG per arrestare il flusso di anteprima:


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



Non importa se il flusso di anteprima proviene da un segnaposto di anteprima nel filtro di acquisizione o dal filtro Smart Tee. Il **metodo ControlStream** funziona in entrambi i modi.

Per i pin di porta video, tuttavia, il metodo avrà esito negativo. In tal caso, un altro approccio consiste nel nascondere la finestra video. Eseguire una query sul **grafo per IVideoWindow** e usare il metodo [**IVideoWindow::p ut \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) per visualizzare o nascondere la finestra.


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



Inoltre, se si chiama [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con il valore OAFALSE prima di eseguire il grafico, il filtro Renderer video nasconde la finestra fino a quando non si specifica diversamente. Per impostazione predefinita, il renderer video mostra la finestra quando si esegue il grafico.

Osservazioni sul controllo di flusso

Il comportamento predefinito per un segnaposto è fornire esempi quando viene eseguito il grafo. Si supponga, ad esempio, di chiamare **ControlStream con PIN** \_ CATEGORY CAPTURE ma non con PIN CATEGORY \_ \_ \_ PREVIEW. Quando si esegue il grafico, il flusso di anteprima verrà eseguito immediatamente, mentre il flusso di acquisizione verrà eseguito in qualsiasi momento specificato in **ControlStream**.

Se si acquisisce più di un flusso e li si invia a un filtro mux, ad esempio se si acquisisce audio e video in un file AVI, è necessario controllare entrambi i flussi in tandem. In caso contrario, il filtro mux potrebbe bloccarsi in attesa di un flusso, mentre tenta di interfoliare i due flussi. Impostare gli stessi orari di avvio e arresto in tutti i flussi di acquisizione prima di eseguire il grafico:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



Internamente, il metodo **ControlStream** usa l'interfaccia [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) esposta sui pin del filtro di acquisizione, il filtro Smart Tee (se presente) ed eventualmente il filtro mux. È possibile usare questa interfaccia direttamente, invece di chiamare **ControlStream**, anche se non esiste alcun vantaggio particolare a tale scopo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



