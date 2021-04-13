---
description: Più destinazioni di rendering (MRT) si riferiscono alla possibilità di eseguire il rendering su più superfici (vedere IDirect3D9Surface) con una singola chiamata di disegnare.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Più destinazioni di rendering (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb7aafeedb621e43abb288eb9bbceb17ddb0cc0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482045"
---
# <a name="multiple-render-targets-direct3d-9"></a><span data-ttu-id="fe7c0-103">Più destinazioni di rendering (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fe7c0-103">Multiple Render Targets (Direct3D 9)</span></span>

<span data-ttu-id="fe7c0-104">Più destinazioni di rendering (MRT) si riferiscono alla possibilità di eseguire il rendering su più superfici (vedere [**IDirect3D9Surface**](/windows/desktop/api)) con una singola chiamata di disegnare.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-104">Multiple Render Targets (MRT) refers to the ability to render to multiple surfaces (see [**IDirect3D9Surface**](/windows/desktop/api)) with a single draw call.</span></span> <span data-ttu-id="fe7c0-105">Queste superfici possono essere create indipendentemente l'una dall'altra.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-105">These surfaces can be created independently of each other.</span></span> <span data-ttu-id="fe7c0-106">È possibile impostare le destinazioni di rendering usando [**IDirect3DDevice9:: SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span><span class="sxs-lookup"><span data-stu-id="fe7c0-106">Render targets can be set using [**IDirect3DDevice9::SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span></span>

<span data-ttu-id="fe7c0-107">Più destinazioni di rendering presentano le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fe7c0-107">Multiple render targets have the following restrictions:</span></span>

-   <span data-ttu-id="fe7c0-108">Tutte le superfici di destinazione di rendering utilizzate insieme devono avere la stessa profondità del bit, ma possono avere formati diversi, a meno che non \_ sia impostato il limite di D3DPMISCCAPS MRTINDEPENDENTBITDEPTHS.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-108">All render target surfaces used together must have the same bit depth but can be of different formats, unless the D3DPMISCCAPS\_MRTINDEPENDENTBITDEPTHS cap is set.</span></span>
-   <span data-ttu-id="fe7c0-109">Tutte le superfici di una destinazione di rendering multipla devono avere la stessa larghezza e altezza.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-109">All surfaces of a multiple render target should have the same width and height.</span></span>
-   <span data-ttu-id="fe7c0-110">Alcune implementazioni non possono eseguire operazioni post-pixel shader su più destinazioni di rendering, tra cui: nessun dithering, test alfa, nessuna nebbia, nessuna fusione o maschera, eccetto il test z-test e stencil.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-110">Some implementations cannot perform post-pixel shader operations on multiple render targets, including: no dithering, alpha test, no fogging, no blending or masking, except the z-test and stencil test.</span></span> <span data-ttu-id="fe7c0-111">I dispositivi in grado di supportare operazioni post-pixel shader impostano il bit Cap su D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-111">Devices that can support post-pixel shader operations set the cap bit to D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING.</span></span>

    <span data-ttu-id="fe7c0-112">Quando \_ viene impostato il limite di MRTPOSTPIXELSHADERBLENDING D3DPMISCCAPS, è necessario prima di tutto consultare [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con la query sull'utilizzo \_ POSTPIXELSHADER il risultato della \_ \_ fusione per il formato di superficie specifico.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-112">When the D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING cap is set, you must first consult the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with the USAGE\_QUERY\_POSTPIXELSHADER\_BLENDING result for the specific surface format.</span></span> <span data-ttu-id="fe7c0-113">Se false, non sarà disponibile alcuna operazione di fusione post-pixel shader per quel formato di superficie specifico.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-113">If false, no post-pixel shader blending operations will be available for that specific surface format.</span></span> <span data-ttu-id="fe7c0-114">Se true, il dispositivo dovrebbe applicare lo stesso stato a tutte le destinazioni di rendering simultanee come segue:</span><span class="sxs-lookup"><span data-stu-id="fe7c0-114">If true, the device is expected to apply the same state to all simultaneous render targets as follows:</span></span>

    -   <span data-ttu-id="fe7c0-115">Alpha Blend: il valore del colore in oCi viene blended con la destinazione di rendering Ith.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-115">Alpha blend: The color value in oCi is blended with the ith render target.</span></span>
    -   <span data-ttu-id="fe7c0-116">Test alfa: il confronto avverrà con oC0.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-116">Alpha test: Comparison will happen with oC0.</span></span> <span data-ttu-id="fe7c0-117">Se il confronto ha esito negativo, il test pixel viene terminato per tutte le destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-117">If the comparison fails, the pixel test is terminated for all render targets.</span></span>
    -   <span data-ttu-id="fe7c0-118">Fog: la destinazione di rendering 0 viene offuscata.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-118">Fog: Render target 0 will get fogged.</span></span> <span data-ttu-id="fe7c0-119">Altre destinazioni di rendering non sono definite.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-119">Other render targets are undefined.</span></span> <span data-ttu-id="fe7c0-120">Le implementazioni possono scegliere di offuscarle tutte usando lo stesso stato.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-120">Implementations can choose to fog them all using the same state.</span></span>
    -   <span data-ttu-id="fe7c0-121">Rethering: non definito.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-121">Dithering: Undefined.</span></span>

-   <span data-ttu-id="fe7c0-122">Non è supportato l'anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-122">No antialiasing is supported.</span></span>
-   <span data-ttu-id="fe7c0-123">Alcune implementazioni non applicano la maschera di scrittura di output (D3DRS \_ COLORWRITEENABLE).</span><span class="sxs-lookup"><span data-stu-id="fe7c0-123">Some of the implementations do not apply the output write mask (D3DRS\_COLORWRITEENABLE).</span></span> <span data-ttu-id="fe7c0-124">Quelli che possono avere maschere di scrittura a colori indipendenti.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-124">Those that can, have independent color write masks.</span></span> <span data-ttu-id="fe7c0-125">Viene espresso usando un nuovo bit di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-125">This is expressed using a new capability bit.</span></span> <span data-ttu-id="fe7c0-126">Il numero di maschere di scrittura a colori indipendenti disponibili sarà uguale al numero massimo di elementi che il dispositivo è in grado di supportare.</span><span class="sxs-lookup"><span data-stu-id="fe7c0-126">The number of independent color write masks available will be equal to the maximum number of elements the device is capable of.</span></span>

<span data-ttu-id="fe7c0-127">Nuovi tappi hardware:</span><span class="sxs-lookup"><span data-stu-id="fe7c0-127">New hardware caps:</span></span>


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a><span data-ttu-id="fe7c0-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe7c0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe7c0-129">Pipeline pixel</span><span class="sxs-lookup"><span data-stu-id="fe7c0-129">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
