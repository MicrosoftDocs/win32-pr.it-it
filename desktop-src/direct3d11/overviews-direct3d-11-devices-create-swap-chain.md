---
title: Come creare una catena di scambio
description: In questo argomento viene illustrato come creare una catena di scambio che incapsula due o più buffer utilizzati per il rendering e la visualizzazione.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8355eafff6e233b89be82fd9e58ca53224248e84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399358"
---
# <a name="how-to-create-a-swap-chain"></a>Procedura: creare una catena di scambio

In questo argomento viene illustrato come creare una catena di scambio che incapsula due o più buffer utilizzati per il rendering e la visualizzazione. Contengono in genere un buffer anteriore presentato al dispositivo di visualizzazione e un buffer nascosto che funge da destinazione di rendering. Al termine del rendering del contesto immediato nel buffer nascosto, la catena di scambio presenta il buffer nascosto scambiando i due buffer.

La catena di scambio definisce diverse caratteristiche di rendering, tra cui:

-   Dimensioni dell'area di rendering.
-   Frequenza di aggiornamento della visualizzazione.
-   Modalità di visualizzazione.
-   Formato della superficie.

Definire le caratteristiche della catena di scambio compilando una struttura [**DXGI \_ swap \_ Chain \_ desc**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) e inizializzando un'interfaccia [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) . Inizializzare una catena di scambio chiamando [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="create-a-device-and-a-swap-chain"></a>Creare un dispositivo e una catena di scambio

Per inizializzare un dispositivo e una catena di scambio, usare una delle due funzioni seguenti:

-   Usare la funzione [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) quando si vuole inizializzare la catena di scambio nello stesso momento dell'inizializzazione del dispositivo. Questa è in genere l'opzione più semplice.

-   Usare la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) quando è già stata creata una catena di scambio con [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 