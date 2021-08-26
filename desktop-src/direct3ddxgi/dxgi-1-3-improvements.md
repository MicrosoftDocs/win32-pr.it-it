---
description: La funzionalità seguente è stata aggiunta in Microsoft DirectX Graphic Infrastructure (DXGI) 1.3, incluso a partire da Windows 8.1.
ms.assetid: 56816212-2B6A-41EC-B57D-29DEBBF440E7
title: Miglioramenti di DXGI 1.3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709dc9e98ffe6ecd67f6bd91aa654b1e0bfe0375dabcd2a344f5b012c57dca2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984121"
---
# <a name="dxgi-13-improvements"></a>Miglioramenti di DXGI 1.3

La funzionalità seguente è stata aggiunta in Microsoft DirectX Graphic Infrastructure (DXGI) 1.3, incluso a partire da Windows 8.1.

## <a name="trim-dxgi-adapter-memory-usage"></a>Ridurre l'utilizzo della memoria dell'adapter DXGI

A partire Windows 8.1, DXGI 1.3 aggiunge la funzionalità per scaricare e rilasciare le risorse di memoria inutilizzate allocate dall'adapter DXGI. Ciò consente alle app di rilasciare memoria temporanea durante la sospensione, riducendo la probabilità che l'app venga terminata per liberare risorse per altre app. Quando l'app riprende, i driver di dispositivo che supportano trim ricreano le risorse in base alle esigenze. A Windows 8.1, tutti i dispositivi Direct3D creati da un'app devono chiamare [**IDXGIDevice3::Trim**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgidevice3-trim) durante la sospensione per ridurre il footprint di memoria e ridurre la probabilità che l'app venga terminata per recuperare le risorse di sistema.

## <a name="multi-plane-overlays"></a>Sovrapposizioni su più piani

A partire Windows 8.1, DXGI 1.3 supporta le sovrapposizioni su più piani. È possibile verificare se il dispositivo supporta sovrapposizioni multi-piano nell'hardware usando [**IDXGIOutput2::SupportsOverlays**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays).

## <a name="overlapping-swap-chains-and-swap-chain-scaling"></a>Concatenazioni di scambio sovrapposte e ridimensionamento della catena di scambio

A partire da Windows 8.1, DXGI 1.3 supporta catene di scambio sovrapposte. Le catene di scambio sovrapposte vengono usate per disegnare grafica 3D a risoluzioni non native (con scalabilità orizzontale dell'hardware) durante la presentazione dell'interfaccia utente alla risoluzione nativa. Ciò consente ai giochi di sfruttare percentuali di riempimento più elevate per il gioco reattivo senza ridurre la qualità visiva degli elementi dell'interfaccia utente, ad esempio il punteggio del giocatore e il testo del dialogo. Nei dispositivi che supportano sovrapposizioni multi-piano, Direct3D userà sovrapposizioni multi-piano per catene di scambio sovrapposte. Creare una catena di scambio in primo piano specificando il flag [**DXGI \_ SWAP CHAIN FLAG FOREGROUND \_ \_ \_ \_ LAYER**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) durante la creazione della catena di scambio e usare [**IDXGISwapChain2::SetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform) e [**IDXGISwapChain2::GetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform) per ridimensionare la catena di scambio usata per il gioco.

## <a name="select-backbuffer-subregion-for-swap-chain"></a>Selezionare la sottoarea backbuffer per la catena di scambio

A partire da Windows 8.1, È possibile usare DXGI 1.3 per selezionare una sottoarea del backbuffer da usare con la catena di scambio, rendendo possibile il rendering in un buffer nascosto più piccolo senza ricreare la catena di scambio. Vedere [**IDXGISwapChain2::SetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize) e [**IDXGISwapChain2::GetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getsourcesize).

## <a name="lower-latency-swap-chain-presentation"></a>Presentazione della catena di scambio a bassa latenza

A partire da Windows 8.1, DXGI 1.3 consente di ridurre la latenza consentendo alla catena di scambio di completare la presentazione del frame precedente prima di iniziare a usare il dispositivo per disegnare il frame successivo. Vedere [**IDXGISwapChain2::GetFrameLatencyWaitableObject**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject), [**IDXGISwapChain2::GetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency)e [**IDXGISwapChain2::SetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency).

## <a name="related-topics"></a>Argomenti correlati

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
