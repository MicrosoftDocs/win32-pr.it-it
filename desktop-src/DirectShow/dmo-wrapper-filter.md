---
description: DMO Filtro wrapper
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: DMO Filtro wrapper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13383e7539f478327f1a904d60fcd069692180239e76bcfd48bcc090a068e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653041"
---
# <a name="dmo-wrapper-filter"></a>DMO Filtro wrapper

Il filtro wrapper DMO consente a un'DirectShow di usare un oggetto multimediale [DirectX](directx-media-objects.md) (DMO) all'interno di un grafo di filtro. Il filtro esegue il wrapping DMO e gestisce tutti i dettagli dell'uso del DMO, ad esempio il passaggio di dati da e verso l'DMO. Inoltre, il filtro aggrega il DMO, in modo che l'applicazione possa eseguire una query sul filtro per qualsiasi interfaccia COM esponga l DMO intervai.



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| Tipi di supporti pin di input                    | Vedere la sezione Osservazioni                                                                                                                                                                                                                                        |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipi di supporti pin di output                   | Vedere la sezione Osservazioni                                                                                                                                                                                                                                        |
| Interfacce pin di output                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID del filtro                             | CLSID \_ DMOWrapperFilter                                                                                                                                                                                                                            |
| CLSID pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                                                                                                                   |
| File eseguibile                               | Qasf.dll                                                                                                                                                                                                                                           |
| [Merito](merit.md)                       | Vedere la sezione Osservazioni                                                                                                                                                                                                                                        |
| [Categoria filtro](filter-categories.md) | Vedere la sezione Osservazioni                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Commenti

### <a name="limitations"></a>Limitazioni

Il wrapper DMO presenta le limitazioni seguenti:

-   Non supporta gli oggetti DMO con zero input, più input o zero output. Supporta gli oggetti DMO con un input e più output.
-   Non supporta trasporti personalizzati. Tutto il trasporto dei dati viene eseguito tramite [**l'interfaccia IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   Non usa **l'interfaccia IMediaObjectInPlace.** tutte le operazioni di elaborazione vengono eseguite [**usando i metodi IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)

### <a name="pins"></a>Segnaposto

Per ogni flusso di input nel DMO, il filtro crea un pin di input corrispondente. Per ogni flusso di output, crea un pin di output corrispondente. I tipi di supporti supportati da ogni pin dipendono dalla DMO

### <a name="encoder-interfaces"></a>Interfacce del codificatore

Se il DMO è un codificatore video o audio, il pin di output espone [**l'interfaccia IAMStreamConfig.**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) Se il DMO è un codificatore video, il pin di output espone anche [**l'interfaccia IAMVideoCompression.**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) In entrambi i casi, se DMO supporta l'interfaccia , il pin delega al DMO. In caso contrario, il pin fornisce la propria implementazione.

### <a name="streaming"></a>Streaming

Il filtro usa [**l'interfaccia IMemInputPin per**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) gestire tutto il flusso. Non supporta le [**connessioni IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) Il filtro chiama [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) sul DMO solo quando riceve dati da upstream (incluse le notifiche di fine flusso). Di conseguenza, non supporta gli oggetti DMO con zero flussi di input.

### <a name="seeking"></a>riercare

Tutte le richieste di ricerca vengono passate al filtro upstream, tramite il primo pin di input nel wrapper DMO. Per gli oggetti DMO a più output, ciò significa che il filtro upstream potrebbe ricevere più richieste di ricerca quando l'applicazione cerca il grafico.

### <a name="merit"></a>Merito

DirectShow assegna a tutti gli oggetti DMO un valore di incando predefinito pari a **NORMAL \_** + 0x800. Questo valore è compreso tra **PREFER \_ NORMAL** **e \_ PREFERENZIALE.** I filtri del decodificatore hanno in genere un valore **di pregio pari \_** a NORMAL. Di conseguenza, il gestore del grafo dei filtri seleziona in genere DMO decodificatore su un filtro del decodificatore. Per eseguire l'override del valore predefinito, aggiungere una voce del Registro di DMO chiave del Registro di sistema in HKEY \_ CLASSES \_ ROOT \\ CLSID. Includere un **valore DWORD** denominato "Merito" il cui valore specifica il valore.

### <a name="category"></a>Category

Il DMO wrapper non viene visualizzato da solo in alcuna categoria. Quando esegue il wrapping di un DMO, viene visualizzato nella categoria DirectShow corrispondente alla categoria del DMO, sotto il nome del DMO.

### <a name="buffers"></a>Buffer

Il DMO wrapper passa i buffer multimediali al DMO che espongono [**l'interfaccia IMediaBuffer.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer)

In Windows Vista o versioni successive, i buffer multimediali espongono anche l'interfaccia IServiceProvider. Il DMO utilizzare questa interfaccia per ottenere un puntatore al campione multimediale associato al buffer. Usare l'identificatore **di servizio IID \_ IMediaSample**. Un video DMO usare l'interfaccia [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) dell'esempio multimediale per impostare flag interlacciati sull'esempio. Il codice seguente illustra come ottenere il puntatore all'esempio multimediale:


```C++
IServiceProvider *pSp = NULL;
IMediaSample2 *pSample2 = NULL;
HRESULT hr = S_OK;

hr = pBuffer->QueryInterface(IID_IServiceProvider, (void**)&pSp);
if (SUCCEEDED(hr))
{
    hr = pSp->QueryService(
        IID_IMediaSample,  // Service identifier.
        IID_IMediaSample2, // Interface identifier.
        (void**)&pSample2
        );
    if (SUCCEEDED(hr))
    {
        // Set flags (not shown).
        pSample2->Release();
    }
    pSp->Release();
}
```



Per altre informazioni sui flag interlacciati per campione, vedere [**Struttura \_ AM SAMPLE2 \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)

### <a name="quality-control"></a>Controllo qualità

Se il DMO espone [**l'interfaccia IDMOQualityControl,**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) il filtro converte le chiamate [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) sul pin di output in chiamate [**IDMOQualityControl::SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) sul DMO. Il *parametro rtNow* di **SetNow** viene calcolato come somma dei **membri TimeStamp** e **Late** della [**struttura Quality.**](/windows/win32/api/strmif/ns-strmif-quality)

### <a name="using-the-fiter-in-graphedit"></a>Uso di Fiter in GraphModifica

In GraphEdit il filtro DMO wrapper non viene visualizzato sotto il proprio nome. Al contrario, ogni DMO registrato è elencato nella categoria di filtro appropriata. Quando si aggiunge un DMO  tramite la finestra di dialogo Inserisci filtri, GraphEdit crea il filtro wrapper DMO e lo configura per l'uso di DMO.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Oggetti multimediali DirectX](directx-media-objects.md)
</dt> </dl>

 

 
