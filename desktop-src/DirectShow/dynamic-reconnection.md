---
description: Riconnessione dinamica
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Riconnessione dinamica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b558a2e00ee2577cf1d31dda7aaebb15b5bd740c6dad5689e70b950c02d4d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966157"
---
# <a name="dynamic-reconnection"></a>Riconnessione dinamica

Nella maggior DirectShow filtri, i pin non possono essere riconnessi mentre il grafico è attivamente in streaming dei dati. L'applicazione deve arrestare il grafo prima di riconnettere i segnaposto. Tuttavia, alcuni filtri supportano le riconnessioni pin mentre il grafo è in esecuzione, un processo noto come riconnessione dinamica. Questa operazione può essere eseguita dall'applicazione o da un filtro nel grafico.

Si consideri ad esempio il grafico nella figura seguente.

![Diagramma dinamico di creazione di grafi](images/dyngraph.png)

Uno scenario per la riconnessione dinamica potrebbe consistere nel rimuovere il filtro 2 dal grafico mentre il grafico è in esecuzione e sostituirlo con un altro filtro. Per il funzionamento di questo scenario, è necessario che siano vere le condizioni seguenti:

-   Il pin di input nel filtro 3 (pin D) deve supportare [**l'interfaccia IPinConnection.**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) Questa interfaccia consente di riconnettere il pin senza arrestare il filtro.
-   Il pin di output nel filtro 1 (pin A) deve essere in grado di bloccare il flusso dei dati multimediali mentre si verifica la riconnessione. Durante la riconnessione non è possibile passare tra il pin A e il pin D. In genere, questo significa che il pin di output deve supportare [**l'interfaccia IPinFlowControl.**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) Tuttavia, se Il filtro 1 è il filtro che avvia la riconnessione, potrebbe avere un meccanismo interno per bloccare il proprio flusso di dati.

La riconnessione dinamica comporterà i passaggi seguenti:

1.  Bloccare il pin A del flusso di dati.
2.  Riconnettere il pin A al pin D, possibilmente tramite un nuovo filtro intermedio.
3.  Sbloccare il pin A in modo che i dati inizino a fluire di nuovo.

**Passaggio 1. Bloccare il flusso di dati**

Per bloccare il flusso di dati, chiamare [**IPinFlowControl::Block al**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) pin A. Questo metodo può essere chiamato in modo asincrono o sincrono. Per chiamare il metodo *in modo asincrono,* creare un oggetto evento Win32 e passare l'handle di evento al **metodo Block.** Il metodo restituirà immediatamente . Attendere che l'evento sia segnalato, usando una funzione come **WaitForSingleObject**. Il pin segnala l'evento quando ha bloccato il flusso di dati. Esempio:


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



Per chiamare il metodo *in modo sincrono,* è sufficiente passare il valore **NULL** anziché l'handle dell'evento. A questo punto il metodo si blocca fino al completamento dell'operazione. Questo problema può verificarsi solo quando il pin non è pronto per distribuire un nuovo campione. Se il filtro è sospeso, questa operazione può richiedere un periodo di tempo arbitrario. Pertanto, non effettuare la chiamata sincrona dal thread principale dell'applicazione. Usare un thread di lavoro oppure chiamare il metodo in modo asincrono.

**Passaggio 2. Riconnettere i pin**

Per riconnettere i pin, eseguire una query in Filter Graph Manager per l'interfaccia **IGraphConfig** e chiamare [**IGraphConfig::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) o [**IGraphConfig::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure). Il **metodo Reconnect** è più semplice da usare. esegue le operazioni seguenti:

-   Arresta i filtri intermedi (filtro 2 nell'esempio) e li rimuove dal grafico.
-   Aggiunge nuovi filtri intermedi, se necessario.
-   Connette tutti i segnaposto.
-   Sospende o esegue i nuovi filtri, in modo che corrispondano allo stato del grafico.

Il **metodo Reconnect** ha diversi parametri facoltativi che possono essere usati per specificare il tipo di supporto per la connessione pin e il filtro intermedio da usare. Esempio:


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



Per informazioni dettagliate, vedere la pagina di riferimento. Se il **metodo Reconnect** non è sufficientemente flessibile, è possibile usare il metodo **Reconfigure,** che chiama un metodo di callback definito dall'applicazione per riconnettere i pin. Per usare questo metodo, implementare [**l'interfaccia IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) nell'applicazione.

Prima di chiamare **Riconfigura**, bloccare il flusso di dati dal pin di output, come descritto in precedenza. Eseguire quindi il push di tutti i dati ancora in sospeso nella sezione del grafico che si sta riconnettendo, come indicato di seguito:

1.  Chiamare [**IPinConnection::NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) sul pin di input più a valle nella catena di riconnessione (pin D nell'esempio). Passare un handle a un evento Win32.
2.  Chiamare [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul pin di input immediatamente a valle dal pin di output in cui è stato bloccato il flusso di dati. In questo esempio il flusso di dati è stato bloccato al pin A, quindi è necessario chiamare **EndOfStream** sul pin B.
3.  Attendere che l'evento sia segnalato. Il pin di input (pin D) segnala l'evento quando riceve la notifica di fine flusso. Ciò indica che nessun dato è in viaggio tra i pin e che il chiamante può riconnettere i pin in modo sicuro.

Si noti che **il metodo IGraphConfig::Reconnect** gestisce automaticamente i passaggi precedenti. È necessario eseguire questi passaggi solo se si usa il **metodo Riconfigura.**

Dopo aver eseguito il push dei dati nel grafico, chiamare **Reconfigure e** passare un puntatore all'interfaccia di callback **IGraphConfigCallback.** Filter Graph Manager chiamerà il [**metodo IGraphConfigCallback::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) fornito.

**Passaggio 3. Sbloccare l'Flow**

Dopo aver riconnesso i pin, sbloccare il flusso di dati chiamando **IPinFlowControl::Block** con un valore pari a zero per il primo parametro.

> [!Note]  
> Se una riconnessione dinamica viene eseguita da un filtro, è necessario tenere presenti alcuni problemi di threading. Se Filter Graph Manager tenta di arrestare il filtro, può verificarsi un deadlock perché il grafico attende l'arresto del filtro, mentre contemporaneamente il filtro potrebbe attendere il push dei dati attraverso il grafico. Per evitare il possibile deadlock, alcuni dei metodi descritti in questa sezione accettano un handle per un evento Win32. Il filtro deve segnalare l'evento se l'Graph manager tenta di arrestare il filtro. Per altre informazioni, vedere [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e [**IPinConnection.**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione Graph dinamica](dynamic-graph-building.md)
</dt> </dl>

 

 



