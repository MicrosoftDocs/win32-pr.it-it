---
description: Questo argomento descrive come usare DirectShow per riprodurre file multimediali protetti con Windows Media Digital Rights Management (DRM).
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Lettura di DRM-Protected file ASF in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a90b61982d6c7c444ddcf53948c225b6fc685
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320843"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a>Lettura di DRM-Protected file ASF in DirectShow

Questo argomento descrive come usare DirectShow per riprodurre file multimediali protetti con Windows Media Digital Rights Management (DRM).

## <a name="drm-concepts"></a>Concetti relativi a DRM

La protezione di un file multimediale con Windows Media DRM prevede due passaggi distinti:

-   Il provider di contenuti esegue il pacchetto del file, ovvero crittografa il file e connette le informazioni sulle licenze all'intestazione del file ASF. Le informazioni sulle licenze includono un URL in cui il client può ottenere la licenza.
-   L'applicazione client acquisisce una licenza per il contenuto.

Il pacchetto si verifica prima della distribuzione del file. L'acquisizione della licenza si verifica quando l'utente tenta di riprodurre o copiare il file. L'acquisizione della licenza può essere *invisibile* all'utente o *non invisibile all'utente*. L'acquisizione invisibile all'utente non richiede alcuna interazione con l'utente. Per l'acquisizione non invisibile all'utente è necessario che l'applicazione apra una finestra del browser e visualizzi una pagina Web. A questo punto, l'utente potrebbe dover fornire un tipo di informazioni al provider di contenuti. Tuttavia, entrambi i tipi di acquisizione della licenza richiedono che il client invii una richiesta HTTP a un server licenze.

### <a name="drm-versions"></a>Versioni DRM

Sono presenti diverse versioni di Windows Media DRM. Dal punto di vista di un'applicazione client, possono essere raggruppate in due categorie: DRM versione 1 e DRM versione 7 o successiva. La seconda categoria include le versioni 9 e 10 di DRM, nonché la versione 7. Il motivo per la categorizzazione delle versioni DRM in questo modo è che le licenze della versione 1 sono gestite in modo diverso rispetto alle licenze della versione 7 o successive. In questa documentazione, il termine *licenza versione 7* indica la versione 7 o successiva.

È anche importante distinguere la creazione di pacchetti DRM dalla licenza DRM. Se il file è incluso in un pacchetto con Windows Media Rights Manager versione 7 o successiva, l'intestazione DRM può contenere un URL di licenza della versione 1 oltre all'URL della licenza della versione 7. L'URL di licenza della versione 1 consente ai lettori meno recenti che non supportano la versione 7 di ottenere una licenza per il contenuto. Tuttavia, il contrario non è vero, quindi un file con la confezione della versione 1 non può avere un URL di licenza della versione 7.

### <a name="application-security-level"></a>Livello di sicurezza dell'applicazione

Per riprodurre file protetti da DRM, l'applicazione client deve essere collegata a una libreria statica fornita in formato binario da Microsoft. Questa libreria, che identifica in modo univoco l'applicazione, viene talvolta chiamata libreria stub. Alla libreria stub è assegnato un livello di sicurezza, il cui valore è determinato dal contratto di licenza firmato quando si è ottenuta la libreria stub.

Il provider di contenuti imposta un livello di sicurezza minimo necessario per acquisire la licenza. Se il livello di sicurezza della libreria stub è inferiore al livello di sicurezza minimo richiesto dal server licenze, l'applicazione non è in grado di ottenere la licenza.

### <a name="individualization"></a>Individualizzazione

Per aumentare la sicurezza, un'applicazione può aggiornare i componenti DRM nel computer del client. Questo aggiornamento, denominato individualizzazione, distingue la copia dell'applicazione dell'utente da tutte le altre copie della stessa applicazione. È possibile che l'intestazione DRM di un file protetto specifichi un livello di individualizzazione minimo. Per ulteriori informazioni, vedere la documentazione relativa a WMRMHeader. IndividualizedVersion in Windows Media Rights Manager SDK.

