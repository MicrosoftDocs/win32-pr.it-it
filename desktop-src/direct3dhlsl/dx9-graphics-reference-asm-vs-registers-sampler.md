---
title: Campionatore (Direct3D 9 ASM-vs)
description: Un campionatore è uno pseudo-registro di input per un vertex shader, usato per identificare la fase di campionamento. Sono disponibili quattro campionatori vertex shader S0 per S3. Quattro superfici di trama possono essere lette in un singolo passaggio dello shader.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Campionatore, tipo (Direct3D 9 ASM-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399664"
---
# <a name="sampler-direct3d-9-asm-vs"></a><span data-ttu-id="24823-106">Campionatore (Direct3D 9 ASM-vs)</span><span class="sxs-lookup"><span data-stu-id="24823-106">Sampler (Direct3D 9 asm-vs)</span></span>

<span data-ttu-id="24823-107">Un campionatore è uno pseudo-registro di input per un vertex shader, usato per identificare la fase di campionamento.</span><span class="sxs-lookup"><span data-stu-id="24823-107">A sampler is a input pseudo-register for a vertex shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="24823-108">Sono disponibili quattro campionatori vertex shader: S0 per S3.</span><span class="sxs-lookup"><span data-stu-id="24823-108">There are four vertex shader samplers: s0 to s3.</span></span> <span data-ttu-id="24823-109">Quattro superfici di trama possono essere lette in un singolo passaggio dello shader.</span><span class="sxs-lookup"><span data-stu-id="24823-109">Four texture surfaces can be read in a single shader pass.</span></span>

<span data-ttu-id="24823-110">Sampler (Direct3D 9 ASM-vs) s sono pseudo-registri perché non è possibile leggere o scrivere direttamente.</span><span class="sxs-lookup"><span data-stu-id="24823-110">Sampler (Direct3D 9 asm-vs)s are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="24823-111">Un'unità di campionamento corrisponde alla fase di campionamento della trama, che incapsula lo stato specifico del campionamento fornito da [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="24823-111">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="24823-112">Ogni campionatore identifica in modo univoco una singola superficie di trama, che viene impostata sul campionatore corrispondente usando la [**texture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="24823-112">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="24823-113">Tuttavia, la stessa superficie di trama può essere impostata su più Sampler.</span><span class="sxs-lookup"><span data-stu-id="24823-113">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="24823-114">In fase di disegnare non è possibile impostare contemporaneamente una trama come destinazione di rendering e una trama in una fase.</span><span class="sxs-lookup"><span data-stu-id="24823-114">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="24823-115">Poiché sono presenti quattro campionatori, è possibile leggere fino a quattro superfici di trama in un unico passaggio dello shader.</span><span class="sxs-lookup"><span data-stu-id="24823-115">Because there are four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="24823-116">Un campionatore potrebbe apparire come unico argomento nell'istruzione di caricamento della trama: [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="24823-116">A sampler might appear as the only argument in the texture load instruction: [texldl - vs](texldl---vs.md).</span></span>

<span data-ttu-id="24823-117">In vs \_ 3 \_ 0, se viene usato un campionatore, è necessario dichiararlo all'inizio del programma shader usando l'istruzione [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="24823-117">In vs\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md) instruction.</span></span>



| <span data-ttu-id="24823-118">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="24823-118">Vertex shader versions</span></span> | <span data-ttu-id="24823-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="24823-119">1\_1</span></span> | <span data-ttu-id="24823-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="24823-120">2\_0</span></span> | <span data-ttu-id="24823-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="24823-121">2\_sw</span></span> | <span data-ttu-id="24823-122">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="24823-122">2\_x</span></span> | <span data-ttu-id="24823-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="24823-123">3\_0</span></span> | <span data-ttu-id="24823-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="24823-124">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="24823-125">Campionatore</span><span class="sxs-lookup"><span data-stu-id="24823-125">Sampler</span></span>                |      |      |       |      | <span data-ttu-id="24823-126">x</span><span class="sxs-lookup"><span data-stu-id="24823-126">x</span></span>    | <span data-ttu-id="24823-127">x</span><span class="sxs-lookup"><span data-stu-id="24823-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="24823-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24823-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24823-129">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="24823-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[<span data-ttu-id="24823-130">Trame di vertici in vs \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="24823-130">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 