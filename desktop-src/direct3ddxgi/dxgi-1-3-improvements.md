---
description: Le funzionalità seguenti sono state aggiunte in Microsoft DirectX Graphics Infrastructure (DXGI) 1,3, incluso a partire da Windows 8.1.
ms.assetid: 56816212-2B6A-41EC-B57D-29DEBBF440E7
title: Miglioramenti di DXGI 1,3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c863bc30ffdf27705492b56a5348040c8e12f4fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876273"
---
# <a name="dxgi-13-improvements"></a>Miglioramenti di DXGI 1,3

Le funzionalità seguenti sono state aggiunte in Microsoft DirectX Graphics Infrastructure (DXGI) 1,3, incluso a partire da Windows 8.1.

## <a name="trim-dxgi-adapter-memory-usage"></a>Taglia utilizzo memoria scheda DXGI

A partire da Windows 8.1, DXGI 1,3 aggiunge la funzionalità per scaricare e rilasciare le risorse di memoria inutilizzate allocate dall'adattatore DXGI. Questo consente alle app di rilasciare memoria temporanea durante la sospensione, riducendo le probabilità che l'app venga terminata per liberare risorse per altre app. Quando l'app riprende, i driver di dispositivo che supportano Trim ricreeranno le risorse in base alle esigenze. A partire da Windows 8.1, tutti i dispositivi Direct3D creati da un'app devono chiamare [**IDXGIDevice3:: Trim**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgidevice3-trim) durante la sospensione per ridurre il footprint di memoria e ridurre la probabilità che l'app venga terminata per recuperare le risorse di sistema.

## <a name="multi-plane-overlays"></a>Sovrapposizioni multipiano

A partire da Windows 8.1, DXGI 1,3 supporta le sovrapposizioni multipiano. È possibile verificare se il dispositivo supporta le sovrapposizioni multipiano nell'hardware usando [**IDXGIOutput2:: SupportsOverlays**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays).

## <a name="overlapping-swap-chains-and-swap-chain-scaling"></a>Catene di scambio sovrapposte e scalabilità della catena di scambio

A partire da Windows 8.1, DXGI 1,3 supporta catene di swapping sovrapposte. Le catene di scambio sovrapposte vengono usate per creare grafica 3D in risoluzioni non native (con scalabilità hardware), presentando l'interfaccia utente alla risoluzione nativa. Questo consente ai giochi di sfruttare i vantaggi di una velocità di riempimento superiore per il gameplay reattivo senza peggiorare la qualità visiva degli elementi dell'interfaccia utente, come il punteggio del lettore e il testo della finestra di dialogo. Nei dispositivi che supportano sovrapposizioni multipiano, Direct3D utilizzerà sovrimpressioni a più livelli per le catene di scambio sovrapposte. Creare una catena di scambio in primo piano specificando il flag del [**\_ \_ \_ \_ \_ livello di primo piano del flag della catena di scambio DXGI**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) durante la creazione della catena di scambio e usare [**IDXGISwapChain2:: SetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform) e [**IDXGISwapChain2:: GetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform) per ridimensionare la catena di scambio usata per il gioco.

## <a name="select-backbuffer-subregion-for-swap-chain"></a>Selezionare l'area secondaria backBuffer per la catena di scambio

A partire da Windows 8.1, è possibile usare DXGI 1,3 per selezionare un'area secondaria del backBuffer da usare con la catena di scambio, rendendo possibile il rendering in un buffer nascosto più piccolo senza ricreare la catena di scambio. Vedere [**IDXGISwapChain2:: SetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize) e [**IDXGISwapChain2:: GetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getsourcesize).

## <a name="lower-latency-swap-chain-presentation"></a>Presentazione della catena di scambio con latenza inferiore

A partire da Windows 8.1, DXGI 1,3 rende possibile ridurre la latenza consentendo alla catena di scambio di terminare la presentazione del frame precedente prima di iniziare a usare il dispositivo per creare il frame successivo. Vedere [**IDXGISwapChain2:: GetFrameLatencyWaitableObject**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject), [**IDXGISwapChain2:: GetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency)e [**IDXGISwapChain2:: SetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency).

## <a name="related-topics"></a>Argomenti correlati

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
