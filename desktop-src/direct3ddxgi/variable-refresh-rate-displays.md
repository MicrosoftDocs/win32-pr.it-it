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
# <a name="variable-refresh-rate-displays"></a>Visualizzazione frequenza di aggiornamento variabili

Le visualizzazioni della frequenza di aggiornamento variabili richiedono l'abilitazione dello *strappo* , noto anche come supporto "VSync".

-   [Frequenza di aggiornamento variabile Visualizza/vsync off](#variable-refresh-rate-displaysvsync-off)
-   [Argomenti correlati](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a>Frequenza di aggiornamento variabile Visualizza/vsync off

Il supporto per la frequenza di aggiornamento delle variabili viene visualizzato impostando determinati flag durante la creazione e la presentazione della catena di scambio.

Per usare questa funzionalità, gli utenti dell'app devono trovarsi nei sistemi Windows 10 con [KB3156421](https://support.microsoft.com/kb/3156421) o con l'aggiornamento dell'anniversario installato. La funzionalità funziona in tutte le versioni di Direct3D 11 e 12 usando gli effetti di swap **DXGI \_ swap \_ Effect \_ Flip \_ \** _.

Per aggiungere il supporto VSYNC alle app, è possibile fare riferimento a un esempio di esecuzione completa per Direct3D 12, _ *D3D12Fullscreen** (vedere gli [esempi funzionanti](../direct3d12/working-samples.md)). Ci sono anche alcuni punti non esplicitamente denominati nel codice di esempio, ma è necessario prestare attenzione a.

-   [**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (o [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) deve avere lo stesso flag di creazione della catena di scambio (il \_ flag della \_ catena di scambio DXGI consente lo \_ \_ \_ strappo) passato come [**presente**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (o [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).
-   DXGI \_ present \_ Consenti \_ strappo può essere usato solo con l'intervallo di sincronizzazione 0. È consigliabile passare sempre questo flag di strappo quando si usa l'intervallo di sincronizzazione 0 se [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) segnala che lo strappo è supportato *e* l'app è in modalità a finestra, inclusa la modalità a schermo intero senza bordo. Per altri dettagli, vedere le costanti [**\_ presenti in DXGI**](dxgi-present.md) .
-   La disabilitazione di vsync non stappare necessariamente la frequenza dei fotogrammi: gli sviluppatori devono anche assicurarsi che le chiamate [**presenti**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) non siano limitate da altri eventi temporali, ad esempio l' `CompositionTarget::Rendering` evento in un'app basata su XAML.

Il codice seguente riassume alcuni elementi chiave che è necessario aggiungere alle app.

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramenti di DXGI 1,5](dxgi-1-5-improvements.md)
</dt> <dt>

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
