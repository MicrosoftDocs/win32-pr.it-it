---
description: Riconnessione dinamica
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Riconnessione dinamica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704178a28b91c6f78bea20b9c73c9a61f80be881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481852"
---
# <a name="dynamic-reconnection"></a>Riconnessione dinamica

Nella maggior parte dei filtri DirectShow non è possibile riconnettere i pin mentre il grafo esegue attivamente lo streaming dei dati. Prima di riconnettere i pin, l'applicazione deve arrestare il grafo. Tuttavia, alcuni filtri supportano la riconnessione del PIN durante l'esecuzione del grafo, un processo noto come riconnessione dinamica. Questa operazione può essere eseguita dall'applicazione o da un filtro nel grafico.

Si consideri, ad esempio, il grafico nella figura seguente.

![diagramma di compilazione dinamica del grafico](images/dyngraph.png)

Uno scenario per la riconnessione dinamica potrebbe essere quello di rimuovere il filtro 2 dal grafico, mentre il grafo è in esecuzione e sostituirlo con un altro filtro. Per il funzionamento di questo scenario, è necessario che siano soddisfatte le condizioni seguenti:

-   Il pin di input sul filtro 3 (pin D) deve supportare l'interfaccia [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) . Questa interfaccia consente la riconnessione del pin senza arrestare il filtro.
-   Il pin di output sul filtro 1 (pin A) deve essere in grado di bloccare il flusso dei dati multimediali mentre si verifica la riconnessione. Nessun dato può spostarsi tra il pin A e il pin D durante la riconnessione. In genere, ciò significa che il pin di output deve supportare l'interfaccia [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) . Tuttavia, se il filtro 1 è il filtro che avvia la riconnessione, potrebbe disporre di un meccanismo interno per bloccare il proprio flusso di dati.

La riconnessione dinamica prevede i passaggi seguenti:

1.  Blocca il flusso di dati dal pin A.
2.  Riconnettere il pin a al pin D, possibilmente tramite un nuovo filtro intermedio.
3.  Sbloccare il pin A in modo che i dati ricomincino a fluire nuovamente.

**Passaggio 1. Blocca il flusso di dati**

Per bloccare il flusso di dati, chiamare [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) sul pin a. Questo metodo può essere chiamato in modo asincrono o sincrono. Per chiamare il metodo in *modo asincrono*, creare un oggetto evento Win32 e passare l'handle di evento al metodo **Block** . Il metodo restituirà immediatamente. Attendere che l'evento venga segnalato, usando una funzione come **WaitForSingleObject**. Il pin segnala l'evento quando il flusso di dati è stato bloccato. Ad esempio:


```C++
// Create an event
HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (hEvent != NULL)
{
    // Block the data flow.
    hr = pFlowControl->Block(AM_PIN_FLOW_CONTROL_BLOCK, hEvent); 
    if (SUCCEEDED(hr))
    {
        // Wait for the pin to finish.
        DWORD dwRes = WaitForSingleObject(hEvent, dwMilliseconds);
    }
}
```



Per chiamare il metodo in modo *sincrono*, è sufficiente passare il valore **null** anziché l'handle dell'evento. A questo punto il metodo si bloccherà fino al completamento dell'operazione. Questo problema può verificarsi solo se il PIN è pronto per fornire un nuovo esempio. Se il filtro è sospeso, l'operazione può richiedere un periodo di tempo arbitrario. Non eseguire pertanto la chiamata sincrona dal thread dell'applicazione principale. Usare un thread di lavoro oppure chiamare il metodo in modo asincrono.

**Passaggio 2. Riconnettere i pin**

Per riconnettere i pin, eseguire una query su Filter Graph Manager per l'interfaccia **IGraphConfig** e chiamare [**IGraphConfig:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) o [**IGraphConfig:: RECONFIGURE**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure). Il metodo di **riconnessione** è più semplice da usare. esegue le operazioni seguenti:

-   Arresta i filtri intermedi (filtro 2 nell'esempio) e li rimuove dal grafico.
-   Aggiunge nuovi filtri intermedi, se necessario.
-   Connette tutti i pin.
-   Sospende o esegue i nuovi filtri per trovare la corrispondenza con lo stato del grafico.

Il metodo **Reconnect** include diversi parametri facoltativi che possono essere usati per specificare il tipo di supporto per la connessione pin e il filtro intermedio da usare. Ad esempio:


```C++
pGraph->AddFilter(pNewFilter, L"New Filter for the Graph");
pConfig->Reconnect(
    pPinA,      // Reconnect this output pin...
    pPinD,      // ... to this input pin.
    pMediaType, // Use this media type.
    pNewFilter, // Connect them through this filter.
    NULL, 
    0);     
```



Per informazioni dettagliate, vedere la pagina di riferimento. Se il metodo di **riconnessione** non è sufficientemente flessibile, è possibile usare il metodo **RECONFIGURE** , che chiama un metodo di callback definito dall'applicazione per riconnettere i pin. Per usare questo metodo, implementare l'interfaccia [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) nell'applicazione.

Prima di chiamare **RECONFIGURE**, bloccare il flusso di dati dal pin di output, come descritto in precedenza. Eseguire quindi il push di tutti i dati ancora in sospeso nella sezione del grafico che si sta riconnettendo, come indicato di seguito:

1.  Chiamare [**IPinConnection:: NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) sul pin di input più a valle nella catena di riconnessione (pin D nell'esempio). Passare un handle a un evento Win32.
2.  Chiamare [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul pin di input che è immediatamente a valle dal pin di output in cui è stato bloccato il flusso di dati. (In questo esempio, il flusso di dati è stato bloccato al pin A, quindi è necessario chiamare **EndOfStream** sul pin B).
3.  Attendere che l'evento venga segnalato. Il pin di input (pin D) segnala l'evento quando riceve la notifica di fine del flusso. Ciò indica che nessun dato è in viaggio tra i pin e che il chiamante può riconnettere i pin in modo sicuro.

Si noti che il metodo **IGraphConfig:: Reconnect** gestisce automaticamente i passaggi precedenti. È necessario eseguire questi passaggi solo se si usa il metodo **RECONFIGURE** .

Dopo aver eseguito il push dei dati attraverso il grafo, chiamare **RECONFIGURE** e passare un puntatore all'interfaccia di callback **IGraphConfigCallback** . Il gestore del grafo del filtro chiamerà il metodo [**IGraphConfigCallback:: RECONFIGURE**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) fornito.

**Passaggio 3. Sbloccare il flusso di dati**

Dopo aver riconnesso i pin, sbloccare il flusso di dati chiamando **IPinFlowControl:: Block** con un valore pari a zero per il primo parametro.

> [!Note]  
> Se una riconnessione dinamica viene eseguita da un filtro, è necessario tenere presenti alcuni problemi di Threading. Se il gestore del grafico del filtro tenta di arrestare il filtro, è possibile che si verifichi un deadlock, perché il grafico attende l'arresto del filtro, mentre al tempo stesso il filtro potrebbe essere in attesa del push dei dati nel grafico. Per evitare il possibile deadlock, alcuni dei metodi descritti in questa sezione accettano un handle per un evento Win32. Il filtro deve segnalare l'evento se il gestore del grafico del filtro tenta di arrestare il filtro. Per ulteriori informazioni, vedere [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di grafici dinamici](dynamic-graph-building.md)
</dt> </dl>

 

 



