---
title: Come creare una catena di scambio
description: In questo argomento viene illustrato come creare una catena di scambio che incapsula due o più buffer utilizzati per il rendering e la visualizzazione.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ef97b261d9831c451c8a81bfc1f4d9d13b1cd423ac28f38de4b90c1d4ae100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530573"
---
# <a name="how-to-create-a-swap-chain"></a>Procedura: Creare una catena di scambio

In questo argomento viene illustrato come creare una catena di scambio che incapsula due o più buffer utilizzati per il rendering e la visualizzazione. Contengono in genere un buffer anteriore che viene presentato al dispositivo di visualizzazione e un buffer nascosto che funge da destinazione di rendering. Al termine del rendering del contesto immediato nel buffer nascosto, la catena di scambio presenta il buffer nascosto scambiando i due buffer.

La catena di scambio definisce diverse caratteristiche di rendering, tra cui:

-   Dimensioni dell'area di rendering.
-   Frequenza di aggiornamento dello schermo.
-   Modalità di visualizzazione.
-   Formato della superficie.

Definire le caratteristiche della catena di scambio compilando una struttura [**\_ DXGI SWAP CHAIN \_ \_ DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) e inizializzando [**un'interfaccia IDXGISwapChain.**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) Inizializzare una catena di scambio chiamando [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="create-a-device-and-a-swap-chain"></a>Creare un dispositivo e una catena di scambio

Per inizializzare un dispositivo e una catena di scambio, usare una delle due funzioni seguenti:

-   Usare la [**funzione D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) quando si vuole inizializzare la catena di scambio contemporaneamente all'inizializzazione del dispositivo. Questa è in genere l'opzione più semplice.

-   Usare la [**funzione D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) quando è già stata creata una catena di scambio [**usando IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 