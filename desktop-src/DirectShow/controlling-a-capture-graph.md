---
description: Controllo di un grafico di acquisizione
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Controllo di un grafico di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6366645f14822a770b828e59b2201e378a0e1e8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522033"
---
# <a name="controlling-a-capture-graph"></a>Controllo di un grafico di acquisizione

L'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) del gestore del grafo del filtro dispone di metodi per l'esecuzione, l'arresto e la sospensione dell'intero grafico. Se il grafo del filtro contiene flussi di acquisizione e di anteprima, è possibile, tuttavia, controllare i due flussi in modo indipendente. Ad esempio, potrebbe essere necessario visualizzare l'anteprima del video senza acquisirlo. Questa operazione può essere eseguita tramite il metodo [**ICaptureGraphBuilder2:: ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) .

> [!Note]  
> Questo metodo non funziona durante l'acquisizione in un file di formato Advanced Systems (ASF).

 

Controllo del flusso di acquisizione

Il codice seguente imposta il flusso di acquisizione video da eseguire per quattro secondi, a partire da un secondo dopo l'esecuzione del grafo:


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



Il primo parametro specifica il flusso da controllare come GUID di categoria pin. Il secondo parametro fornisce il tipo di supporto. Il terzo parametro è un puntatore al filtro di acquisizione. Per controllare tutti i flussi di acquisizione nel grafico, impostare il secondo e il terzo parametro su **null**.

I due parametri successivi definiscono i tempi di avvio e arresto del flusso, rispetto all'ora di inizio dell'esecuzione del grafico. Chiamare [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) per eseguire il grafo. Fino a quando non si esegue il grafo, il metodo **ControlStream** non ha alcun effetto. Se il grafo è già in esecuzione, le impostazioni diventano effettive immediatamente.

Gli ultimi due parametri vengono usati per ricevere notifiche degli eventi quando il flusso viene avviato e interrotto. Per ogni flusso controllato usando questo metodo, il grafico dei filtri invia una coppia di eventi: il [**controllo del flusso EC viene \_ \_ \_ avviato**](ec-stream-control-started.md) all'avvio del flusso e il controllo del flusso di EC si interrompe quando il flusso viene [**\_ \_ \_ arrestato**](ec-stream-control-stopped.md) . I valori di **wStartCookie** e **wStopCookie** vengono usati come secondo parametro dell'evento. Quindi, *lParam2* nell'evento di avvio è uguale a **wStartCookie** e *lParam2* nell'evento Stop è uguale a **wStopCookie**. Il codice seguente mostra come ottenere questi eventi:


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



Il metodo **ControlStream** definisce alcuni valori speciali per le ore di inizio e di fine.



|             |                                        |                                    |
|-------------|----------------------------------------|------------------------------------|
|             | Inizia                                  | Stop                               |
| MAXLONGLONG | Non avviare mai questo flusso.               | Non arrestare finché il grafico non viene arrestato. |
| **NULL**    | Inizia immediatamente quando il grafico viene eseguito. | Arresta immediatamente.                  |



 

Ad esempio, il codice seguente arresta immediatamente il flusso di acquisizione:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



Sebbene sia possibile arrestare il flusso di acquisizione e riavviarlo in un secondo momento, verrà creato un gap nei timestamp. Durante la riproduzione, il video verrà bloccato durante il gap (a seconda del formato di file).

Controllo del flusso di anteprima

Per controllare il pin di anteprima, chiamare **ControlStream** ma impostare il primo parametro su \_ Aggiungi \_ anteprima categoria. Questa operazione funziona esattamente come per l' \_ acquisizione di categorie pin \_ , ma non è possibile usare i tempi di riferimento per specificare l'avvio e l'arresto, perché i frame di anteprima non hanno timestamp. Pertanto, è necessario utilizzare **null** o MAXLONGLONG. Usare **null** per avviare il flusso di anteprima:


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



Non è importante se il flusso di anteprima deriva da un pin di anteprima nel filtro di acquisizione o dal filtro Smart Tee. Il metodo **ControlStream** funziona in qualsiasi modo.

Per i pin della porta video, tuttavia, il metodo avrà esito negativo. In tal caso, un altro approccio consiste nel nascondere la finestra video. Eseguire una query sul grafo per **IVideoWindow** e usare il metodo [**IVideoWindow::p UT \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) per mostrare o nascondere la finestra.


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



Inoltre, se si chiama [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con il valore OAFALSE prima di eseguire il grafo, il filtro renderer video nasconde la finestra fino a quando non viene specificato diversamente. Per impostazione predefinita, il renderer video mostra la finestra quando si esegue il grafo.

Osservazioni sul controllo Stream

Il comportamento predefinito per un PIN consiste nel recapitare gli esempi durante l'esecuzione del grafo. Si supponga, ad esempio, di chiamare **ControlStream** con l' \_ acquisizione della categoria pin \_ , ma non con l' \_ anteprima della categoria pin \_ . Quando si esegue il grafo, il flusso di anteprima viene eseguito immediatamente, mentre il flusso di acquisizione viene eseguito in qualsiasi momento specificato in **ControlStream**.

Se si acquisisce più di un flusso e lo si invia a un filtro Mux, ad esempio se si acquisisce audio e video in un file AVI, è necessario controllare entrambi i flussi in tandem. In caso contrario, il filtro Mux potrebbe bloccarsi in attesa di un flusso, in quanto tenta di eseguire l'interleave dei due flussi. Impostare le stesse ore di inizio e di fine su tutti i flussi di acquisizione prima di eseguire il grafo:


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



Internamente, il metodo **ControlStream** usa l'interfaccia [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , esposta nei pin del filtro di acquisizione, il filtro di Smart Tee (se presente) e possibilmente il filtro MUX. È possibile utilizzare direttamente questa interfaccia, anziché chiamare **ControlStream**, anche se non esiste un particolare vantaggio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



