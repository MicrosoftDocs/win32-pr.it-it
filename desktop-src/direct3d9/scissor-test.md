---
description: Il test a forbice esegue il ritaglio dei pixel esterni al rettangolo della forbice, una sottosezione rettangolare definita dall'utente della destinazione di rendering.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Test a forbice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304376"
---
# <a name="scissor-test-direct3d-9"></a><span data-ttu-id="11f0e-103">Test a forbice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="11f0e-103">Scissor Test (Direct3D 9)</span></span>

<span data-ttu-id="11f0e-104">Il test a forbice esegue il ritaglio dei pixel esterni al rettangolo della forbice, una sottosezione rettangolare definita dall'utente della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="11f0e-104">The scissor test culls pixels that are outside of the scissor rectangle, a user-defined rectangular sub-section of the render target.</span></span>

<span data-ttu-id="11f0e-105">Il rettangolo a forbice può essere usato per indicare l'area della destinazione di rendering in cui viene disegnato il mondo del gioco.</span><span class="sxs-lookup"><span data-stu-id="11f0e-105">The scissor rectangle could be used to indicate the area of the render target where the game world is drawn.</span></span> <span data-ttu-id="11f0e-106">L'area esterna al rettangolo viene abbattuti e potrebbe essere dedicata all'interfaccia utente grafica del gioco.</span><span class="sxs-lookup"><span data-stu-id="11f0e-106">The area outside the rectangle is culled and could be devoted to a game's GUI.</span></span> <span data-ttu-id="11f0e-107">Il test a forbice non può eliminare aree non rettangolari.</span><span class="sxs-lookup"><span data-stu-id="11f0e-107">The scissor test cannot cull non-rectangular areas.</span></span>

<span data-ttu-id="11f0e-108">I rettangoli a forbice non possono essere impostati su un numero maggiore rispetto alla destinazione di rendering, ma possono essere impostati su un numero maggiore rispetto al viewport.</span><span class="sxs-lookup"><span data-stu-id="11f0e-108">Scissor rectangles cannot be set larger than the render target, but they can be set larger than the viewport.</span></span>

<span data-ttu-id="11f0e-109">Il rettangolo a forbice è gestito da uno stato di rendering del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11f0e-109">The scissor rectangle is managed by a device render state.</span></span> <span data-ttu-id="11f0e-110">Un test a forbice viene abilitato o disabilitato impostando RenderState su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="11f0e-110">A scissor test is enabled or disabled by setting the renderstate to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="11f0e-111">Questo test viene eseguito dopo il calcolo del colore del frammento ma prima del test alfa.</span><span class="sxs-lookup"><span data-stu-id="11f0e-111">This test is performed after the fragment color is computed but before alpha testing.</span></span> <span data-ttu-id="11f0e-112">[**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) Reimposta il rettangolo della forbice sulla destinazione di rendering completa, analoga alla reimpostazione del viewport.</span><span class="sxs-lookup"><span data-stu-id="11f0e-112">[**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) resets the scissor rectangle to the full render target, analogous to the viewport reset.</span></span> <span data-ttu-id="11f0e-113">[**IDirect3DDevice9:: SetScissorRect**](/windows/desktop/api) viene registrato da Stateblocks e [**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) con l'impostazione All State (D3DSBT \_ All value in [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span><span class="sxs-lookup"><span data-stu-id="11f0e-113">[**IDirect3DDevice9::SetScissorRect**](/windows/desktop/api) is recorded by stateblocks, and [**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) with the all state setting (D3DSBT\_ALL value in [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span></span> <span data-ttu-id="11f0e-114">Il test a forbice influisca anche sull'operazione [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11f0e-114">The scissor test also affects the device [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) operation.</span></span>


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



<span data-ttu-id="11f0e-115">Il rettangolo a forbice predefinito è il viewport completo.</span><span class="sxs-lookup"><span data-stu-id="11f0e-115">The default scissor rectangle is the full viewport.</span></span>

<span data-ttu-id="11f0e-116">Il test a forbice viene eseguito subito dopo il completamento dell'elaborazione dei pixel da parte di un pixel shader o della pipeline della funzione fissa, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="11f0e-116">Scissor testing is done just after pixel processing is completed by a pixel shader or the fixed function pipeline, as shown in the following diagram.</span></span>

![diagramma del momento in cui viene eseguito il test a forbice rispetto ad altri passaggi](images/scissor-test.png)

## <a name="related-topics"></a><span data-ttu-id="11f0e-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11f0e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11f0e-119">Pipeline pixel</span><span class="sxs-lookup"><span data-stu-id="11f0e-119">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
