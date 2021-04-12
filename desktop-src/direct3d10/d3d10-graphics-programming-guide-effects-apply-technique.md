---
description: Con le costanti, le trame e lo stato dello shader dichiarati e inizializzati, l'unica cosa che rimane da fare è impostare lo stato dell'effetto nel dispositivo.
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: Applicare una tecnica (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7cc48c9115dfb81c1688a3a499e24d46cc563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483013"
---
# <a name="apply-a-technique-direct3d-10"></a><span data-ttu-id="45694-103">Applicare una tecnica (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="45694-103">Apply a Technique (Direct3D 10)</span></span>

<span data-ttu-id="45694-104">Con le costanti, le trame e lo stato dello shader dichiarati e inizializzati, l'unica cosa che rimane da fare è impostare lo stato dell'effetto nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45694-104">With the constants, textures, and shader state declared and initialized, the only thing left to do is to set the effect state in the device.</span></span>

## <a name="set-non-shader-state-in-the-device"></a><span data-ttu-id="45694-105">Impostare lo stato non dello shader nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="45694-105">Set Non-Shader State in the Device</span></span>

<span data-ttu-id="45694-106">Uno stato della pipeline non è impostato da un effetto.</span><span class="sxs-lookup"><span data-stu-id="45694-106">Some pipeline state is not set by an effect.</span></span> <span data-ttu-id="45694-107">Ad esempio, la cancellazione di una destinazione di rendering prepara la destinazione di rendering per i dati.</span><span class="sxs-lookup"><span data-stu-id="45694-107">For example clearing a render target prepares the render target for data.</span></span> <span data-ttu-id="45694-108">Prima di impostare lo stato dell'effetto nel dispositivo, di seguito è riportato un esempio di cancellazione dei buffer di output.</span><span class="sxs-lookup"><span data-stu-id="45694-108">Before setting the effect state in the device, here is an example of clearing output buffers.</span></span>


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a><span data-ttu-id="45694-109">Impostare lo stato dell'effetto nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="45694-109">Set Effect State in the Device</span></span>

<span data-ttu-id="45694-110">L'impostazione dello stato dell'effetto viene eseguita applicando lo stato dell'effetto all'interno del ciclo di rendering.</span><span class="sxs-lookup"><span data-stu-id="45694-110">Setting effect state is done by applying the effect state within the render loop.</span></span> <span data-ttu-id="45694-111">Questa operazione viene eseguita dall'esterno di.</span><span class="sxs-lookup"><span data-stu-id="45694-111">This is done from the outside in.</span></span> <span data-ttu-id="45694-112">Ovvero selezionare una tecnica, quindi impostare lo stato per ogni passaggio (a seconda del risultato desiderato).</span><span class="sxs-lookup"><span data-stu-id="45694-112">That is, select a technique, and then set the state for each of the passes (depending on your desired result).</span></span>


```
    D3D10_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



<span data-ttu-id="45694-113">Un effetto non esegue alcun rendering, ma imposta semplicemente lo stato dell'effetto sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45694-113">An effect doesn't render anything, it simply sets effect state to the device.</span></span> <span data-ttu-id="45694-114">Il codice di rendering viene chiamato dopo che lo stato dell'effetto aggiorna lo stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45694-114">The rendering code is called after the effect state updates device state.</span></span> <span data-ttu-id="45694-115">In questo esempio, la chiamata a DrawIndexed esegue il rendering.</span><span class="sxs-lookup"><span data-stu-id="45694-115">In this example, the DrawIndexed call performs the rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45694-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="45694-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45694-117">Rendering di un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="45694-117">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



