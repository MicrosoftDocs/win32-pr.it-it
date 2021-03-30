---
title: continuec (SM4-ASM)
description: Continua l'esecuzione in modo condizionale all'inizio del ciclo corrente.
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d480d8828f8f68af1f6a2ff4f52224041d5241df
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976367"
---
# <a name="continuec-sm4---asm"></a><span data-ttu-id="5449a-103">continuec (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5449a-103">continuec (sm4 - asm)</span></span>

<span data-ttu-id="5449a-104">Continua l'esecuzione in modo condizionale all'inizio del ciclo corrente.</span><span class="sxs-lookup"><span data-stu-id="5449a-104">Conditionally continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="5449a-105">continuec { \_ z </span><span class="sxs-lookup"><span data-stu-id="5449a-105">continuec{\_z</span></span>\|<span data-ttu-id="5449a-106">\_NZ} src0. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="5449a-106">\_nz} src0.select\_component</span></span> |
|---------------------------------------------|



 



| <span data-ttu-id="5449a-107">Termine</span><span class="sxs-lookup"><span data-stu-id="5449a-107">Term</span></span>                                                            | <span data-ttu-id="5449a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5449a-108">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="5449a-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5449a-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5449a-110">\[nel \] componente rispetto al quale testare la condizione.</span><span class="sxs-lookup"><span data-stu-id="5449a-110">\[in\] The component against which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5449a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5449a-111">Remarks</span></span>

<span data-ttu-id="5449a-112">**continuec** può essere utilizzato solo all'interno di un [ciclo](loop--sm4---asm-.md) o di [EndLoop](endloop--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="5449a-112">**continuec** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="5449a-113">Nell'esempio seguente viene illustrato come utilizzare l'istruzione **continuec** .</span><span class="sxs-lookup"><span data-stu-id="5449a-113">The following example shows how to use the **continuec** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



<span data-ttu-id="5449a-114">Il formato del token contiene l'offset dell'istruzione del ciclo corrispondente nello shader come praticità.</span><span class="sxs-lookup"><span data-stu-id="5449a-114">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="5449a-115">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="5449a-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5449a-116">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="5449a-116">Vertex Shader</span></span> | <span data-ttu-id="5449a-117">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="5449a-117">Geometry Shader</span></span> | <span data-ttu-id="5449a-118">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="5449a-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5449a-119">x</span><span class="sxs-lookup"><span data-stu-id="5449a-119">x</span></span>             | <span data-ttu-id="5449a-120">x</span><span class="sxs-lookup"><span data-stu-id="5449a-120">x</span></span>               | <span data-ttu-id="5449a-121">x</span><span class="sxs-lookup"><span data-stu-id="5449a-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5449a-122">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="5449a-122">Minimum Shader Model</span></span>

<span data-ttu-id="5449a-123">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="5449a-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5449a-124">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="5449a-124">Shader Model</span></span>                                              | <span data-ttu-id="5449a-125">Supportato</span><span class="sxs-lookup"><span data-stu-id="5449a-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5449a-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="5449a-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5449a-127">sì</span><span class="sxs-lookup"><span data-stu-id="5449a-127">yes</span></span>       |
| [<span data-ttu-id="5449a-128">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="5449a-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5449a-129">sì</span><span class="sxs-lookup"><span data-stu-id="5449a-129">yes</span></span>       |
| [<span data-ttu-id="5449a-130">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="5449a-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5449a-131">sì</span><span class="sxs-lookup"><span data-stu-id="5449a-131">yes</span></span>       |
| [<span data-ttu-id="5449a-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5449a-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5449a-133">no</span><span class="sxs-lookup"><span data-stu-id="5449a-133">no</span></span>        |
| [<span data-ttu-id="5449a-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5449a-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5449a-135">no</span><span class="sxs-lookup"><span data-stu-id="5449a-135">no</span></span>        |
| [<span data-ttu-id="5449a-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5449a-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5449a-137">no</span><span class="sxs-lookup"><span data-stu-id="5449a-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5449a-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5449a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5449a-139">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5449a-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





