---
description: Questo argomento descrive come usare DirectShow per riprodurre file multimediali protetti con Windows Media Digital Rights Management (DRM).
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Lettura DRM-Protected file ASF in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178dc0dbaa9a8b8e2e849164106816afc6990c89
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786967"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a>Lettura DRM-Protected file ASF in DirectShow

Questo argomento descrive come usare DirectShow per riprodurre file multimediali protetti con Windows Media Digital Rights Management (DRM).

## <a name="drm-concepts"></a>Concetti relativi a DRM

La protezione di un file multimediale Windows Media DRM prevede due passaggi distinti:

-   Il provider di contenuto esegue il pacchetto del file, ovvero crittografa il file e allega le informazioni sulle licenze all'intestazione del file ASF. Le informazioni sulle licenze includono un URL in cui il client può ottenere la licenza.
-   L'applicazione client acquisisce una licenza per il contenuto.

La creazione del pacchetto avviene prima della distribuzione del file. L'acquisizione della licenza si verifica quando l'utente prova a riprodurre o copiare il file. L'acquisizione della licenza può essere *invisibile* all'utente *o non invisibile all'utente.* L'acquisizione invisibile all'utente non richiede alcuna interazione con l'utente. L'acquisizione non invisibile all'utente richiede all'applicazione di aprire una finestra del browser e visualizzare una pagina Web all'utente. A questo punto, l'utente potrebbe dover fornire informazioni al provider di contenuti. Tuttavia, entrambi i tipi di acquisizione delle licenze richiedono al client di inviare una richiesta HTTP a un server licenze.

### <a name="drm-versions"></a>Versioni di DRM

Esistono diverse versioni Windows Media DRM. Dal punto di vista di un'applicazione client, possono essere raggruppate in due categorie: DRM versione 1 e DRM versione 7 o successiva. La seconda categoria include le versioni 9 e 10 di DRM e la versione 7. Il motivo per classificare le versioni DRM in questo modo è che le licenze della versione 1 vengono gestite in modo leggermente diverso rispetto alle licenze versione 7 o successive. In questa documentazione il termine licenza *versione 7* indica la versione 7 o successiva.

È anche importante distinguere la creazione di pacchetti DRM dalla licenza DRM. Se il file viene in pacchetto usando Windows Media Rights Manager versione 7 o successiva, l'intestazione DRM può contenere un URL di licenza versione 1 oltre all'URL di licenza versione 7. L'URL della licenza versione 1 consente ai lettori meno recenti che non supportano la versione 7 di ottenere una licenza per il contenuto. Tuttavia, il contrario non è vero, quindi un file con pacchetto versione 1 non può avere un URL di licenza versione 7.

### <a name="application-security-level"></a>Livello di sicurezza dell'applicazione

Per riprodurre file protetti da DRM, l'applicazione client deve essere collegata a una libreria statica fornita in formato binario da Microsoft. Questa libreria, che identifica in modo univoco l'applicazione, viene talvolta chiamata libreria stub. Alla libreria stub è assegnato un livello di sicurezza, il cui valore è determinato dal contratto di licenza firmato quando è stata ottenuta la libreria stub.

Il provider di contenuti imposta un livello di sicurezza minimo necessario per acquisire la licenza. Se il livello di sicurezza della libreria stub è inferiore al livello di sicurezza minimo richiesto dal server licenze, l'applicazione non può ottenere la licenza.

### <a name="individualization"></a>Individualizzazione

Per aumentare la sicurezza, un'applicazione può aggiornare i componenti DRM nel computer del client. Questo aggiornamento, denominato individualizzazione, differenzia la copia dell'applicazione dell'utente da tutte le altre copie della stessa applicazione. L'intestazione DRM di un file protetto può specificare un livello di individualizzazione minimo. Per altre informazioni, vedere la documentazione relativa a WMRMHeader.IndividualizedVersion in Windows Media Rights Manager SDK.

Poiché il servizio di individualizzazione Microsoft gestisce le informazioni dell'utente, è necessario visualizzare l'informativa sulla privacy Microsoft o fornire un collegamento a tale pagina nel sito Web Microsoft prima che l'applicazione personalizzi: <https://go.microsoft.com/fwlink/p/?linkid=10240> .

