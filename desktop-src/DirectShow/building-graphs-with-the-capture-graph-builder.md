---
description: Creazione di grafici con il generatore di grafici di acquisizione
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Creazione di grafici con il generatore di grafici di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876957"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a>Creazione di grafici con il generatore di grafici di acquisizione

Nonostante il nome, il generatore di grafici di acquisizione è utile per la creazione di molti tipi di grafici di filtri personalizzati, non solo per l'acquisizione dei grafici. Questo articolo fornisce una breve panoramica su come usare questo oggetto.

Il generatore di grafici di acquisizione espone l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Per iniziare, chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il generatore del grafico di acquisizione e il gestore del grafico dei filtri. Inizializzare quindi il generatore del grafico di acquisizione chiamando [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) con un puntatore al gestore del grafico di filtro, come indicato di seguito:


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a>Connessione di filtri

Il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) connette due o tre filtri insieme in una catena. In genere, il metodo funziona meglio quando ogni filtro non contiene più di un pin di input o di output dello stesso tipo. Questa discussione inizia ignorando i primi due parametri di **RenderStream** e concentrandosi sugli ultimi tre parametri. Il terzo parametro è un puntatore [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , che può specificare un filtro (come puntatore di interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) ) o un pin di output (come puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) ). Il quarto e il quinto parametro specificano i puntatori **IBaseFilter** . Il metodo **RenderStream** connette tutti e tre i filtri in una catena. Si supponga, ad esempio, che *a*, *B* e *C* siano filtri. Si supponga per ora che ogni filtro includa esattamente un pin di input e un pin di output. La chiamata seguente connette a a B, quindi B a C:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

Tutte le connessioni sono "intelligenti", vale a dire che i filtri aggiuntivi vengono aggiunti al grafico in base alle esigenze. Per informazioni dettagliate, vedere [connessione intelligente](intelligent-connect.md). Per connettere solo due filtri, impostare il valore intermedio su **null**. Questa chiamata, ad esempio, connette a C:

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

È possibile creare catene più lunghe chiamando il metodo due volte:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

Se l'ultimo parametro è **null**, il metodo individua automaticamente un renderer predefinito. Usa il [renderer video](video-renderer-filter.md) per video e il [renderer DirectSound](directsound-renderer-filter.md) per l'audio. Così

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

equivale a

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

dove *R* è il renderer appropriato. Tuttavia, per connettere il filtro renderer video mixing anziché il renderer video, è necessario specificarlo in modo esplicito.

Se si specifica un filtro nel terzo parametro, anziché un PIN, potrebbe essere necessario indicare quale pin di output deve essere usato per la connessione. Questo è lo scopo dei primi due parametri del metodo. Il primo parametro si applica solo ai filtri di acquisizione. Specifica un GUID che indica una categoria di pin. Per un elenco completo delle categorie, vedere [impostare la proprietà pin](pin-property-set.md). Due categorie sono valide per tutti i filtri di acquisizione:

-   **\_ \_ blocca acquisizione categoria**
-   **\_anteprima categoria \_ pin**

Se un filtro di acquisizione non fornisce pin distinti per l'acquisizione e l'anteprima, il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserisce un filtro di [Smart Tee](smart-tee-filter.md) , che suddivide il flusso in un flusso di acquisizione e in un flusso di anteprima. Dal punto di vista dell'applicazione, è possibile considerare semplicemente tutti i filtri di acquisizione come aventi pin distinti e ignorare la topologia sottostante del grafo.

Per l'acquisizione di file, connettere il pin di acquisizione a un filtro MUX. Per l'anteprima in tempo reale, connettere il pin di anteprima a un renderer. Se si passa a due categorie, il grafico potrebbe eliminare un numero eccessivo di fotogrammi durante l'acquisizione dei file; Tuttavia, se il grafo è connesso correttamente, i frame di anteprima vengono eliminati in base alle esigenze, in modo da mantenere la velocità effettiva nel flusso di acquisizione.

Nell'esempio seguente viene illustrato come connettere entrambi i flussi:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



Alcuni filtri di acquisizione supportano anche le didascalie chiuse, indicate dalla **\_ categoria pin \_ VBI**. Per acquisire le didascalie chiuse in un file, eseguire il rendering di questa categoria nel filtro MUX. Per visualizzare le didascalie chiuse nella finestra di anteprima, connettersi al renderer:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



Il secondo parametro di [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifica il tipo di supporto ed è in genere uno dei seguenti:

-   \_Audio MEDIATYPE
-   Video di MEDIATYPE \_
-   MEDIATYPE con \_ interfoliazione (DV)

È possibile utilizzare questo parametro ogni volta che i pin di output del filtro supportano l'enumerazione dei tipi di supporto preferiti. Per le origini file, il generatore di grafici di acquisizione aggiunge automaticamente un filtro del parser, se necessario, e quindi esegue una query sui tipi di supporto nel parser. Per un esempio, vedere [ricompressione di un file AVI](recompressing-an-avi-file.md). Se, inoltre, l'ultimo filtro della catena include diversi pin di input, il metodo tenterà di enumerare i tipi di supporto. Tuttavia, non tutti i filtri supportano questa funzionalità.

## <a name="finding-interfaces-on-filters-and-pins"></a>Ricerca di interfacce su filtri e pin

Dopo aver compilato un grafo, in genere è necessario individuare varie interfacce esposte da filtri e pin nel grafico. Ad esempio, un filtro di acquisizione potrebbe esporre l'interfaccia [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) , mentre i pin di output del filtro potrebbero esporre l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) .

Il modo più semplice per trovare un'interfaccia consiste nell'usare il metodo [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) . Questo metodo consente di visualizzare il grafico (filtri e pin) fino a individuare l'interfaccia desiderata. È possibile specificare il punto di partenza per la ricerca ed è possibile limitare la ricerca ai filtri upstream o downstream dal punto di partenza.

L'esempio seguente cerca l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) in un pin di anteprima video:


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> L'argomento [trovare un'interfaccia in un filtro o un pin](find-an-interface-on-a-filter-or-pin.md) Mostra un approccio alternativo che usa l'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) anziché [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2). L'approccio da usare dipende dall'applicazione. Se l'applicazione usa già **ICaptureGraphBuilder2** per compilare il grafo, [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) è un approccio valido. In caso contrario, provare a usare i metodi **IGraphBuilder** .

 

## <a name="finding-pins"></a>Ricerca di pin

Meno comunemente, potrebbe essere necessario individuare un singolo pin in un filtro, sebbene nella maggior parte dei casi i metodi [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) e [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) consentano di evitare il problema. Se è necessario trovare un pin particolare su un filtro, il metodo helper [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) è utile. Specificare la categoria, il tipo di supporto (video o audio), la direzione e se il PIN deve essere scollegato.

Ad esempio, il codice seguente cerca un pin di anteprima video non connesso in un filtro di acquisizione:


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 
