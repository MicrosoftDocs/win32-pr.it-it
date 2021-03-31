---
title: firstbit (SM5-ASM)
description: Trova il primo bit impostato in un numero, sia da LSB che da MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335623"
---
# <a name="firstbit-sm5---asm"></a><span data-ttu-id="6b2d5-103">firstbit (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6b2d5-103">firstbit (sm5 - asm)</span></span>

<span data-ttu-id="6b2d5-104">Trova il primo bit impostato in un numero, sia da LSB che da MSB.</span><span class="sxs-lookup"><span data-stu-id="6b2d5-104">Finds the first bit set in a number, either from LSB or MSB.</span></span>



| <span data-ttu-id="6b2d5-105">firstbit { \_ Hi </span><span class="sxs-lookup"><span data-stu-id="6b2d5-105">firstbit{\_hi</span></span>\|<span data-ttu-id="6b2d5-106">\_lo</span><span class="sxs-lookup"><span data-stu-id="6b2d5-106">\_lo\</span></span>|<span data-ttu-id="6b2d5-107">\_Shi} dest \[ . mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6b2d5-107">\_shi} dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="6b2d5-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6b2d5-108">Item</span></span>                                                            | <span data-ttu-id="6b2d5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b2d5-109">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2d5-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6b2d5-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6b2d5-111">\[nella \] posizione integer del primo bit impostato in *src0* a partire da LSB per FIRSTBIT \_ lo o MSB per firstbit \_ Hi.</span><span class="sxs-lookup"><span data-stu-id="6b2d5-111">\[in\] The integer position of the first bit set in *src0* starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span><br/> |
| <span data-ttu-id="6b2d5-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6b2d5-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6b2d5-113">\[nell' \] Integer di input.</span><span class="sxs-lookup"><span data-stu-id="6b2d5-113">\[in\] The input integer.</span></span><br/>                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="6b2d5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b2d5-114">Remarks</span></span>

<span data-ttu-id="6b2d5-115">Questa operazione restituisce la posizione integer del primo bit impostato nell'input a 32 bit a partire da LSB per firstbit \_ lo o MSB per firstbit \_ Hi.</span><span class="sxs-lookup"><span data-stu-id="6b2d5-115">This operation returns the integer position of the first bit set in the 32-bit input starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span> <span data-ttu-id="6b2d5-116">Ad esempio \_ , firstbit lo in 0x00000001 restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="6b2d5-116">For example firstbit\_lo on 0x00000001 returns 0.</span></span> <span data-ttu-id="6b2d5-117">firstbit \_ Hi on 0x10000000 restituisce 3.</span><span class="sxs-lookup"><span data-stu-id="6b2d5-117">firstbit\_hi on 0x10000000 returns 3.</span></span>

<span data-ttu-id="6b2d5-118">firstbit \_ Shi (s per Signed) restituisce il primo 0 da MSB se il numero è negativo. in caso contrario, restituisce il primo 1 da MSB.</span><span class="sxs-lookup"><span data-stu-id="6b2d5-118">firstbit\_shi (s for signed) returns the first 0 from the MSB if the number is negative; otherwise it returns the first 1 from the MSB.</span></span>

<span data-ttu-id="6b2d5-119">Tutte le varianti dell'istruzione restituiscono ~ 0 (0xFFFFFFFF nel registro a 32 bit) se non viene trovata alcuna corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="6b2d5-119">All variants of the instruction return ~0 (0xffffffff in 32-bit register) if no match is found.</span></span>

<span data-ttu-id="6b2d5-120">Usare questa istruzione per enumerare rapidamente i bit impostati in un bit o trovare la maggiore potenza di 2 in un numero.</span><span class="sxs-lookup"><span data-stu-id="6b2d5-120">Use this instruction to quickly enumerate set bits in a bitfield, or find the largest power of 2 in a number.</span></span>

<span data-ttu-id="6b2d5-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b2d5-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6b2d5-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="6b2d5-122">Vertex</span></span> | <span data-ttu-id="6b2d5-123">Hull</span><span class="sxs-lookup"><span data-stu-id="6b2d5-123">Hull</span></span> | <span data-ttu-id="6b2d5-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="6b2d5-124">Domain</span></span> | <span data-ttu-id="6b2d5-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="6b2d5-125">Geometry</span></span> | <span data-ttu-id="6b2d5-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="6b2d5-126">Pixel</span></span> | <span data-ttu-id="6b2d5-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="6b2d5-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6b2d5-128">X</span><span class="sxs-lookup"><span data-stu-id="6b2d5-128">X</span></span>      | <span data-ttu-id="6b2d5-129">X</span><span class="sxs-lookup"><span data-stu-id="6b2d5-129">X</span></span>    | <span data-ttu-id="6b2d5-130">X</span><span class="sxs-lookup"><span data-stu-id="6b2d5-130">X</span></span>      | <span data-ttu-id="6b2d5-131">X</span><span class="sxs-lookup"><span data-stu-id="6b2d5-131">X</span></span>        | <span data-ttu-id="6b2d5-132">X</span><span class="sxs-lookup"><span data-stu-id="6b2d5-132">X</span></span>     | <span data-ttu-id="6b2d5-133">X</span><span class="sxs-lookup"><span data-stu-id="6b2d5-133">X</span></span>       |



 

## <a name="mimimum-shader-model"></a><span data-ttu-id="6b2d5-134">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="6b2d5-134">Mimimum Shader Model</span></span>

<span data-ttu-id="6b2d5-135">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b2d5-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6b2d5-136">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="6b2d5-136">Shader Model</span></span>                                              | <span data-ttu-id="6b2d5-137">Supportato</span><span class="sxs-lookup"><span data-stu-id="6b2d5-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6b2d5-138">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="6b2d5-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6b2d5-139">sì</span><span class="sxs-lookup"><span data-stu-id="6b2d5-139">yes</span></span>       |
| [<span data-ttu-id="6b2d5-140">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="6b2d5-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6b2d5-141">no</span><span class="sxs-lookup"><span data-stu-id="6b2d5-141">no</span></span>        |
| [<span data-ttu-id="6b2d5-142">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="6b2d5-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6b2d5-143">no</span><span class="sxs-lookup"><span data-stu-id="6b2d5-143">no</span></span>        |
| [<span data-ttu-id="6b2d5-144">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b2d5-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6b2d5-145">no</span><span class="sxs-lookup"><span data-stu-id="6b2d5-145">no</span></span>        |
| [<span data-ttu-id="6b2d5-146">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b2d5-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6b2d5-147">no</span><span class="sxs-lookup"><span data-stu-id="6b2d5-147">no</span></span>        |
| [<span data-ttu-id="6b2d5-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b2d5-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6b2d5-149">no</span><span class="sxs-lookup"><span data-stu-id="6b2d5-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6b2d5-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b2d5-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b2d5-151">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b2d5-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