## <a name="provide-the-software-certificate"></a>Fornire il certificato software

Per consentire all'applicazione di usare la licenza DRM,  l'applicazione deve fornire un certificato software o una chiave a Filter Graph Manager. Questa chiave è contenuta in una libreria statica individualizzata per l'applicazione. Per informazioni su come ottenere la libreria individualizzata, vedere [Obtaining the Required DRM Library](../wmformat/obtaining-the-required-drm-library.md) (Ottenere la libreria DRM richiesta) nella documentazione di Windows Media Format SDK.

Per fornire la chiave software, seguire questa procedura:

1.  Collegamento alla libreria statica.
2.  Implementare **l'interfaccia IServiceProvider.**
3.  Eseguire una query su Filter Graph Manager per [**l'interfaccia IObjectWithSite.**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
4.  Chiamare [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) con un puntatore all'implementazione di **IServiceProvider**.
5.  Filter Graph Manager chiamerà **IServiceProvider::QueryService**, specificando **\_ IWMReader IID** per l'identificatore del servizio.
6.  Nell'implementazione **di QueryService** chiamare [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) per creare la chiave software.

Il codice seguente illustra come implementare il **metodo QueryService:**


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



Il codice seguente illustra come chiamare [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) in Filter Graph Manager:


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





## <a name="building-the-playback-graph"></a>Compilazione del Graph

Per riprodurre un file ASF protetto da DRM, seguire questa procedura:

1.  Creare Filter [Graph Manager](filter-graph-manager.md) e usare l'interfaccia [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) per la registrazione per gli eventi del grafo.
2.  Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare una nuova istanza del filtro [lettore ASF WM.](wm-asf-reader-filter.md)
3.  Chiamare [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafico dei filtri.
4.  Eseguire una query sul filtro per [**l'interfaccia IFileSourceFilter.**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)
5.  Chiamare [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) con l'URL del file.
6.  Gestire [**gli eventi EC \_ WMT \_ EVENT.**](ec-wmt-event.md)
7.  Nel primo evento [**\_ EC WMT \_ EVENT**](ec-wmt-event.md) eseguire una query sul filtro [lettore ASF WM](wm-asf-reader-filter.md) per **l'interfaccia IServiceProvider.**
8.  Chiamare **IServiceProvider::QueryService** per ottenere un puntatore [**all'interfaccia IWMDRMReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
9.  Chiamare [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) per eseguire il rendering dei pin di output del filtro [lettore ASF WM.](wm-asf-reader-filter.md)

> [!Note]  
> Quando si apre un file protetto da DRM, non chiamare [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) per creare il grafico dei filtri. Il filtro lettore ASF WM non può connettersi ad altri filtri finché non viene acquisita la licenza DRM. Questo passaggio richiede all'applicazione di usare [**l'interfaccia IWMDRMReader,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) che deve essere ottenuta dal filtro, come descritto nei passaggi da 7 a 8. È quindi necessario creare il filtro e aggiungerlo al grafico

 

> [!Note]  
> È importante registrarsi per gli eventi del grafo (passaggio 1) prima di aggiungere il filtro [lettore ASF WM](wm-asf-reader-filter.md) al grafo (passaggio 3), perché l'applicazione deve gestire gli eventi [**EC \_ WMT \_ EVENT.**](ec-wmt-event.md) Gli eventi vengono inviati quando [**viene chiamato Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) (passaggio 5).

 

Il codice seguente illustra come compilare il grafo:


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




| C++ | 
|-----|
| <pre><code>            if (FAILED(hr))            {                goto done;            }            hr = RenderOutputPins(pGraph, m_pReader);    }    else    {        // Not a Windows Media file, so just render the standard way.        hr = pGraph-&gt;RenderFile(pwszFile, NULL);    }done:    return hr;}</code></pre> | 




Nel codice precedente la funzione enumera i pin di output nel filtro `RenderOutputPins` [lettore ASF WM](wm-asf-reader-filter.md) e chiama [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) per ogni pin.


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



Il codice seguente illustra come ottenere un puntatore [**all'interfaccia IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) dal lettore [ASF WM:](wm-asf-reader-filter.md)


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

 

 
