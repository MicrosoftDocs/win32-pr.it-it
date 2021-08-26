---
title: Catene di scambio
description: Le catene di scambio controllano la rotazione del buffer nascosto, formando la base dell'animazione grafica.
ms.assetid: AABF5FDE-DB49-4B29-BC0E-032E0C7DF9EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e98fc2baf63d7d80fefc190f2d01da33ea24d420e647b4f0c57df7ec4c501f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850651"
---
# <a name="swap-chains"></a>Catene di scambio

Le catene di scambio controllano la rotazione del buffer nascosto, formando la base dell'animazione grafica.

## <a name="overview"></a>Panoramica

Il modello di programmazione per le catene di scambio in Direct3D 12 non è identico a quello delle versioni precedenti di D3D. La praticità di programmazione, ad esempio, del supporto della rotazione automatica delle risorse presente in D3D10 e D3D11 non è ora supportata. La rotazione automatica delle risorse consente alle app di eseguire il rendering dello stesso oggetto API mentre la superficie effettiva di cui viene eseguito il rendering modifica ogni fotogramma. Il comportamento delle catene di scambio viene modificato con Direct3D 12 per consentire ad altre funzionalità di Direct3D 12 di avere un basso sovraccarico della CPU. La chiave di colore automatica e il multicampionamento non sono supportati, anche se lo sono ancora in particolare l'estensione e la rotazione.

### <a name="buffer-lifetime"></a>Durata del buffer

Alle app è consentito archiviare descrittori creati in precedenza che fanno riferimento a buffer nascosto Questa funzionalità è abilitata assicurando che il set di buffer di proprietà di una catena di scambio non cambi mai per la durata della catena di scambio. Il set di buffer restituito da [**IDXGISwapChain::GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) non cambia fino a quando non vengono chiamate determinate API:

-   [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)
-   [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers)

L'ordine dei buffer restituiti [**da GetBuffer non**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) cambia mai.

[**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) restituisce l'indice del buffer nascosto corrente all'app.

### <a name="swap-effects"></a>Effetti di scambio

Gli unici effetti di scambio supportati [**sono DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) e [**DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect), che richiede che il numero di buffer sia maggiore di uno.

### <a name="transitioning-between-windowed-and-full-screen-modes"></a>Transizione tra modalità a finestra e a schermo intero

Direct3D 12 non supporta la modalità esclusiva a schermo intero (FSE). Quando invece un gioco è l'unica applicazione visibile sullo schermo, il sistema operativo usa una strategia denominata ottimizzazione a schermo intero (FSO) per ottenere un effetto simile a FSE senza gli svantaggi delle prestazioni. Per altre informazioni su FSO, vedere [Demystifying Fullscreen Optimisations](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/).

Direct3D 12 mantiene la restrizione che le applicazioni devono chiamare [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) dopo la transizione tra le modalità a finestra e a schermo intero (le catene di scambio del modello flip D3D11 hanno le stesse restrizioni).

Le [**transizioni IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) non modificano il set di buffer visibili all'app nella catena di scambio. Solo le [**chiamate ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) [**e ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) creano o eliminano i buffer visibili all'app. Tuttavia, in Direct3D 12 [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) non entra nella modalità esclusiva a schermo intero e modifica semplicemente le risoluzioni e le frequenze di aggiornamento per consentire le ottimizzazioni a schermo intero. Queste modifiche possono essere apportate da un'app senza l'uso di questo metodo

Quando o viene chiamato [**IDXGISwapChain::P resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) o [**IDXGISwapChain1::P resent,**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) il buffer nascosto da presentare deve essere nello stato [**D3D12 \_ RESOURCE STATE \_ \_ PRESENT.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) Present avrà esito negativo **con ERRORE DXGI \_ CHIAMATA NON \_ \_ VALIDA** se non è così.

Le catene di scambio a schermo intero continuano ad avere la restrizione per cui è necessario chiamare [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)(FALSE, NULL) prima del rilascio finale della catena di scambio. **SetFullscreenState**(FALSE) ha esito positivo nelle catene di scambio in esecuzione nei dispositivi Direct3D 12.

Le operazioni presenti si verificano nella coda 3D fornita durante la creazione dello swapchain e le app possono presentare contemporaneamente più catene di scambio e registrare ed eseguire elenchi di comandi.

Quando la parte finale del lavoro grafico (ad esempio, la post-elaborazione dei frame) viene eseguita in una coda di calcolo o non comporta la coda grafica del dispositivo, la creazione di una seconda coda 3D per la presentazione può essere utile e impedire la latenza di presentazione ritardando l'inizio del frame successivo. 

### <a name="example"></a>Esempio

Il codice di esempio seguente sarebbe presente nel ciclo di rendering principale:

```cpp
void Present()
{
    m_swapChain->Present(0, m_presentFlags);
    m_backBufferIndex = (m_backBufferIndex + 1) % m_backBufferCount;
}
```

### <a name="creating-swap-chains"></a>Creazione di catene di scambio

Quando si usano le chiamate [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)o [**CreateSwapChainForComposition,**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) si noti che il *parametro pDevice* richiede effettivamente un puntatore a una coda di comandi diretta in Direct3D 12 e non a un dispositivo.

### <a name="presenting-on-windows-7"></a>Presentazione in Windows 7

Quando la destinazione è Direct3D 12 in Windows 7, i tipi DXGI necessari per Direct3D 12 non sono presenti, quindi è necessario usare **l'ID3D12On7 fornito da D3D12CommandQueueDownLevel** (sottoposto a query dalla coda di comandi diretta) per presentare.

Si fornisce un elenco di comandi aperti al metodo Windows 7, che verrà quindi usato, chiuso e inviato automaticamente al dispositivo. È necessario fornire un buffer nascosto che deve essere creato dall'app, deve essere una risorsa di cui è stato eseguito il commit, deve essere a campionamento singolo e deve essere uno dei formati seguenti.

* **DXGI_FORMAT_R16G16B16A16_FLOAT**
* **DXGI_FORMAT_R10G10B10A2_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB**
* **DXGI_FORMAT_B8G8R8X8_UNORM**
* **DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM_SRGB**

## <a name="related-topics"></a>Argomenti correlati

* [D3D12_HEAP_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)
* [Esercitazioni video sull'apprendimento avanzato di DirectX: Framerate non limitato](https://www.youtube.com/watch?v=wn02zCXa9IU)
* [Rendering](rendering.md)
