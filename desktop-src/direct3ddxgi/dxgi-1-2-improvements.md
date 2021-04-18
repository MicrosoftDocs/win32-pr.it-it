---
description: In Microsoft DirectX Graphics Infrastructure (DXGI) 1,2 sono state aggiunte le funzionalità seguenti.
ms.assetid: E2D8DA99-4EA2-4847-B699-80A6994C66C0
title: Miglioramenti di DXGI 1.2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd274918d179bc7adeb8dd132fe604cf56d80f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303788"
---
# <a name="dxgi-12-improvements"></a>Miglioramenti di DXGI 1.2

In Microsoft DirectX Graphics Infrastructure (DXGI) 1,2 sono state aggiunte le funzionalità seguenti.

## <a name="presentation-enhancements-and-optimizations"></a>Miglioramenti e ottimizzazioni della presentazione

DXGI 1,2 migliora la presentazione con una nuova catena di scambio del modello Flip, protezione del contenuto, presentazione senza finestra e una presentazione ottimizzata in cui è possibile specificare rettangoli Dirty e aree a scorrimento. La presentazione è inoltre migliorata con il comportamento di visualizzazione stereoscopica 3D.

È possibile usare l'API DXGI 1,2 seguente per la presentazione avanzata.

-   [**IDXGIDisplayControl::IsStereoEnabled**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled)
-   [**IDXGIDisplayControl::SetStereoEnabled**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-setstereoenabled)
-   [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)
-   [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
-   [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
-   [**IDXGIFactory2::IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)
-   [**IDXGIFactory2::RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
-   [**IDXGIFactory2::RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
-   [**IDXGIFactory2::UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
-   [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
-   [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
-   [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
-   [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1)
-   [**IDXGIOutput1::GetDisplaySurfaceData1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1)
-   [**IDXGIOutput1::FindClosestMatchingMode1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1)
-   [**IDXGIResource1::CreateSubresourceSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsubresourcesurface)
-   [**IDXGISurface2:: GetResource**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgisurface2-getresource)
-   [**IDXGISwapChain1::GetDesc1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1)
-   [**IDXGISwapChain1::GetFullscreenDesc**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getfullscreendesc)
-   [**IDXGISwapChain1:: GetHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-gethwnd)
-   [**IDXGISwapChain1::GetCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
-   [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**IDXGISwapChain1::IsTemporaryMonoSupported**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported)
-   [**IDXGISwapChain1::GetRestrictToOutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrestricttooutput)
-   [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)
-   [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)
-   [**IDXGISwapChain1:: serotation**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
-   [**IDXGISwapChain1:: getrotation**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)

Per altre informazioni su come usare l'API DXGI 1,2 per una presentazione avanzata, vedere [migliorare la presentazione con il modello Flip, i rettangoli Dirty e le aree a scorrimento](dxgi-1-2-presentation-improvements.md).

Per informazioni su come determinare se è possibile eseguire il rendering in stereo, vedere [rendering in stereo e notifica sullo stato stereo](stereo-rendering-stereo-status-notifying.md).

Per informazioni su come determinare le modifiche nello stato di occlusione dell'app, vedere [attesa di un evento quando il rendering non è necessario](waiting-when-occluded.md).

Per informazioni sul modo in cui i valori dei dati cambiano quando si presenta il contenuto sullo schermo, vedere [conversione dei dati per lo spazio colore](converting-data-color-space.md).

## <a name="desktop-duplication"></a>Duplicazione del desktop

Windows 8 Disabilita i driver mirror standard di Windows 2000 Display Driver Model (XDDM). DXGI 1,2 fornisce l'API per la duplicazione del desktop come alternativa. L'API di duplicazione desktop fornisce accesso remoto all'immagine desktop per gli scenari di collaborazione.

L'API di duplicazione desktop è costituita dai metodi seguenti.

-   [**IDXGIOutput1::D uplicateOutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
-   [**IDXGIOutputDuplication:: getdesc**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getdesc)
-   [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)
-   [**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects)
-   [**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects)
-   [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape)
-   [**IDXGIOutputDuplication::MapDesktopSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface)
-   [**IDXGIOutputDuplication::UnMapDesktopSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-unmapdesktopsurface)
-   [**IDXGIOutputDuplication::ReleaseFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-releaseframe)

Per ulteriori informazioni sull'utilizzo dell'API di duplicazione desktop, vedere [API di duplicazione desktop](desktop-dup-api.md).

## <a name="improved-usage-of-shared-resources-and-synchronized-events"></a>Miglioramento dell'utilizzo delle risorse condivise e degli eventi sincronizzati

Nelle versioni precedenti di Windows, le app usano il polling continuo per determinare se l'unità di elaborazione grafica (GPU) ha terminato l'elaborazione dei comandi arbitrari. DXGI 1,2 consente a un'app di accodare un evento a un dispositivo DXGI. L'app può quindi attendere che il dispositivo DXGI segnali l'evento per determinare che la GPU ha terminato l'esecuzione di tutti i comandi di rendering. DXGI 1,2 consente a più dispositivi di condividere una risorsa tramite un handle NT.

Per condividere le risorse e sincronizzare gli eventi, è possibile usare la seguente API DXGI 1,2 e l'API Direct3D 11,1.

-   [**IDXGIDevice2::EnqueueSetEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
-   [**IDXGIResource1::CreateSharedHandle**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
-   [**IDXGIFactory2::GetSharedResourceAdapterLuid**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
-   [**ID3D11Device1::OpenSharedResource1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
-   [**ID3D11Device1::OpenSharedResourceByName**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)
-   [**D3D11 \_ risorse \_ varie \_ \_ NTHANDLE condivise**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="offer-the-video-memory-of-resources"></a>Offrire la memoria video delle risorse

DXGI 1,2 consente a un'app di offrire la memoria video delle risorse con un sovraccarico ridotto. Grazie alla memoria video, il sistema operativo può liberare la memoria del video.

Questa funzionalità DXGI 1,2 è costituita dai metodi seguenti.

-   [**IDXGIDevice2::OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources)
-   [**IDXGIDevice2::ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources)

È possibile usare il metodo [**ID3D11Debug:: SetFeatureMask**](/windows/win32/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask) per impostare i flag della maschera di funzionalità che consentono di eseguire il debug del comportamento dei metodi [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) e [**IDXGIDevice2:: ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) nell'app.

## <a name="gpu-preemption-at-finer-granularity-levels-for-wddm-12-driver-model"></a>Precedenza GPU a livelli di granularità più fini per il modello di driver WDDM 1,2

A partire dal modello di driver Windows Display Driver Model (WDDM) 1,2, l'utilità di pianificazione WDDM può intercedere l'esecuzione delle attività dell'applicazione della GPU a livelli di granularità più fini. DXGI 1,2 consente di determinare i livelli di granularità di precedenza della GPU.

Questa funzionalità DXGI 1,2 è costituita dal seguente metodo.

-   [**IDXGIAdapter2::GetDesc2**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiadapter2-getdesc2)

## <a name="debugging-apis"></a>API di debug

Windows 8 SDK fornisce funzionalità di debug aggiuntive. È possibile usare le API DXGI seguenti da Dxgidebug.dll per eseguire il debug dell'app:

-   [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)
-   [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug)
-   [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue)

Per accedere a [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface), chiamare la funzione [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per ottenere Dxgidebug.dll e la funzione [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere l'indirizzo di **DXGIGetDebugInterface**. È quindi possibile chiamare **DXGIGetDebugInterface** per ottenere l'interfaccia [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug) o [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) .

Per informazioni su come eseguire il debug di app DirectX in modalità remota, vedere [debug di app DirectX in modalità remota](../direct3dtools/debugging-directx-apps-remotely.md).

## <a name="related-topics"></a>Argomenti correlati

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
