---
title: texldd-PS
description: Esegue il campionamento di una trama con input di sfumatura aggiuntivi.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399051"
---
# <a name="texldd---ps"></a><span data-ttu-id="3f09b-103">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="3f09b-103">texldd - ps</span></span>

<span data-ttu-id="3f09b-104">Esegue il campionamento di una trama con input di sfumatura aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="3f09b-104">Samples a texture with additional gradient inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f09b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f09b-105">Syntax</span></span>



| <span data-ttu-id="3f09b-106">texldd, DST, src0, src1, src2, src3</span><span class="sxs-lookup"><span data-stu-id="3f09b-106">texldd, dst, src0, src1, src2, src3</span></span> |
|-------------------------------------|



 

<span data-ttu-id="3f09b-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="3f09b-107">Where:</span></span>

-   <span data-ttu-id="3f09b-108">DST è un registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3f09b-108">dst is a destination register.</span></span>
-   <span data-ttu-id="3f09b-109">src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama.</span><span class="sxs-lookup"><span data-stu-id="3f09b-109">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="3f09b-110">Vedere [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="3f09b-110">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="3f09b-111">src1 identifica i registri del campionatore \# di origine, dove \# specifica il numero del campionatore di trama da campionare.</span><span class="sxs-lookup"><span data-stu-id="3f09b-111">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="3f09b-112">Il campionatore è associato a una trama e a uno stato del controllo definito dall'enumerazione [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (es.</span><span class="sxs-lookup"><span data-stu-id="3f09b-112">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (ex.</span></span> <span data-ttu-id="3f09b-113">D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="3f09b-113">D3DSAMP\_MINFILTER).</span></span>
-   <span data-ttu-id="3f09b-114">src2 è un registro di origine di input che specifica la sfumatura x.</span><span class="sxs-lookup"><span data-stu-id="3f09b-114">src2 is an input source register that specifies the x gradient.</span></span>
-   <span data-ttu-id="3f09b-115">src3 è un registro di origine di input che specifica la sfumatura y.</span><span class="sxs-lookup"><span data-stu-id="3f09b-115">src3 is an input source register that specifies the y gradient.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f09b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f09b-116">Remarks</span></span>



| <span data-ttu-id="3f09b-117">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3f09b-117">Pixel shader versions</span></span> | <span data-ttu-id="3f09b-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="3f09b-118">1\_1</span></span> | <span data-ttu-id="3f09b-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="3f09b-119">1\_2</span></span> | <span data-ttu-id="3f09b-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3f09b-120">1\_3</span></span> | <span data-ttu-id="3f09b-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="3f09b-121">1\_4</span></span> | <span data-ttu-id="3f09b-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f09b-122">2\_0</span></span> | <span data-ttu-id="3f09b-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3f09b-123">2\_x</span></span> | <span data-ttu-id="3f09b-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3f09b-124">2\_sw</span></span> | <span data-ttu-id="3f09b-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f09b-125">3\_0</span></span> | <span data-ttu-id="3f09b-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3f09b-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3f09b-127">texldd</span><span class="sxs-lookup"><span data-stu-id="3f09b-127">texldd</span></span>                |      |      |      |      |      | <span data-ttu-id="3f09b-128">x \*</span><span class="sxs-lookup"><span data-stu-id="3f09b-128">x \*</span></span> | <span data-ttu-id="3f09b-129">x</span><span class="sxs-lookup"><span data-stu-id="3f09b-129">x</span></span>     | <span data-ttu-id="3f09b-130">x</span><span class="sxs-lookup"><span data-stu-id="3f09b-130">x</span></span>    | <span data-ttu-id="3f09b-131">x</span><span class="sxs-lookup"><span data-stu-id="3f09b-131">x</span></span>     |



 

<span data-ttu-id="3f09b-132">\* Questa istruzione è supportata solo da PS \_ 2 \_ a.</span><span class="sxs-lookup"><span data-stu-id="3f09b-132">\* This instruction is only supported by ps\_2\_a.</span></span> <span data-ttu-id="3f09b-133">Non è supportato da PS \_ 2 \_ b.</span><span class="sxs-lookup"><span data-stu-id="3f09b-133">It is not supported by ps\_2\_b.</span></span> <span data-ttu-id="3f09b-134">Per ulteriori informazioni sui profili, vedere [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="3f09b-134">For more information about profiles, see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span></span>

<span data-ttu-id="3f09b-135">Questa istruzione esegue il campionamento di una trama usando le coordinate di trama in src0, il campionatore specificato da src1 e le sfumature DSX e DSY provenienti da src2 e src3.</span><span class="sxs-lookup"><span data-stu-id="3f09b-135">This instruction samples a texture using the texture coordinates at src0, the sampler specified by src1, and the gradients DSX and DSY coming from src2 and src3.</span></span> <span data-ttu-id="3f09b-136">I valori delle sfumature x e y vengono usati per selezionare il livello di mipmap appropriato della trama per il campionamento.</span><span class="sxs-lookup"><span data-stu-id="3f09b-136">The x and y gradient values are used to select the appropriate mipmap level of the texture for sampling.</span></span>

<span data-ttu-id="3f09b-137">Tutte le origini supportano swizzles arbitrario.</span><span class="sxs-lookup"><span data-stu-id="3f09b-137">All sources support arbitrary swizzles.</span></span>

<span data-ttu-id="3f09b-138">Tutte le maschere di scrittura sono valide nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="3f09b-138">All write masks are valid on the destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f09b-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f09b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f09b-140">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3f09b-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 