---
description: Filtro wrapper DMO
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: Filtro wrapper DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b01ee006203e2e1fd328bacc13c01de4a3b25f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482436"
---
# <a name="dmo-wrapper-filter"></a>Filtro wrapper DMO

Il filtro del wrapper DMO consente a un'applicazione DirectShow di usare un oggetto DMO ( [DirectX Media Object](directx-media-objects.md) ) in un grafico di filtro. Il filtro esegue il wrapping di DMO e gestisce tutti i dettagli dell'uso di DMO, ad esempio il passaggio di dati da e verso DMO. Inoltre, il filtro aggrega il DMO, in modo che l'applicazione possa eseguire una query sul filtro per tutte le interfacce COM esposte da DMO.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| Tipi di supporti pin di input                    | Vedere la sezione Osservazioni                                                                                                                                                                                                                                        |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipi di supporti pin di output                   | Vedere la sezione Osservazioni                                                                                                                                                                                                                                        |
| Interfacce del PIN di output                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID filtro                             | \_DMOWRAPPERFILTER CLSID                                                                                                                                                                                                                            |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                                                                                                                   |
| File eseguibile                               | Qasf.dll                                                                                                                                                                                                                                           |
| [Merito](merit.md)                       | Vedere la sezione Osservazioni                                                                                                                                                                                                                                        |
| [Categoria filtro](filter-categories.md) | Vedere la sezione Osservazioni                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Commenti

### <a name="limitations"></a>Limitazioni

Il wrapper DMO presenta le limitazioni seguenti:

-   Non supporta DMOs con zero input, più input o zero output. Supporta DMOs con un input e più output.
-   Non supporta i trasporti personalizzati. Tutto il trasporto di dati viene eseguito tramite l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Non usa l'interfaccia **IMediaObjectInPlace** ; tutte le operazioni di elaborazione vengono eseguite usando i metodi [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .

### <a name="pins"></a>Segnaposto

Per ogni flusso di input su DMO, il filtro crea un pin di input corrispondente. Per ogni flusso di output, viene creato un pin di output corrispondente. I tipi di supporto supportati da ciascun pin dipendono da DMO

### <a name="encoder-interfaces"></a>Interfacce del codificatore

Se DMO è un codificatore video o un codificatore audio, il pin di output espone l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) . Se DMO è un codificatore video, il pin di output espone anche l'interfaccia [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) . In entrambi i casi, se DMO supporta l'interfaccia, il pin delega a DMO. In caso contrario, il pin fornisce una propria implementazione.

### <a name="streaming"></a>Streaming

Il filtro usa l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) per gestire tutti i flussi. Non supporta le connessioni [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Il filtro chiama [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) su DMO solo quando riceve dati da upstream (incluse le notifiche di fine flusso). Non supporta pertanto DMOs con zero flussi di input.

### <a name="seeking"></a>La ricerca

Tutte le richieste Seek vengono passate al filtro upstream, tramite il primo pin di input nel wrapper DMO. Per DMOs a più output, ciò significa che il filtro upstream può ricevere più richieste di ricerca quando l'applicazione cerca il grafo.

### <a name="merit"></a>Merito

DirectShow assegna a tutti DMOs un valore predefinito di Merit **\_ Normal** + 0x800. Questo valore è compreso tra **Merit \_ Normal** e **Merit \_ preferenziale**. I filtri decodificatore in genere hanno un valore Merit **\_ Normal**. Di conseguenza, il gestore del grafo del filtro selezionerà in genere un decodificatore DMO su un filtro del decodificatore. Per eseguire l'override del valore Merit predefinito, aggiungere una voce del registro di sistema alla chiave del registro di sistema DMO nel \_ CLSID radice delle classi HKEY \_ \\ . Includere un valore **DWORD** denominato "Merit" il cui valore specifichi il merito.

### <a name="category"></a>Category

Il filtro del wrapper DMO non viene visualizzato da solo in alcuna categoria. Quando esegue il wrapping di un DMO, viene visualizzato nella categoria DirectShow che corrisponde alla categoria DMO, sotto il nome del DMO.

### <a name="buffers"></a>Buffer

Il filtro del wrapper DMO passa i buffer multimediali a DMO che espongono l'interfaccia [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) .

In Windows Vista o versioni successive, i buffer multimediali espongono anche l'interfaccia IServiceProvider. DMO può usare questa interfaccia per ottenere un puntatore all'esempio multimediale associato al buffer. Usare l'identificatore del servizio **IID \_ IMediaSample**. Un video DMO può usare l'interfaccia [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) dell'esempio multimediale per impostare i flag di interlacciamento nell'esempio. Il codice seguente illustra come ottenere il puntatore all'esempio di supporto:


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



Per ulteriori informazioni sui flag di interlacciamento per campione, vedere la [**\_ struttura delle \_ Proprietà SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).

### <a name="quality-control"></a>Controllo qualità

Se DMO espone l'interfaccia [**IDMOQualityControl**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) , il filtro converte [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) calls sul rispettivo pin di output in [**IDMOQualityControl:: SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) chiama su DMO. Il parametro *rtNow* di **SetNow** viene calcolato come la somma del **timestamp** e dei membri **tardivi** della struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) .

### <a name="using-the-fiter-in-graphedit"></a>Uso di Fiter in GraphEdit

In GraphEdit il filtro del wrapper DMO non viene visualizzato con il proprio nome. Ogni DMO registrato viene invece elencato sotto la categoria di filtro appropriata. Quando si aggiunge una DMO tramite la finestra di dialogo **Inserisci filtri** , GraphEdit crea il filtro del wrapper DMO e lo configura per l'uso di tale DMO.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Oggetti multimediali DirectX](directx-media-objects.md)
</dt> </dl>

 

 