Poiché il servizio di individualizzazione Microsoft gestisce le informazioni dell'utente, è necessario visualizzare l'informativa sulla privacy di Microsoft o fornire un collegamento a tale pagina nel sito Web Microsoft prima dell'applicazione individua: <https://go.microsoft.com/fwlink/p/?linkid=10240> .

## <a name="provide-the-software-certificate"></a>Fornire il certificato software

Per consentire all'applicazione di utilizzare la licenza DRM, è necessario che l'applicazione fornisca una *chiave* o un certificato software al gestore del grafico dei filtri. Questa chiave è contenuta in una libreria statica che viene personalizzata per l'applicazione. Per informazioni su come ottenere la libreria personalizzata, vedere [ottenere la libreria DRM necessaria](../wmformat/obtaining-the-required-drm-library.md) nella documentazione di Windows Media Format SDK.

Per fornire la chiave software, seguire questa procedura:

1.  Collegamento alla libreria statica.
2.  Implementare l'interfaccia **IServiceProvider** .
3.  Eseguire una query su Filter Graph Manager per l'interfaccia [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) .
4.  Chiamare [**IObjectWithSite:: SESITE**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) con un puntatore all'implementazione di **IServiceProvider**.
5.  Il gestore del grafico del filtro chiamerà **IServiceProvider:: QueryService**, specificando **IID \_ IWMReader** per l'identificatore del servizio.
6.  Nell'implementazione di **QueryService**, chiamare [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) per creare la chiave software.

Nel codice seguente viene illustrato come implementare il metodo **QueryService** :


```C++
STDMETHODIMP Player::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (ppv == NULL ) 
    { 
        return E_POINTER; 
    }

    if (siid == __uuidof(IWMReader) && riid == __uuidof(IUnknown))
    {
        IUnknown *punkCert;

        HRESULT hr = WMCreateCertificate(&punkCert);

        if (SUCCEEDED(hr))
        {
            *ppv = (void *) punkCert;
        }

        return hr;
    }
    return E_NOINTERFACE;
}
```



Nel codice riportato di seguito viene illustrato [**come chiamare il**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) metodo in gestione grafico dei filtri:


```C++
HRESULT Player::CreateFilterGraph()
{
    CComPtr<IObjectWithSite> pSite;

    HRESULT hr = pGraph.CoCreateInstance(CLSID_FilterGraph);

    if (FAILED(hr))
    {
        goto done;
    }

    // Register the application as a site (service).
    hr = pGraph->QueryInterface(&pSite);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSite->SetSite(this);


done:
    return hr;
}
```





## <a name="building-the-playback-graph"></a>Creazione del grafico di riproduzione

Per riprodurre un file ASF protetto da DRM, seguire questa procedura:

