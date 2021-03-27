---
title: Campionatore (Direct3D 9 ASM-PS)
description: Un campionatore è uno pseudo-registro di input per un pixel shader, che viene usato per identificare la fase di campionamento.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Campionatore, tipo (Direct3D 9 ASM-PS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046922"
---
# <a name="sampler-direct3d-9-asm-ps"></a><span data-ttu-id="d4cc2-104">Campionatore (Direct3D 9 ASM-PS)</span><span class="sxs-lookup"><span data-stu-id="d4cc2-104">Sampler (Direct3D 9 asm-ps)</span></span>

<span data-ttu-id="d4cc2-105">Un campionatore è uno pseudo-registro di input per un pixel shader, che viene usato per identificare la fase di campionamento.</span><span class="sxs-lookup"><span data-stu-id="d4cc2-105">A sampler is a input pseudo-register for a pixel shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="d4cc2-106">Sono disponibili 16 registri per la fase di campionamento pixel shader: S0 per S15.</span><span class="sxs-lookup"><span data-stu-id="d4cc2-106">There are 16 pixel shader sampling stage registers: s0 to s15.</span></span> <span data-ttu-id="d4cc2-107">Pertanto, è possibile leggere fino a 16 superfici di trama in un singolo passaggio dello shader.</span><span class="sxs-lookup"><span data-stu-id="d4cc2-107">Therefore, up to 16 texture surfaces can be read in a single shader pass.</span></span> <span data-ttu-id="d4cc2-108">Le istruzioni che usano un registro campionatore sono texld e texldp.</span><span class="sxs-lookup"><span data-stu-id="d4cc2-108">The instructions that use a sampler register are texld and texldp.</span></span>

<span data-ttu-id="d4cc2-109">Il campionatore deve essere dichiarato prima dell'uso con l'istruzione [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="d4cc2-109">Sampler must be declared before use with the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>



| <span data-ttu-id="d4cc2-110">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="d4cc2-110">Pixel shader versions</span></span> | <span data-ttu-id="d4cc2-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="d4cc2-111">1\_1</span></span> | <span data-ttu-id="d4cc2-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="d4cc2-112">1\_2</span></span> | <span data-ttu-id="d4cc2-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d4cc2-113">1\_3</span></span> | <span data-ttu-id="d4cc2-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="d4cc2-114">1\_4</span></span> | <span data-ttu-id="d4cc2-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d4cc2-115">2\_0</span></span> | <span data-ttu-id="d4cc2-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d4cc2-116">2\_sw</span></span> | <span data-ttu-id="d4cc2-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d4cc2-117">2\_x</span></span> | <span data-ttu-id="d4cc2-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d4cc2-118">3\_0</span></span> | <span data-ttu-id="d4cc2-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d4cc2-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="d4cc2-120">Campionatore</span><span class="sxs-lookup"><span data-stu-id="d4cc2-120">Sampler</span></span>               |      |      |      |      | <span data-ttu-id="d4cc2-121">x</span><span class="sxs-lookup"><span data-stu-id="d4cc2-121">x</span></span>    | <span data-ttu-id="d4cc2-122">x</span><span class="sxs-lookup"><span data-stu-id="d4cc2-122">x</span></span>     | <span data-ttu-id="d4cc2-123">x</span><span class="sxs-lookup"><span data-stu-id="d4cc2-123">x</span></span>    | <span data-ttu-id="d4cc2-124">x</span><span class="sxs-lookup"><span data-stu-id="d4cc2-124">x</span></span>    | <span data-ttu-id="d4cc2-125">x</span><span class="sxs-lookup"><span data-stu-id="d4cc2-125">x</span></span>     |



 

<span data-ttu-id="d4cc2-126">I sampler sono pseudo-registri perché non è possibile leggerli o scriverli direttamente.</span><span class="sxs-lookup"><span data-stu-id="d4cc2-126">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="d4cc2-127">Un'unità di campionamento corrisponde alla fase di campionamento della trama, che incapsula lo stato specifico del campionamento fornito da [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="d4cc2-127">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="d4cc2-128">Ogni campionatore identifica in modo univoco una singola superficie di trama, che viene impostata sul campionatore corrispondente usando la [**texture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="d4cc2-128">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="d4cc2-129">Tuttavia, la stessa superficie di trama può essere impostata su più Sampler.</span><span class="sxs-lookup"><span data-stu-id="d4cc2-129">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="d4cc2-130">In fase di disegnare non è possibile impostare contemporaneamente una trama come destinazione di rendering e una trama in una fase.</span><span class="sxs-lookup"><span data-stu-id="d4cc2-130">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="d4cc2-131">Un campionatore potrebbe apparire come unico argomento nell'istruzione di caricamento della trama: [texldl-PS](texldl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="d4cc2-131">A sampler might appear as the only argument in the texture load instruction: [texldl - ps](texldl---ps.md).</span></span>

<span data-ttu-id="d4cc2-132">In PS \_ 3 \_ 0, se viene usato un campionatore, è necessario dichiararlo all'inizio del programma shader usando l'istruzione [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="d4cc2-132">In ps\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>

<span data-ttu-id="d4cc2-133">Il campionamento di una trama con una dimensione superiore a quella presente nelle coordinate di trama non è valido.</span><span class="sxs-lookup"><span data-stu-id="d4cc2-133">Sampling a texture with a higher dimension than is present in the texture coordinates is illegal.</span></span> <span data-ttu-id="d4cc2-134">Il campionamento di una trama con una dimensione inferiore rispetto a quello presente nelle coordinate di trama ignorerà le coordinate di trama aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="d4cc2-134">Sampling a texture with a lower dimension than is present in the texture coordinates will ignore the extra texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4cc2-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d4cc2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4cc2-136">Registri</span><span class="sxs-lookup"><span data-stu-id="d4cc2-136">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 