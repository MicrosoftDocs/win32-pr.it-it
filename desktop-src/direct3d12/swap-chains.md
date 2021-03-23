---
title: Scambia catene
description: Le catene di scambio controllano la rotazione del buffer indietro, formando la base dell'animazione grafica.
ms.assetid: AABF5FDE-DB49-4B29-BC0E-032E0C7DF9EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbc7ec1b62ba620b42bc85c1c1f491ff7ba952d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104548839"
---
# <a name="swap-chains"></a>Scambia catene

Le catene di scambio controllano la rotazione del buffer indietro, formando la base dell'animazione grafica.

## <a name="overview"></a>Panoramica

Il modello di programmazione per le catene di scambio in Direct3D 12 non è identico a quello delle versioni precedenti di D3D. La praticità di programmazione, ad esempio, di supportare la rotazione automatica delle risorse che era presente in D3D10 e D3D11 non è ora supportata. App automatiche con rotazione delle risorse abilitate per il rendering dello stesso oggetto API mentre la superficie effettiva di cui viene eseguito il rendering cambia ogni frame. Il comportamento delle catene di scambio è stato modificato con Direct3D 12 per consentire ad altre funzionalità di Direct3D 12 di avere un sovraccarico della CPU ridotto. La chiave di colore automatica e il campionamento multiplo non sono supportati, anche se in particolare l'allungamento e la rotazione sono ancora.

### <a name="buffer-lifetime"></a>Durata buffer

Le app sono autorizzate a archiviare descrittori creati in precedenza che fanno riferimento a buffer indietro questo è abilitato garantendo che il set di buffer di proprietà di una catena di scambio non cambi mai per la durata della catena di scambio. Il set di buffer restituito da [**IDXGISwapChain:: GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) non cambia fino a quando non vengono chiamate determinate API:

-   [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)
-   [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers)

L'ordine dei buffer restituiti da [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) non viene mai modificato.

[**IDXGISwapChain3:: GetCurrentBackBufferIndex**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) restituisce l'indice del buffer nascosto corrente all'app.

### <a name="swap-effects"></a>Effetti swap

Gli unici effetti di scambio supportati sono [**DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) e [**DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect), che richiede che il conteggio del buffer sia maggiore di uno.

### <a name="transitioning-between-windowed-and-full-screen-modes"></a>Transizione tra modalità a finestra e a schermo intero

Direct3D 12 non supporta la modalità esclusiva a schermo intero (FSE). Al contrario, quando un gioco è l'unica applicazione visibile sullo schermo, il sistema operativo usa una strategia denominata ottimizzazioni a schermo intero (FSO) per ottenere un effetto simile a FSE senza svantaggi delle prestazioni. Per ulteriori informazioni su FSO, vedere [demistificazione di ottimizzazioni a schermo intero](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/).

Direct3D 12 mantiene la restrizione che le applicazioni devono chiamare [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) dopo la transizione tra le modalità a schermo intero e a schermo intero (le catene di scambio d3d11 flip-model hanno le stesse restrizioni).

Le transizioni [**IDXGISwapChain:: SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) non modificano il set di buffer visibili per l'app nella catena di scambio. Solo le chiamate [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) e [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) creano o eliminano i buffer visibili per l'app. Tuttavia, in Direct3D 12 [**IDXGISwapChain:: SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) non entra in modalità esclusiva a schermo intero e modifica semplicemente le risoluzioni e le frequenze di aggiornamento per consentire le ottimizzazioni a schermo intero. Queste modifiche possono essere apportate da un'app senza usare questo metodo

When o [**IDXGISwapChain::P**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) restart o [**IDXGISwapChain1::P**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) reinviate viene chiamato, il buffer nascosto da presentare deve trovarsi nello stato della [**\_ risorsa \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) . La presente operazione avrà esito negativo con la **\_ chiamata di errore DXGI \_ non valida \_** in caso contrario.

Le catene di scambio a schermo intero continuano a avere la restrizione che [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)(false, null) deve essere chiamato prima della versione finale della catena di scambio. **SetFullscreenState**(false) ha esito positivo sulle catene di scambio in esecuzione su dispositivi Direct3D 12.

Le operazioni presenti si verificano nella coda 3D fornita al momento della creazione del presentazione catena e le app possono presentare contemporaneamente più catene di scambio e registrare ed eseguire elenchi di comandi.

Quando la parte finale del lavoro grafico (ad esempio, la post-elaborazione dei frame) viene eseguita in una coda di calcolo o non interessa la coda grafica del dispositivo, la creazione di una seconda coda 3D da presentare può risultare utile e impedire la latenza di presentazione che ritarda l'avvio del frame successivo. 

### <a name="example"></a>Esempio

Il codice di esempio seguente sarà presente nel ciclo di rendering principale:

```cpp
void Present()
{
    m_swapChain->Present(0, m_presentFlags);
    m_backBufferIndex = (m_backBufferIndex + 1) % m_backBufferCount;
}
```

### <a name="creating-swap-chains"></a>Creazione di catene di scambio

Quando si usano le chiamate a [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)o [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) , si noti che il parametro *PDEVICE* richiede effettivamente un puntatore a una coda di comandi diretta in Direct3D 12 e non a un dispositivo.

### <a name="presenting-on-windows-7"></a>Presentazione su Windows 7

Quando la destinazione è Direct3D 12 in Windows 7, i tipi di DXGI necessari per Direct3D 12 non sono presenti, quindi è necessario usare il **ID3D12CommandQueueDownLevel** fornito da D3D12On7 (sottoposto a query dalla coda dei comandi diretta) per presentare.

Si fornisce un elenco di comandi aperti al metodo Windows 7 presente, che verrà quindi usato, chiuso e inviato automaticamente al dispositivo. È necessario fornire un buffer nascosto che deve essere creato dall'app, deve essere una risorsa di cui è stato eseguito il commit, deve essere un singolo campionamento e deve essere uno dei formati seguenti.

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
* [Esercitazioni video su DirectX Advanced Learning: framerate non limitato](https://www.youtube.com/watch?v=wn02zCXa9IU)
* [Rendering](rendering.md)
