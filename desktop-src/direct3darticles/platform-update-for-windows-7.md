---
title: Aggiornamento della piattaforma per Windows 7
description: Questo argomento descrive i miglioramenti apportati ai componenti dello stack di grafica di Windows 7 che diventano disponibili tramite l'aggiornamento della piattaforma per Windows 7.
ms.assetid: C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fd1e6e2681673d2bb2bab7a4a6de42f77988eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872858"
---
# <a name="platform-update-for-windows-7"></a>Aggiornamento della piattaforma per Windows 7

Questo argomento descrive i miglioramenti apportati ai componenti dello stack di grafica di Windows 7 che diventano disponibili tramite l' [aggiornamento della piattaforma per Windows 7](https://support.microsoft.com/kb/2670838).

Se installato in Windows 7, l'aggiornamento della piattaforma per Windows 7 Aggiorna Windows 7 con le funzionalità disponibili in Windows 8. Questi componenti di Windows 8, ad esempio, diventano disponibili con funzionalità complete:

-   Direct2D 1,1 (inclusi gli effetti Direct2D)
-   DirectWrite
-   Windows Imaging Component (WIC)

Che forniscono funzionalità parziali:

-   Direct3D 11,1
-   DXGI 1,2

E, ad esempio, questo componente non è disponibile:

-   DirectComposition (DComp)

Per informazioni su Direct2D, DirectWrite e WIC con l'aggiornamento della piattaforma, vedere gli argomenti seguenti:

