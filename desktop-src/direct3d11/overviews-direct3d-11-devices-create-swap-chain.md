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
# <a name="how-to-create-a-swap-chain"></a><span data-ttu-id="67551-103">Procedura: creare una catena di scambio</span><span class="sxs-lookup"><span data-stu-id="67551-103">How To: Create a Swap Chain</span></span>

<span data-ttu-id="67551-104">In questo argomento viene illustrato come creare una catena di scambio che incapsula due o più buffer utilizzati per il rendering e la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="67551-104">This topic show how to create a swap chain that encapsulates two or more buffers that are used for rendering and display.</span></span> <span data-ttu-id="67551-105">Contengono in genere un buffer anteriore presentato al dispositivo di visualizzazione e un buffer nascosto che funge da destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="67551-105">They usually contain a front buffer that is presented to the display device and a back buffer that serves as the render target.</span></span> <span data-ttu-id="67551-106">Al termine del rendering del contesto immediato nel buffer nascosto, la catena di scambio presenta il buffer nascosto scambiando i due buffer.</span><span class="sxs-lookup"><span data-stu-id="67551-106">After the immediate context is done rendering to the back buffer, the swap chain presents the back buffer by swapping the two buffers.</span></span>

<span data-ttu-id="67551-107">La catena di scambio definisce diverse caratteristiche di rendering, tra cui:</span><span class="sxs-lookup"><span data-stu-id="67551-107">The swap chain defines several rendering characteristics including:</span></span>

-   <span data-ttu-id="67551-108">Dimensioni dell'area di rendering.</span><span class="sxs-lookup"><span data-stu-id="67551-108">The size of the render area.</span></span>
-   <span data-ttu-id="67551-109">Frequenza di aggiornamento della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="67551-109">The display refresh rate.</span></span>
-   <span data-ttu-id="67551-110">Modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="67551-110">The display mode.</span></span>
-   <span data-ttu-id="67551-111">Formato della superficie.</span><span class="sxs-lookup"><span data-stu-id="67551-111">The surface format.</span></span>

<span data-ttu-id="67551-112">Definire le caratteristiche della catena di scambio compilando una struttura [**DXGI \_ swap \_ Chain \_ desc**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) e inizializzando un'interfaccia [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) .</span><span class="sxs-lookup"><span data-stu-id="67551-112">Define the characteristics of the swap chain by filling in a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure and initializing an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) interface.</span></span> <span data-ttu-id="67551-113">Inizializzare una catena di scambio chiamando [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="67551-113">Initialize a swap chain by calling [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="create-a-device-and-a-swap-chain"></a><span data-ttu-id="67551-114">Creare un dispositivo e una catena di scambio</span><span class="sxs-lookup"><span data-stu-id="67551-114">Create a device and a swap chain</span></span>

<span data-ttu-id="67551-115">Per inizializzare un dispositivo e una catena di scambio, usare una delle due funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="67551-115">To initialize a device and swap chain, use one of the following two functions:</span></span>

-   <span data-ttu-id="67551-116">Usare la funzione [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) quando si vuole inizializzare la catena di scambio nello stesso momento dell'inizializzazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67551-116">Use the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function when you want to initialize the swap chain at the same time as device initialization.</span></span> <span data-ttu-id="67551-117">Questa è in genere l'opzione più semplice.</span><span class="sxs-lookup"><span data-stu-id="67551-117">This usually is the easiest option.</span></span>

-   <span data-ttu-id="67551-118">Usare la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) quando è già stata creata una catena di scambio con [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span><span class="sxs-lookup"><span data-stu-id="67551-118">Use the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function when you have already created a swap chain using [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67551-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67551-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67551-120">Dispositivi</span><span class="sxs-lookup"><span data-stu-id="67551-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="67551-121">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="67551-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 