1.  Creare il [gestore del grafo del filtro](filter-graph-manager.md) e usare l'interfaccia [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) per registrare eventi Graph.
2.  Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare una nuova istanza del filtro [WM ASF Reader](wm-asf-reader-filter.md) .
3.  Chiamare [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafico dei filtri.
4.  Eseguire una query sul filtro per l'interfaccia [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .
5.  Chiamare [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) con l'URL del file.
6.  Gestisce gli eventi di [**\_ \_ evento WMT EC**](ec-wmt-event.md) .
7.  Nel primo evento [**EC \_ WMT \_ evento**](ec-wmt-event.md) , eseguire una query sul filtro [WM ASF Reader](wm-asf-reader-filter.md) per l'interfaccia **IServiceProvider** .
8.  Chiamare **IServiceProvider:: QueryService** per ottenere un puntatore all'interfaccia [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .
9.  Chiamare [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) per eseguire il rendering dei pin di output del filtro [WM ASF Reader](wm-asf-reader-filter.md) .

> [!Note]  
> Quando si apre un file protetto da DRM, non chiamare [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) per creare il grafico dei filtri. Il filtro WM ASF Reader non è in grado di connettersi ad altri filtri fino a quando non viene acquistata la licenza DRM. Per questo passaggio è necessario che l'applicazione usi l'interfaccia [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) , che deve essere ottenuta dal filtro, come descritto nei passaggi 7-8. Pertanto, è necessario creare il filtro e aggiungerlo al grafo

 

> [!Note]  
> È importante registrarsi per gli eventi Graph (passaggio 1) prima di aggiungere il filtro [WM ASF Reader](wm-asf-reader-filter.md) al grafo (passaggio 3), perché l'applicazione deve gestire gli eventi dell' [**\_ \_ evento EC WMT**](ec-wmt-event.md) . Gli eventi vengono inviati quando viene chiamato il metodo [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) (passaggio 5).

 

Nel codice seguente viene illustrato come compilare il grafico:


```C++
HRESULT Player::LoadMediaFile(PCWSTR pwszFile)
{


    BOOL bIsWindowsMediaFile = IsWindowsMediaFile(pwszFile);

    HRESULT hr = S_OK;

    // If this is the first time opening the file, create the
    // filter graph and add the WM ASF Reader filter.

    if (m_DRM.State() == DRM_INITIAL)
    {
        hr = CreateFilterGraph();
        if (FAILED(hr))
        {
            goto done;
        }

        // Use special handling for Windows Media files.
        if (bIsWindowsMediaFile)
        {
            // Add the ASF Reader filter to the graph.
            hr = m_pReader.CoCreateInstance(CLSID_WMAsfReader);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pGraph->AddFilter(m_pReader, NULL);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = m_pReader->QueryInterface(&m_pFileSource);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    }

    if (bIsWindowsMediaFile)
    {
            hr = m_pFileSource->Load(pwszFile, NULL);
```

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            if (FAILED(hr))
            {
                goto done;
            }
            hr = RenderOutputPins(pGraph, m_pReader);
    }
    else
    {
        // Not a Windows Media file, so just render the standard way.
        hr = pGraph->RenderFile(pwszFile, NULL);
    }

done:
    return hr;
}</code></pre></td>
</tr>
</tbody>
</table>



Nel codice precedente, la `RenderOutputPins` funzione enumera i pin di output sul filtro [WM ASF Reader](wm-asf-reader-filter.md) e chiama [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) per ogni pin.


```C++
HRESULT RenderOutputPins(IGraphBuilder *pGraph, IBaseFilter *pFilter)
{
    CComPtr<IEnumPins>  pEnumPin = NULL;
    CComPtr<IPin>       pConnectedPin;
    CComPtr<IPin>       pPin;

    // Enumerate all pins on the filter
    HRESULT hr = pFilter->EnumPins(&pEnumPin);
    if (FAILED(hr))
    {
        goto done;
    }

    // Step through every pin, looking for the output pins.
    while (S_OK == (hr = pEnumPin->Next(1, &pPin, NULL)))
    {
        // Skip connected pins.
        hr = pPin->ConnectedTo(&pConnectedPin);
        if (hr == VFW_E_NOT_CONNECTED)
        {
            PIN_DIRECTION PinDirection;
            hr = pPin->QueryDirection(&PinDirection);

            if ((S_OK == hr) && (PinDirection == PINDIR_OUTPUT))
            {
                hr = pGraph->Render(pPin);
            }
        }

        pConnectedPin.Release();
        pPin.Release();

        // If there was an error, stop enumerating.
        if (FAILED(hr))
        {
            break;
        }
    }

done:
    return hr;
}
```



Il codice seguente illustra come ottenere un puntatore all'interfaccia [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) dal [lettore di WM ASF](wm-asf-reader-filter.md):


```C++
HRESULT DrmManager::Initialize(IBaseFilter *pFilter)
{


    CComPtr<IServiceProvider> pService;
    CComPtr<IWMDRMReader> pDrmReader;

    HRESULT hr = pFilter->QueryInterface(&pService);
    if (SUCCEEDED(hr))
    {
        hr = pService->QueryService(
            __uuidof(IWMDRMReader), IID_PPV_ARGS(&m_pDrmReader));
    }
    return hr;
}
```





## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
