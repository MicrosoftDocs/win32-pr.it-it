---
description: Le frequenze di aggiornamento variabili richiedono che sia abilitato lo tearing, noto anche come &\# 0034;vsync-off&\# 0034; supporto.
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: Visualizzazione della frequenza di aggiornamento variabile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349592ce49d1008f6337b53c7f524ac7303907f75cd99205fe79bf55988b934b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288924"
---
# <a name="variable-refresh-rate-displays"></a>Visualizzazione della frequenza di aggiornamento variabile

Le frequenze di aggiornamento variabili richiedono che sia abilitato lo *tearing.* Questo supporto è noto anche come "vsync-off".

-   [Visualizzazione frequenza di aggiornamento variabile/Vsync disattivata](#variable-refresh-rate-displaysvsync-off)
-   [Argomenti correlati](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a>Visualizzazione frequenza di aggiornamento variabile/Vsync disattivata

Il supporto per la frequenza di aggiornamento variabile viene ottenuto impostando determinati flag durante la creazione e la presentazione della catena di scambio.

Per usare questa funzionalità, gli utenti dell'app devono Windows 10 sistemi con [KB3156421](https://support.microsoft.com/kb/3156421) o l'aggiornamento dell'anniversario installato. La funzionalità funziona in tutte le versioni di Direct3D 11 e 12 usando gli effetti di swap **swap DXGI \_ SWAP EFFECT \_ \_ FLIP. \_ \***

Per aggiungere il supporto vsync-off alle app, è possibile fare riferimento a un esempio completo per Direct3D 12, **D3D12Fullscreen** (vedere Esempi [di lavoro).](../direct3d12/working-samples.md) Esistono anche alcuni punti non esplicitamente definiti nel codice di esempio, ma è necessario prestare attenzione.

-   [**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (o [**ResizeBuffers1)**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)deve avere lo stesso flag di creazione della catena di scambio (DXGI SWAP CHAIN FLAG ALLOW TEARING) passato come \_ \_ \_ \_ \_ [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (o [**Present1).**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   DXGI PRESENT ALLOW TEARING può essere \_ usato solo con \_ \_ l'intervallo di sincronizzazione 0. È consigliabile passare sempre questo flag di tearing quando si usa l'intervallo di  sincronizzazione 0 se [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) segnala che lo tearing è supportato e l'app è in modalità a finestre, inclusa la modalità a schermo intero senza bordo. Per altri dettagli, vedere le [**costanti DXGI \_ PRESENT.**](dxgi-present.md)
-   La disabilitazione di vsync non annulla necessariamente la frequenza dei fotogrammi: gli sviluppatori devono anche assicurarsi che le chiamate Present non siano limitate da altri eventi di temporizzazione (ad esempio l'evento in un'app basata su [](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) `CompositionTarget::Rendering` XAML).

Il codice seguente ricava alcune parti chiave che è necessario aggiungere alle app.

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

[Miglioramenti di DXGI 1.5](dxgi-1-5-improvements.md)
</dt> <dt>

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
