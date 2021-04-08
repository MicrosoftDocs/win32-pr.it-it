---
description: Questo argomento descrive come supportare l'accelerazione video DirectX (DXVA) 2,0 in un filtro del decodificatore DirectShow.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Supporto di DXVA 2,0 in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880050"
---
# <a name="supporting-dxva-20-in-directshow"></a>Supporto di DXVA 2,0 in DirectShow

Questo argomento descrive come supportare l'accelerazione video DirectX (DXVA) 2,0 in un filtro del decodificatore DirectShow. In particolare, descrive la comunicazione tra il decodificatore e il renderer video. In questo argomento non viene descritto come implementare la decodifica DXVA.

-   [Prerequisiti](#prerequisites)
-   [Note sulla migrazione](#migration-notes)
-   [Ricerca di una configurazione del decodificatore](#finding-a-decoder-configuration)
-   [Notifica al renderer video](#notifying-the-video-renderer)
-   [Allocazione di buffer non compressi](#allocating-uncompressed-buffers)
-   [Decodifica](#decoding)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

In questo argomento si presuppone che l'utente abbia familiarità con la scrittura di filtri DirectShow. Per ulteriori informazioni, vedere l'argomento relativo alla [scrittura dei filtri DirectShow](../directshow/writing-directshow-filters.md) nella documentazione di DirectShow SDK. Gli esempi di codice in questo argomento presuppongono che il filtro decodificatore sia derivato dalla classe [**CTransformFilter**](../directshow/ctransformfilter.md) , con la definizione di classe seguente:


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



Nella parte restante di questo argomento, il termine *decodificatore* indica il filtro del decodificatore, che riceve video compresso e genera video non compressi. Il termine *dispositivo decodificatore* si riferisce a un acceleratore video hardware implementato dal driver Graphics.

Ecco i passaggi di base che devono essere eseguiti da un filtro decodificatore per supportare DXVA 2,0:

1.  Negoziare un tipo di supporto.
2.  Trovare una configurazione del decodificatore DXVA.
3.  Notifica al renderer video che il decodificatore usa la decodifica DXVA.
4.  Fornire un allocatore personalizzato che alloca superfici Direct3D.

Questi passaggi sono descritti in modo più dettagliato nella parte restante di questo argomento.

## <a name="migration-notes"></a>Note sulla migrazione

Se si esegue la migrazione da DXVA 1,0, è necessario tenere presenti alcune differenze significative tra le due versioni:

-   DXVA 2,0 non usa le interfacce [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) e [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) , perché il decodificatore può accedere alle API DXVA 2,0 direttamente tramite l'interfaccia [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
-   Durante la negoziazione del tipo di supporto, il decodificatore non usa un GUID di accelerazione video come sottotipo. Il sottotipo è invece solo il formato video non compresso, ad esempio NV12, come per la decodifica software.
-   La procedura per la configurazione dell'acceleratore è cambiata. In DXVA 1,0, il decodificatore chiama **Execute** con una struttura **\_ ConfigPictureDecode di DXVA** per configurare il accerlator. In DXVA 2,0, il decodificatore usa l'interfaccia [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) , come descritto nella sezione successiva.
-   Il decodificatore alloca i buffer non compressi. Il renderer video non li alloca più.
-   Anziché chiamare [**IAMVideoAccelerator::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) per visualizzare il frame decodificato, il decodificatore recapita il frame al renderer chiamando [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), come con la decodifica software.
-   Il decodificatore non è più responsabile del controllo quando i buffer dei dati sono sicuri per gli aggiornamenti. Pertanto DXVA 2,0 non dispone di alcun metodo equivalente a [**IAMVideoAccelerator:: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).
-   Il renderer video esegue la fusione di sottoimmagini, usando le API del processore video DXVA 2.0. I decodificatori che forniscono le immagini secondarie (ad esempio, i decodificatori DVD) devono inviare i dati di un'immagine in un pin di output separato.

Per le operazioni di decodifica, DXVA 2,0 usa le stesse strutture di dati di DXVA 1,0.

Il filtro EVR (Enhanced video renderer) supporta DXVA 2,0. I filtri renderer di video mixing (VMR-7 e VMR-9) supportano solo DXVA 1,0.

## <a name="finding-a-decoder-configuration"></a>Ricerca di una configurazione del decodificatore

Una volta negoziato il tipo di supporto di output, il decodificatore deve trovare una configurazione compatibile per il dispositivo DXVA decoder. È possibile eseguire questo passaggio all'interno del metodo [**CBaseOutputPin:: CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) del PIN di output. Questo passaggio garantisce che il driver di grafica supporti le funzionalità richieste dal decodificatore, prima del commit del decodificatore nell'uso di DXVA.

Per trovare una configurazione per il dispositivo di decodificatore, eseguire le operazioni seguenti:

1.  Eseguire una query sul pin di input del renderer per l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . Il GUID del servizio è \_ il \_ servizio accelerazione video \_ .
3.  Chiamare [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) per ottenere un handle per il dispositivo Direct3D del renderer.
4.  Chiamare [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) e passare l'handle del dispositivo. Questo metodo restituisce un puntatore all'interfaccia [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .
5.  Chiamare [**IDirectXVideoDecoderService:: GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Questo metodo restituisce una matrice di GUID del dispositivo del decodificatore.
6.  Scorrere la matrice dei GUID del decodificatore per trovare quelli supportati dal filtro del decodificatore. Per un decodificatore MPEG-2, ad esempio, si cercherà **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** o **DXVA2 \_ ModeMPEG2 \_ VLD.**

7.  Quando si trova un GUID del dispositivo del decodificatore candidato, passare il GUID al metodo [**IDirectXVideoDecoderService:: GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) . Questo metodo restituisce una matrice di formati di destinazione di rendering, specificati come valori **D3DFORMAT** .
8.  Scorrere i formati della destinazione di rendering e cercarne uno corrispondente al formato di output. In genere, un dispositivo di decodificatore supporta un unico formato di destinazione di rendering. Il filtro del decodificatore deve connettersi al renderer usando questo sottotipo. Nella prima chiamata a [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), il decodificatore può denominare il formato della destinazione di rendering e quindi restituire questo formato come tipo di output preferito.

9.  Chiamare [**IDirectXVideoDecoderService:: GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Passare lo stesso GUID del dispositivo di decodificatore, insieme a una struttura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) che descrive il formato proposto. Il metodo restituisce una matrice di [**strutture \_ ConfigPictureDecode di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) . Ogni struttura descrive una possibile configurazione per il dispositivo di decodificatore.

10. Supponendo che i passaggi precedenti abbiano esito positivo, archiviare l'handle del dispositivo Direct3D, il GUID del dispositivo del decodificatore e la struttura di configurazione. Il filtro utilizzerà queste informazioni per creare il dispositivo di decodificatore.

Il codice seguente illustra come trovare una configurazione del decodificatore.


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



Poiché questo esempio è generico, alcune della logica sono state inserite in funzioni helper che devono essere implementate dal decodificatore. Nel codice seguente vengono illustrate le dichiarazioni per queste funzioni:


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a>Notifica al renderer video

Se il decodificatore trova una configurazione del decodificatore, il passaggio successivo consiste nel notificare al renderer video che il decodificatore userà l'accelerazione hardware. È possibile eseguire questo passaggio all'interno del metodo [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) . Questo passaggio deve verificarsi prima che l'allocatore venga selezionato, perché influiscono sulla modalità di selezione dell'allocatore.

1.  Eseguire una query sul pin di input del renderer per l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere un puntatore all'interfaccia [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) . Il GUID del servizio è il **\_ \_ \_ servizio accelerazione video**.
3.  Chiamare [**IDirectXVideoMemoryConfiguration:: GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in un ciclo, incrementando la variabile *dwTypeIndex* da zero. Arrestare quando il metodo restituisce il valore **DXVA2 \_ SurfaceType \_ DecoderRenderTarget** nel parametro *pdwType* . Questo passaggio garantisce che il renderer video supporti la decodifica con accelerazione hardware. Questo passaggio avrà sempre esito positivo per il filtro EVR.
4.  Se il passaggio precedente ha avuto esito positivo, chiamare [**IDirectXVideoMemoryConfiguration:: SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) con il valore DXVA2 \_ SurfaceType \_ DecoderRenderTarget. La chiamata di **SetSurfaceType** con questo valore inserisce il renderer video in modalità DXVA. Quando il renderer video è in questa modalità, il decodificatore deve fornire il proprio allocatore.

Il codice seguente illustra come inviare una notifica al renderer video.


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



Se il decodificatore trova una configurazione valida e invia una notifica al renderer video, il decodificatore può usare DXVA per la decodifica. Il decodificatore deve implementare un allocatore personalizzato per il pin di output, come descritto nella sezione successiva.

## <a name="allocating-uncompressed-buffers"></a>Allocazione di buffer non compressi

In DXVA 2,0, il decodificatore è responsabile dell'allocazione di superfici Direct3D da usare come buffer video non compressi. Pertanto, il decodificatore deve implementare un allocatore personalizzato che creerà le superfici. Gli esempi di supporti forniti da questo allocatore conterranno i puntatori alle superfici Direct3D. EVR recupera un puntatore all'area chiamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) nell'esempio multimediale. L'identificatore del servizio è il **\_ \_ servizio buffer** di.

Per fornire l'allocatore personalizzato, seguire questa procedura:

1.  Definire una classe per gli esempi di supporti. Questa classe può derivare dalla classe [**CMediaSample**](../directshow/cmediasample.md) . All'interno di questa classe, eseguire le operazioni seguenti:
    -   Archiviare un puntatore alla superficie Direct3D.
    -   Implementare l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . Nel metodo [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , se il GUID del servizio è **il \_ \_ servizio buffer**, eseguire una query sulla superficie Direct3D per l'interfaccia richiesta. In caso contrario, **GetService** può restituire il **\_ \_ \_ servizio MF E non supportato**.
    -   Eseguire l'override del metodo [**CMediaSample:: Getpointer**](../directshow/cmediasample-getpointer.md) per restituire E \_ NOTIMPL.
2.  Definire una classe per l'allocatore. L'allocatore può derivare dalla classe [**CBaseAllocator**](../directshow/cbaseallocator.md) . All'interno di questa classe, eseguire le operazioni seguenti.
    -   Eseguire l'override del metodo [**CBaseAllocator:: Alloc**](../directshow/cbaseallocator-alloc.md) . All'interno di questo metodo, chiamare [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) per creare le superfici. (L'interfaccia [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) eredita questo metodo da [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)).
    -   Eseguire l'override del metodo [**CBaseAllocator:: Free**](../directshow/cbaseallocator-free.md) per rilasciare le superfici.
3.  Nel pin di output del filtro, eseguire l'override del metodo [**CBaseOutputPin:: InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) . All'interno di questo metodo, creare un'istanza dell'allocatore personalizzato.
4.  Nel filtro implementare il metodo [**CTransformFilter::D ecidebuffersize**](../directshow/ctransformfilter-decidebuffersize.md) . Il parametro *pProperties* indica il numero di superfici necessarie per il EVR. Aggiungere a questo valore il numero di superfici richieste dal decodificatore e chiamare [**IMemAllocator::**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) SetValue nell'allocatore.

Il codice seguente illustra come implementare la classe di esempio media:


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



Nel codice seguente viene illustrato come implementare il metodo [**Alloc**](../directshow/cbaseallocator-alloc.md) nell'allocatore.


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



Ecco il codice per il metodo [**gratuito**](../directshow/cbaseallocator-free.md) :


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



Per ulteriori informazioni sull'implementazione di allocatori personalizzati, vedere l'argomento relativo alla [fornitura di un allocatore personalizzato](../directshow/providing-a-custom-allocator.md) nella documentazione di DirectShow SDK.

## <a name="decoding"></a>Decodifica

Per creare il dispositivo di decodificatore, chiamare [**IDirectXVideoDecoderService:: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). Il metodo restituisce un puntatore all'interfaccia [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) del dispositivo di decodificatore.

In ogni frame, chiamare [**IDirect3DDeviceManager9:: TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) per testare l'handle del dispositivo. Se il dispositivo è stato modificato, il metodo restituisce \_ il \_ nuovo \_ dispositivo video DXVA2 E \_ . In tal caso, effettuare le operazioni seguenti:

1.  Chiudere l'handle del dispositivo chiamando [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Rilasciare i puntatori [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) e [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
3.  Aprire un nuovo handle di dispositivo.
4.  Negoziare una nuova configurazione del decodificatore, come descritto nella sezione [ricerca di una configurazione del decodificatore](#finding-a-decoder-configuration).
5.  Creare un nuovo dispositivo di decodificatore.

Supponendo che l'handle del dispositivo sia valido, il processo di decodifica funziona nel modo seguente:

1.  Chiamare [**IDirectXVideoDecoder:: BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
2.  Eseguire le operazioni seguenti una o più volte:
    1.  Chiamare [**IDirectXVideoDecoder:: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) per ottenere un buffer del decodificatore DXVA.
    2.  Riempire il buffer.
    3.  Chiamare [**IDirectXVideoDecoder:: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
3.  Chiamare [**IDirectXVideoDecoder:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) per eseguire le operazioni di decodifica sul frame.

DXVA 2,0 usa le stesse strutture di dati di DXVA 1,0 per le operazioni di decodifica. Per il set originale di profili DXVA (per H. 261, H. 263 e MPEG-2), queste strutture di dati sono descritte nella [specifica DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

All'interno di ogni [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)coppia di chiamate di / [**esecuzione**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) BeginFrame, è possibile chiamare più volte [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) , ma solo una volta per ogni tipo di buffer DXVA. Se viene chiamato due volte con lo stesso tipo di buffer, i dati vengono sovrascritti.

Dopo la chiamata a [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), chiamare [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) per recapitare il frame al renderer video, come per la decodifica del software. Il metodo **Receive** è asincrono. una volta restituito, il decodificatore può continuare a decodificare il frame successivo. Il driver di visualizzazione impedisce a tutti i comandi di decodifica di sovrascrivere il buffer mentre il buffer è in uso. Il decodificatore non deve riutilizzare una superficie per decodificare un altro frame finché il renderer non ha rilasciato l'esempio. Quando il renderer rilascia l'esempio, l'allocatore riporta l'esempio al relativo pool di esempi disponibili. Per ottenere il successivo esempio disponibile, chiamare [**CBaseOutputPin:: GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), che a sua volta chiama [**IMemAllocator:: GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer). Per ulteriori informazioni, vedere l'argomento [Cenni preliminari sul flusso di dati in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) nella documentazione di DirectShow.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accelerazione video DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