-   [Novità di Direct2D per Windows 8 (Windows)](/windows/desktop/Direct2D/what-s-new-in-direct2d-for-windows-8-consumer-preview)
-   [Novità di DirectWrite per Windows 8 (Windows)](/windows/desktop/DirectWrite/what-s-new-in-directwrite-for-windows-8-consumer-preview)
-   [Novità di WIC in Windows 8 (Windows)](/previous-versions//hh994467(v=vs.85))

Per informazioni su Direct3D e DXGI con l'aggiornamento della piattaforma, vedere gli argomenti seguenti:

-   [Funzionalità di D3D 11.1](/windows/desktop/direct3d11/direct3d-11-1-features)
-   [Miglioramenti di DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

Dopo l'installazione dell'aggiornamento della piattaforma, le interfacce introdotte in Direct3D 11.1 e DXGI 1,2 saranno disponibili con funzionalità parziali. Le funzionalità di questi componenti grafici sono legate direttamente ai componenti del kernel grafico, ai driver grafici e all'hardware grafico. Prima di usare Direct3D 11.1 in Windows 7, acquisire familiarità con queste specifiche:

-   In Windows 8 è stato introdotto il modello di driver WDDM 1,2, che fornisce miglioramenti nella superficie dell'API associata per tutti i [livelli di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro). Quando si legge la documentazione di Direct3D 11.1, comprendere che i *nuovi driver* significano driver WDDM 1,2. Queste versioni di driver aggiornate, nonché la maggior parte delle funzionalità facoltative esposte tramite [**CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport), non sono disponibili in Windows 7. Poiché non vi è alcuna garanzia che queste funzionalità opzionali siano disponibili, assicurarsi che le applicazioni abbiano comportamenti di fallback appropriati nel caso in cui la funzionalità desiderata non sia disponibile.

    Esiste un'eccezione importante. Diverse funzionalità, ad esempio [**PSSetConstantBuffers1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1) con offset del buffer costanti, richiedono nuovi driver per il [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10 e versioni successive, ma vengono effettivamente emulati per il livello di funzionalità 9. Questa emulazione è disponibile in Windows 7 con l'aggiornamento della piattaforma. Per altre informazioni sulle funzionalità da emulare, vedere [**\_ \_ \_ \_ Opzioni di d3d11 dei dati della funzionalità d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .

-   Il modello di driver Windows 8 WDDM 1,2 supporta una nuova generazione di hardware, esposto tramite il [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) D3D 11,1. Windows 7 con l'aggiornamento della piattaforma supporta solo il modello di driver WDDM 1,1 e pertanto il supporto hardware del livello di funzionalità 11,1 non è disponibile (tramite l'aggiornamento della piattaforma). In Windows 7 con l'aggiornamento della piattaforma, [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) restituisce sempre un livello di funzionalità di 11,0 o inferiore, ad eccezione di con un dispositivo di riferimento che può essere usato per testare un percorso di codice 11,1 in Windows 7. Usare solo le funzionalità disponibili ai livelli di funzionalità di destinazione, come descritto nel riferimento a livello di funzionalità.
-   Alcuni nuovi metodi introdotti in DGXI 1,2 non sono completamente supportati con l'aggiornamento della piattaforma per Windows 7. è possibile verificare la disponibilità di queste funzioni chiamandole direttamente e verificando la presenza di un codice di errore. Verificare che le applicazioni destinate a Windows 7 con l'aggiornamento della piattaforma dispongano di un fallback quando la funzionalità desiderata non è disponibile. Queste classi di funzionalità non sono disponibili per l'aggiornamento della piattaforma per Windows 7:

    -   Stereo
    -   Le catene non destinati a HWND
    -   Notifiche di stato occlusione
    -   Duplicazione del desktop
    -   Risorse di gestione NT

    In particolare, le API seguenti restituiranno un \_ errore DXGI \_ non supportato, una \_ chiamata DXGI \_ non valida \_ , e \_ NOTIMPL o e \_ INVALIDARG:

    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterStereoStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterOcclusionStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**serotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**getrotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**DuplicateOutput**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**EnqueueSetEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
    -   [**IDXGIResource1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1)::[**CreateSharedHandle**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**GetSharedResourceAdapterLuid**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResource1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResourceByName**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)

-   Queste API presentano differenze di comportamento, come indicato di seguito:
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) accetta una struttura a [**\_ \_ catena \_ di scambio DXGI**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) che dispone di un campo per la **scalabilità**. [**DXGI \_ Il RIDIMENSIONAmento di \_ None**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling) non è supportato in Windows 7 con l'aggiornamento della piattaforma e fa in modo che **CreateSwapChainForHwnd** restituisca una \_ \_ chiamata non valida DXGI Error quando viene \_ chiamato.
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetBackgroundColor**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) è utile solo quando viene impostato su un presentazione catena usando DXGI \_ Scalable \_ None. Il relativo valore è ancora archiviato e può essere recuperato, ma non ha alcun effetto.
    -   [**IDXGIDisplayControl**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol)::[**IsStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled), [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**IsWindowedStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)e [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**IsTemporaryMonoSupported**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported) restituiscono **false**.
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**GetDisplayModeList1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) e **IDXGIOutput1**::[**FindClosestMatchingMode1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1) sono stati aggiunti per semplificare le modalità di visualizzazione stereo. Stereo non è supportato nell'aggiornamento della piattaforma per Windows 7, pertanto questo metodo è equivalente a [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput)::[**FindClosestMatchingMode**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode) As [**DXGI \_ mode \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1). Lo stereo sarà sempre FALSE.
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) e **IDXGIDevice2**::[**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) non sono supportati nell'aggiornamento della piattaforma per Windows 7. Tuttavia, il runtime ne consente la chiamata ed esegue la convalida in modo che vengano usate correttamente su risorse non condivise.
    -   I dispositivi [Warp](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) supportano solo il [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0. Ovvero i dispositivi WARP creati passando il [tipo di \_ driver \_ D3D \_ Warp](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type) nel parametro *DriverType* di [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) non supportano 11,1 né supportano le aree condivise.
-   Per gli sviluppatori che attualmente lavorano sulle applicazioni in Microsoft Visual Studio 2010 o versioni precedenti usando il flag di debug per la [**\_ creazione di \_ dispositivi \_ d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag) , tenere presente che le chiamate a [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) avranno esito negativo. Questo perché il runtime D3D 11.1 richiede ora D3D11 \_1SDKLayers.dll anziché D3D11SDKLayers.dll. Per ottenere questa nuova DLL (D3D11 \_1SDKLayers.dll), installare [Windows 8 SDK](https://dev.windows.com/downloads/windows-8-sdk)o [Visual Studio 2012](https://www.microsoft.com/visualstudio/eng/downloads)o Visual Studio 2012 Remote Debugging Tools. Per ulteriori informazioni, vedere la documentazione relativa al [livello di debug](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) .

 

 