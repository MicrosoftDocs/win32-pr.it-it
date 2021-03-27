---
title: breakc (SM4-ASM)
description: Sposta in modo condizionale il punto di esecuzione nell'istruzione dopo il EndLoop o endswitch successivo.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398254"
---
# <a name="breakc-sm4---asm"></a><span data-ttu-id="9146b-103">breakc (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9146b-103">breakc (sm4 - asm)</span></span>

<span data-ttu-id="9146b-104">Sposta in modo condizionale il punto di esecuzione nell'istruzione dopo il [EndLoop](endloop--sm4---asm-.md) o [endswitch](endswitch--sm4---asm-.md)successivo.</span><span class="sxs-lookup"><span data-stu-id="9146b-104">Conditionally moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="9146b-105">breakc { \_ z </span><span class="sxs-lookup"><span data-stu-id="9146b-105">breakc{\_z</span></span>\|<span data-ttu-id="9146b-106">\_NZ} src0. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="9146b-106">\_nz} src0.select\_component</span></span> |
|------------------------------------------|



 



| <span data-ttu-id="9146b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="9146b-107">Item</span></span>                                                            | <span data-ttu-id="9146b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9146b-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9146b-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9146b-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9146b-110">\[nel \] componente su cui eseguire il test della condizione.</span><span class="sxs-lookup"><span data-stu-id="9146b-110">\[in\] The component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9146b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9146b-111">Remarks</span></span>

<span data-ttu-id="9146b-112">Il formato del token contiene l'offset dell'istruzione **EndLoop** corrispondente nello shader per praticità.</span><span class="sxs-lookup"><span data-stu-id="9146b-112">The token format contains the offset of the corresponding **endloop** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="9146b-113">Nell'esempio seguente viene illustrata l'istruzione **breakc** .</span><span class="sxs-lookup"><span data-stu-id="9146b-113">The following example shows the **breakc** instruction.</span></span>


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



<span data-ttu-id="9146b-114">Questa istruzione deve essere visualizzata all'interno di un **ciclo** / **EndLoop** o **Switch** / **endswitch**.</span><span class="sxs-lookup"><span data-stu-id="9146b-114">This instruction must appear within a **loop**/**endloop** or **switch**/**endswitch**.</span></span>

<span data-ttu-id="9146b-115">Il registro a 32 bit fornito da *src0* viene testato a livello di bit.</span><span class="sxs-lookup"><span data-stu-id="9146b-115">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="9146b-116">Se un bit è diverso da zero, **breakc \_ NZ** eseguirà l'operazione break.</span><span class="sxs-lookup"><span data-stu-id="9146b-116">If any bit is nonzero, **breakc\_nz** will perform the break.</span></span> <span data-ttu-id="9146b-117">Se tutti i bit sono zero, **breakc \_ z** eseguirà l'operazione break.</span><span class="sxs-lookup"><span data-stu-id="9146b-117">If all bits are zero, **breakc\_z** will perform the break.</span></span>

<span data-ttu-id="9146b-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9146b-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9146b-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="9146b-119">Vertex Shader</span></span> | <span data-ttu-id="9146b-120">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="9146b-120">Geometry Shader</span></span> | <span data-ttu-id="9146b-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="9146b-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9146b-122">x</span><span class="sxs-lookup"><span data-stu-id="9146b-122">x</span></span>             | <span data-ttu-id="9146b-123">x</span><span class="sxs-lookup"><span data-stu-id="9146b-123">x</span></span>               | <span data-ttu-id="9146b-124">x</span><span class="sxs-lookup"><span data-stu-id="9146b-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9146b-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="9146b-125">Minimum Shader Model</span></span>

<span data-ttu-id="9146b-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9146b-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9146b-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="9146b-127">Shader Model</span></span>                                              | <span data-ttu-id="9146b-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="9146b-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9146b-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9146b-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9146b-130">sì</span><span class="sxs-lookup"><span data-stu-id="9146b-130">yes</span></span>       |
| [<span data-ttu-id="9146b-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="9146b-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9146b-132">sì</span><span class="sxs-lookup"><span data-stu-id="9146b-132">yes</span></span>       |
| [<span data-ttu-id="9146b-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="9146b-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9146b-134">sì</span><span class="sxs-lookup"><span data-stu-id="9146b-134">yes</span></span>       |
| [<span data-ttu-id="9146b-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9146b-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9146b-136">no</span><span class="sxs-lookup"><span data-stu-id="9146b-136">no</span></span>        |
| [<span data-ttu-id="9146b-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9146b-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9146b-138">no</span><span class="sxs-lookup"><span data-stu-id="9146b-138">no</span></span>        |
| [<span data-ttu-id="9146b-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9146b-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9146b-140">no</span><span class="sxs-lookup"><span data-stu-id="9146b-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9146b-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9146b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9146b-142">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9146b-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





