---
title: Aggiornamento della piattaforma per Windows 7
description: Questo argomento descrive i miglioramenti apportati ai componenti dello stack di grafica Windows 7 che diventano disponibili tramite l'aggiornamento della piattaforma per Windows 7.
ms.assetid: C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a577d74613a22a176c038b6c85e53b94f413edbc49d07a886a613ddff5a83b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627581"
---
# <a name="platform-update-for-windows-7"></a>Aggiornamento della piattaforma per Windows 7

Questo argomento descrive i miglioramenti apportati ai componenti dello stack di grafica Windows 7 che diventano disponibili tramite l'aggiornamento della piattaforma [per Windows 7](https://support.microsoft.com/kb/2670838).

Se installato in Windows 7, l'aggiornamento della piattaforma per Windows 7 Windows 7 con funzionalità disponibili in Windows 8. Ad esempio, questi componenti Windows 8 diventano disponibili con funzionalità complete:

-   Direct2D 1.1 (inclusi gli effetti Direct2D)
-   DirectWrite
-   Windows Imaging Component (WIC)

Questi forniscono funzionalità parziali:

-   Direct3D 11.1
-   DXGI 1.2

E, ad esempio, questo componente non è disponibile:

-   DirectComposition (DComp)

Per informazioni su Direct2D, DirectWrite e WIC con l'aggiornamento della piattaforma, vedere questi argomenti:

