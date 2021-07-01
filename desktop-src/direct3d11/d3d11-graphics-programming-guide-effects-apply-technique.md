---
title: Applicare una tecnica (Direct3D 11)
description: Informazioni su come impostare lo stato dell'effetto nel dispositivo per Direct3D 11 dopo che le costanti, le trame e lo stato dello shader sono stati dichiarati e inizializzati.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d03f92957eaf1b3d501c0acd54aafde7e16d8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118946"
---
# <a name="apply-a-technique-direct3d-11"></a><span data-ttu-id="c7b3e-103">Applicare una tecnica (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="c7b3e-103">Apply a Technique (Direct3D 11)</span></span>

<span data-ttu-id="c7b3e-104">Con le costanti, le trame e lo stato dello shader dichiarati e inizializzati, l'unica cosa da fare è impostare lo stato dell'effetto nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-104">With the constants, textures, and shader state declared and initialized, the only thing left to do is to set the effect state in the device.</span></span>

## <a name="set-non-shader-state-in-the-device"></a><span data-ttu-id="c7b3e-105">Impostare lo stato non shader nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="c7b3e-105">Set Non-Shader State in the Device</span></span>

<span data-ttu-id="c7b3e-106">Uno stato della pipeline non è impostato da un effetto.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-106">Some pipeline state is not set by an effect.</span></span> <span data-ttu-id="c7b3e-107">Ad esempio, la cancellazione di una destinazione di rendering prepara la destinazione di rendering per i dati.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-107">For example clearing a render target prepares the render target for data.</span></span> <span data-ttu-id="c7b3e-108">Prima di impostare lo stato dell'effetto nel dispositivo, ecco un esempio di cancellazione dei buffer di output.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-108">Before setting the effect state in the device, here is an example of clearing output buffers.</span></span>


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a><span data-ttu-id="c7b3e-109">Impostare lo stato dell'effetto nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="c7b3e-109">Set Effect State in the Device</span></span>

<span data-ttu-id="c7b3e-110">L'impostazione dello stato dell'effetto viene eseguita applicando lo stato dell'effetto all'interno del ciclo di rendering.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-110">Setting effect state is done by applying the effect state within the render loop.</span></span> <span data-ttu-id="c7b3e-111">Questa operazione viene eseguita dall'esterno in .</span><span class="sxs-lookup"><span data-stu-id="c7b3e-111">This is done from the outside in.</span></span> <span data-ttu-id="c7b3e-112">Ovvero, selezionare una tecnica e quindi impostare lo stato per ogni passaggio (a seconda del risultato desiderato).</span><span class="sxs-lookup"><span data-stu-id="c7b3e-112">That is, select a technique, and then set the state for each of the passes (depending on your desired result).</span></span>


```
    D3D11_TECHNIQUE_DESC techDesc;
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



<span data-ttu-id="c7b3e-113">Un effetto non esegue il rendering di alcun elemento, ma imposta semplicemente lo stato dell'effetto sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-113">An effect doesn't render anything, it simply sets effect state to the device.</span></span> <span data-ttu-id="c7b3e-114">Il codice di rendering viene chiamato dopo che lo stato dell'effetto aggiorna lo stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-114">The rendering code is called after the effect state updates device state.</span></span> <span data-ttu-id="c7b3e-115">In questo esempio la chiamata DrawIndexed esegue il rendering.</span><span class="sxs-lookup"><span data-stu-id="c7b3e-115">In this example, the DrawIndexed call performs the rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7b3e-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7b3e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7b3e-117">Rendering di un effetto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="c7b3e-117">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




