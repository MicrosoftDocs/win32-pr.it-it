---
description: Le visualizzazioni della frequenza di aggiornamento variabili richiedono l'abilitazione dello strappo, anche noto come &\# 0034; vsync-off&\# 0034; supporto.
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: Visualizzazione frequenza di aggiornamento variabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6e658d84c51a6b51bc32855226194b9c22507e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225372"
---
# <a name="variable-refresh-rate-displays"></a><span data-ttu-id="fee80-103">Visualizzazione frequenza di aggiornamento variabili</span><span class="sxs-lookup"><span data-stu-id="fee80-103">Variable refresh rate displays</span></span>

<span data-ttu-id="fee80-104">Le visualizzazioni della frequenza di aggiornamento variabili richiedono l'abilitazione dello *strappo* , noto anche come supporto "VSync".</span><span class="sxs-lookup"><span data-stu-id="fee80-104">Variable refresh rate displays require *tearing* to be enabled, this is also known as "vsync-off" support.</span></span>

-   [<span data-ttu-id="fee80-105">Frequenza di aggiornamento variabile Visualizza/vsync off</span><span class="sxs-lookup"><span data-stu-id="fee80-105">Variable refresh rate displays/Vsync off</span></span>](#variable-refresh-rate-displaysvsync-off)
-   [<span data-ttu-id="fee80-106">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fee80-106">Related topics</span></span>](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a><span data-ttu-id="fee80-107">Frequenza di aggiornamento variabile Visualizza/vsync off</span><span class="sxs-lookup"><span data-stu-id="fee80-107">Variable refresh rate displays/Vsync off</span></span>

<span data-ttu-id="fee80-108">Il supporto per la frequenza di aggiornamento delle variabili viene visualizzato impostando determinati flag durante la creazione e la presentazione della catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="fee80-108">Support for variable refresh rate displays is achieved by setting certain flags when creating and presenting the swap chain.</span></span>

<span data-ttu-id="fee80-109">Per usare questa funzionalità, gli utenti dell'app devono trovarsi nei sistemi Windows 10 con [KB3156421](https://support.microsoft.com/kb/3156421) o con l'aggiornamento dell'anniversario installato.</span><span class="sxs-lookup"><span data-stu-id="fee80-109">To use this feature, app users need to be on Windows 10 systems with either [KB3156421](https://support.microsoft.com/kb/3156421) or the Anniversary Update installed.</span></span> <span data-ttu-id="fee80-110">La funzionalità funziona in tutte le versioni di Direct3D 11 e 12 usando gli effetti di swap \**DXGI \_ swap \_ Effect \_ Flip \_ \** _.</span><span class="sxs-lookup"><span data-stu-id="fee80-110">The feature works on all versions of Direct3D 11 and 12 using \**DXGI\_SWAP\_EFFECT\_FLIP\_\** _ swap effects.</span></span>

<span data-ttu-id="fee80-111">Per aggiungere il supporto VSYNC alle app, è possibile fare riferimento a un esempio di esecuzione completa per Direct3D 12, _ *D3D12Fullscreen*\* (vedere gli [esempi funzionanti](../direct3d12/working-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="fee80-111">To add vsync-off support to your apps, you can refer to a complete running sample for Direct3D 12, _ *D3D12Fullscreen*\* (refer to [Working Samples](../direct3d12/working-samples.md)).</span></span> <span data-ttu-id="fee80-112">Ci sono anche alcuni punti non esplicitamente denominati nel codice di esempio, ma è necessario prestare attenzione a.</span><span class="sxs-lookup"><span data-stu-id="fee80-112">There are also a few points not explicitly called out in the sample code but you need to pay attention to.</span></span>

-   <span data-ttu-id="fee80-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (o [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) deve avere lo stesso flag di creazione della catena di scambio (il \_ flag della \_ catena di scambio DXGI consente lo \_ \_ \_ strappo) passato come [**presente**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (o [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).</span><span class="sxs-lookup"><span data-stu-id="fee80-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (or [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) must have the same swap chain creation flag (DXGI\_SWAP\_CHAIN\_FLAG\_ALLOW\_TEARING) passed to it as [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (or [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).</span></span>
-   <span data-ttu-id="fee80-114">DXGI \_ present \_ Consenti \_ strappo può essere usato solo con l'intervallo di sincronizzazione 0.</span><span class="sxs-lookup"><span data-stu-id="fee80-114">DXGI\_PRESENT\_ALLOW\_TEARING can only be used with sync interval 0.</span></span> <span data-ttu-id="fee80-115">È consigliabile passare sempre questo flag di strappo quando si usa l'intervallo di sincronizzazione 0 se [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) segnala che lo strappo è supportato *e* l'app è in modalità a finestra, inclusa la modalità a schermo intero senza bordo.</span><span class="sxs-lookup"><span data-stu-id="fee80-115">It is recommended to always pass this tearing flag when using sync interval 0 if [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) reports that tearing is supported *and* the app is in a windowed mode - including border-less fullscreen mode.</span></span> <span data-ttu-id="fee80-116">Per altri dettagli, vedere le costanti [**\_ presenti in DXGI**](dxgi-present.md) .</span><span class="sxs-lookup"><span data-stu-id="fee80-116">Refer to the [**DXGI\_PRESENT**](dxgi-present.md) constants for more details.</span></span>
-   <span data-ttu-id="fee80-117">La disabilitazione di vsync non stappare necessariamente la frequenza dei fotogrammi: gli sviluppatori devono anche assicurarsi che le chiamate [**presenti**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) non siano limitate da altri eventi temporali, ad esempio l' `CompositionTarget::Rendering` evento in un'app basata su XAML.</span><span class="sxs-lookup"><span data-stu-id="fee80-117">Disabling vsync does not necessarily uncap your frame rate: developers also need to make sure [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) calls are not throttled by other timing events (such as the `CompositionTarget::Rendering` event in an XAML-based app).</span></span>

<span data-ttu-id="fee80-118">Il codice seguente riassume alcuni elementi chiave che è necessario aggiungere alle app.</span><span class="sxs-lookup"><span data-stu-id="fee80-118">The code below recaps a few key pieces you need to add to your apps.</span></span>

``` syntax
//--------------------------------------------------------------------------------------------------------
// Check Tearing Support
//--------------------------------------------------------------------------------------------------------

// Determines whether tearing support is available for fullscreen borderless windows.

void DXSample::CheckTearingSupport()
{
// Rather than create the 1.5 factory interface directly, we create the 1.4
// interface and query for the 1.5 interface. This will enable the graphics
// debugging tools which might not support the 1.5 factory interface.

    ComPtr<IDXGIFactory4> factory4;
    HRESULT hr = CreateDXGIFactory1(IID_PPV_ARGS(&factory4));
    BOOL allowTearing = FALSE;
    if (SUCCEEDED(hr))
    { 
        ComPtr<IDXGIFactory5> factory5;
        hr = factory4.As(&factory5);
        if (SUCCEEDED(hr))
        {
            hr = factory5->CheckFeatureSupport(DXGI_FEATURE_PRESENT_ALLOW_TEARING, &allowTearing, sizeof(allowTearing));
        }
    }
    m_tearingSupport = SUCCEEDED(hr) && allowTearing;
}

//--------------------------------------------------------------------------------------------------------
// Set up swapchain properly
//--------------------------------------------------------------------------------------------------------

// It is recommended to always use the tearing flag when it is supported.
swapChainDesc.Flags = m_tearingSupport ? DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING : 0;

//--------------------------------------------------------------------------------------------------------
// Present
//--------------------------------------------------------------------------------------------------------

UINT presentFlags = (m_tearingSupport && m_windowedMode) ? DXGI_PRESENT_ALLOW_TEARING : 0;

// Present the frame.
ThrowIfFailed(m_swapChain->Present(0, presentFlags));
```

## <a name="related-topics"></a><span data-ttu-id="fee80-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fee80-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fee80-120">Miglioramenti di DXGI 1,5</span><span class="sxs-lookup"><span data-stu-id="fee80-120">DXGI 1.5 Improvements</span></span>](dxgi-1-5-improvements.md)
</dt> <dt>

[<span data-ttu-id="fee80-121">Guida per programmatori per DXGI</span><span class="sxs-lookup"><span data-stu-id="fee80-121">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