-   [Novità di Direct2D per Windows 8 (Windows)](/windows/desktop/Direct2D/what-s-new-in-direct2d-for-windows-8-consumer-preview)
-   [Novità di DirectWrite per Windows 8 (Windows)](/windows/desktop/DirectWrite/what-s-new-in-directwrite-for-windows-8-consumer-preview)
-   [Novità di WIC in Windows 8 (Windows)](/previous-versions//hh994467(v=vs.85))

Per informazioni su Direct3D e DXGI con l'aggiornamento della piattaforma, vedere questi argomenti:

-   [Funzionalità D3D11.1](/windows/desktop/direct3d11/direct3d-11-1-features)
-   [Miglioramenti di DXGI 1.2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

Dopo l'installazione dell'aggiornamento della piattaforma, le interfacce introdotte in Direct3D11.1 e DXGI 1.2 saranno disponibili con funzionalità parziali. Le funzionalità di questi componenti grafici sono legate direttamente ai componenti del kernel di grafica, ai driver di grafica e all'hardware grafico. Prima di usare Direct3D11.1 in Windows 7, acquisire familiarità con queste specifiche:

-   Windows 8 introdotto il modello di driver WDDM 1.2, che ha fornito miglioramenti nella superficie API associata per tutti i [livelli di funzionalità.](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Quando si legge la documentazione di Direct3D11.1, comprendere che i *nuovi driver* significano driver WDDM 1.2. Queste versioni aggiornate dei driver, nonché la maggior parte delle funzionalità facoltative esposte tramite [**CheckFeatureSupport,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport)non sono disponibili Windows 7. Poiché non vi è alcuna garanzia che queste funzionalità facoltative siano disponibili, assicurarsi che le applicazioni presentino comportamenti di fallback appropriati nel caso in cui la funzionalità desiderata non sia disponibile.

    Esiste un'eccezione importante. Diverse funzionalità, ad esempio [**PSSetConstantBuffers1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1) con offset di [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) buffer costanti, richiedono nuovi driver per il livello di funzionalità 10 e versioni successive, ma sono effettivamente emulate per il livello di funzionalità 9. Questa emulazione è disponibile in Windows 7 con l'aggiornamento della piattaforma. Vedere [**D3D11 \_ FEATURE DATA \_ \_ D3D11 OPTIONS (OPZIONI D3D11 \_ FEATURE DATA D3D11)**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) per altre informazioni sulle funzionalità emulate.

-   Il Windows 8 di driver WDDM 1.2 supporta una nuova generazione di hardware, esposto tramite la funzionalità D3D [livello](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.1. Windows 7 con l'aggiornamento della piattaforma supporta solo il modello di driver WDDM 1.1 e pertanto il supporto hardware del livello di funzionalità 11.1 non è disponibile (tramite l'aggiornamento della piattaforma). In Windows 7 con l'aggiornamento della [**piattaforma, D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) restituisce sempre un livello di funzionalità 11.0 o inferiore, ad eccezione di un dispositivo di riferimento che può essere usato per testare un percorso di codice 11.1 in Windows 7. Usare solo le funzionalità disponibili ai livelli di funzionalità di destinazione, come descritto nel riferimento a livello di funzionalità.
-   Alcuni nuovi metodi introdotti in DGXI 1.2 non sono completamente supportati con l'aggiornamento della piattaforma per Windows 7. È possibile testare la disponibilità di queste funzioni chiamandole direttamente e verificando la presenza di un codice di errore. Assicurarsi che le applicazioni di destinazione Windows 7 con l'aggiornamento della piattaforma presentino un fallback quando la funzionalità desiderata non è disponibile. Queste classi di funzionalità non sono disponibili in Platform Update per Windows 7:

    -   Stereo
    -   Swapchain che non hanno come destinazione Hwnd
    -   Notifiche sullo stato di occlusione
    -   Duplicazione del desktop
    -   NT Gestisce le risorse

    In particolare, le API seguenti restituiranno DXGI \_ ERROR \_ UNSUPPORTED, DXGI \_ ERROR INVALID \_ \_ CALL, E \_ NOTIMPL o E \_ INVALIDARG:

    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterStereoStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterOcclusionStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**DuplicateOutput**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**EnqueueSetEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
    -   [**IDXGIResource1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1)::[**CreateSharedHandle**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**GetSharedResourceAdapterLuid**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResource1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResourceByName**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)

-   Queste API hanno differenze di comportamento, come illustrato di seguito:
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) accetta una struttura [**DXGI \_ SWAP CHAIN \_ \_ DESC1,**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) che include un campo per **il ridimensionamento**. [**DXGI \_ SCALING \_ NONE**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling) non è supportato in Windows 7 con l'aggiornamento della piattaforma e fa in modo che **CreateSwapChainForHwnd** restituirà DXGI ERROR INVALID CALL quando \_ viene \_ \_ chiamato.
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetBackgroundColor**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) è utile solo se impostato in un swapchain usando DXGI \_ SCALING \_ NONE. Il valore è ancora archiviato e può essere recuperato, ma non ha alcun effetto.
    -   [**IDXGIDisplayControl**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol)::[**IsStereoEnabled,**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled) [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**IsWindowedStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)e [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**IsTemporaryMonoSupported**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported) restituisce **TUTTI FALSE.**
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**GetDisplayModeList1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) e **IDXGIOutput1**::[**FindClosestMatchingMode1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1) sono stati aggiunti per facilitare le modalità di visualizzazione stereo. Stereo non è supportato in Platform Update per Windows 7, quindi questo metodo equivale a [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput)::[**FindClosestMatchingMode**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode) come [**DXGI \_ MODE \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1). Stereo sarà sempre FALSE.
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) e **IDXGIDevice2**::[**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) non sono supportati in Platform Update per Windows 7. Tuttavia, il runtime consente comunque di chiamarli ed esegue la convalida che vengono usati correttamente nelle risorse non condivise.
    -   [I dispositivi WARP](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) supportano [solo il livello di](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) funzionalità 11.0. Ciò significa che i dispositivi WARP creati passando [D3D \_ DRIVER \_ TYPE \_ WARP](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type) nel parametro *DriverType* [**di D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) non supportano la versione 11.1 né supportano superfici condivise.
-   Per gli sviluppatori che attualmente usano applicazioni in Microsoft Visual Studio 2010 o versioni precedenti usando il flag [**D3D11 \_ CREATE \_ DEVICE \_ DEBUG,**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag) tenere presente che le chiamate a [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) avranno esito negativo. Questo perché il runtime D3D11.1 richiede ora D3D111SDKLayers.dll invece di \_ D3D11SDKLayers.dll. Per ottenere questa nuova DLL (D3D111SDKLayers.dll), installare Windows 8 \_ [SDK](https://dev.windows.com/downloads/windows-8-sdk)o [Visual Studio 2012](https://www.microsoft.com/visualstudio/eng/downloads)o gli strumenti di debug remoto Visual Studio 2012. Per altre [informazioni, vedere](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) la documentazione del livello di debug.

 

 