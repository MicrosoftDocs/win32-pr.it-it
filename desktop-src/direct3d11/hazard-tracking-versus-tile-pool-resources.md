---
title: Verifica dei rischi e risorse pool di riquadri
description: Per le risorse non affiancate, Direct3D può impedire determinate condizioni di rischio durante il rendering, ma poiché il rilevamento dei rischi è a livello di riquadro per le risorse affiancate, il rilevamento delle condizioni di rischio durante il rendering delle risorse affiancate potrebbe essere troppo costoso.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395431"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a><span data-ttu-id="3be70-103">Verifica dei rischi e risorse pool di riquadri</span><span class="sxs-lookup"><span data-stu-id="3be70-103">Hazard tracking versus tile pool resources</span></span>

<span data-ttu-id="3be70-104">Per le risorse non affiancate, Direct3D può impedire determinate condizioni di rischio durante il rendering, ma poiché il rilevamento dei rischi è a livello di riquadro per le risorse affiancate, il rilevamento delle condizioni di rischio durante il rendering delle risorse affiancate potrebbe essere troppo costoso.</span><span class="sxs-lookup"><span data-stu-id="3be70-104">For non-tiled resources, Direct3D can prevent certain hazard conditions during rendering, but because hazard tracking would be at a tile level for tiled resources, tracking hazard conditions during rendering of tiled resources might be too expensive.</span></span>

<span data-ttu-id="3be70-105">Per le risorse non affiancate, ad esempio, il runtime non consente l'associazione di una determinata sottorisorsa come input (ad esempio ShaderResourceView) e come output (ad esempio, RenderTargetView) allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="3be70-105">For example, for non-tiled resources, the runtime doesn't allow any given SubResource to be bound as an input (such as a ShaderResourceView) and as an output (such as a RenderTargetView) at the same time.</span></span> <span data-ttu-id="3be70-106">Se viene rilevato un caso di questo tipo, il runtime annulla l'associazione dell'input.</span><span class="sxs-lookup"><span data-stu-id="3be70-106">If such a case is encountered, the runtime unbinds the input.</span></span> <span data-ttu-id="3be70-107">Questo sovraccarico di rilevamento nel runtime è economico e viene eseguito a livello di sottorisorse.</span><span class="sxs-lookup"><span data-stu-id="3be70-107">This tracking overhead in the runtime is cheap and is done at the SubResource level.</span></span> <span data-ttu-id="3be70-108">Uno dei vantaggi di questo sovraccarico di rilevamento consiste nel ridurre al minimo le probabilità che le applicazioni vengano accidentalmente a seconda dell'ordine di esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="3be70-108">One of the benefits of this tracking overhead is to minimize the chances of applications accidentally depending on hardware shader execution order.</span></span> <span data-ttu-id="3be70-109">L'ordine di esecuzione dello shader hardware può variare in base a una determinata GPU (Graphics Processing Unit), quindi certamente tra le diverse GPU.</span><span class="sxs-lookup"><span data-stu-id="3be70-109">Hardware shader execution order can vary if not on a given graphics processing unit (GPU), then certainly across different GPUs.</span></span>

<span data-ttu-id="3be70-110">Il rilevamento delle risorse associate potrebbe essere troppo costoso per le risorse affiancate poiché il rilevamento è a livello di riquadro.</span><span class="sxs-lookup"><span data-stu-id="3be70-110">Tracking how resources are bound might be too expensive for tiled resources because tracking is at a tile level.</span></span> <span data-ttu-id="3be70-111">Si verificano nuovi problemi, ad esempio la convalida dei tentativi di eseguire il rendering in un RenderTargetView con un riquadro mappato a più aree della superficie simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="3be70-111">New issues arise such as possibly validating away attempts to render to an RenderTargetView with one tile mapped to multiple areas in the surface simultaneously.</span></span> <span data-ttu-id="3be70-112">Se questo rilevamento dei rischi per riquadro è troppo costoso per il runtime, idealmente questa sarebbe almeno un'opzione nel livello debug.</span><span class="sxs-lookup"><span data-stu-id="3be70-112">If it turns out this per-tile hazard tracking is too expensive for the runtime, ideally this would at least be an option in the debug layer.</span></span>

<span data-ttu-id="3be70-113">Un'applicazione deve informare il driver di visualizzazione quando ha emesso un'operazione di scrittura o lettura in una risorsa affiancata che fa riferimento alla memoria del pool di riquadri a cui verrà anche fatto riferimento da risorse affiancate separate nelle operazioni di lettura o scrittura imminenti che si prevede venga completata prima di poter iniziare le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3be70-113">An application must inform the display driver when it has issued a write or read operation to a tiled resource that references tile pool memory that will also be referenced by separate tiled resources in upcoming read or write operations that it is expecting the first operation to complete before the following operations can begin.</span></span> <span data-ttu-id="3be70-114">Per altre informazioni su questa condizione, vedere [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) note.</span><span class="sxs-lookup"><span data-stu-id="3be70-114">For more info about this condition, see [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) remarks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3be70-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3be70-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3be70-116">Mapping inclusi in un pool di riquadri</span><span class="sxs-lookup"><span data-stu-id="3be70-116">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




