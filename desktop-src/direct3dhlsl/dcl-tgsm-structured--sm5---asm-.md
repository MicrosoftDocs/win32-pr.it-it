---
title: dcl_tgsm_structured (SM5-ASM)
description: Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread compute shader. La memoria viene visualizzata come una matrice di strutture.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993040"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a><span data-ttu-id="815ef-104">\_ \_ strutturato DCL TGSM (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="815ef-104">dcl\_tgsm\_structured (sm5 - asm)</span></span>

<span data-ttu-id="815ef-105">Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread compute shader.</span><span class="sxs-lookup"><span data-stu-id="815ef-105">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span> <span data-ttu-id="815ef-106">La memoria viene visualizzata come una matrice di strutture.</span><span class="sxs-lookup"><span data-stu-id="815ef-106">The memory is viewed as an array of structures.</span></span>



| <span data-ttu-id="815ef-107">DCL \_ TGSM \_ strutturato g \# , structByteStride, structCount</span><span class="sxs-lookup"><span data-stu-id="815ef-107">dcl\_tgsm\_structured g\#, structByteStride, structCount</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="815ef-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="815ef-108">Item</span></span>                                                                                                                                   | <span data-ttu-id="815ef-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="815ef-109">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="815ef-110"><span id="g_"></span><span id="G_"></span>*g\#*</span><span class="sxs-lookup"><span data-stu-id="815ef-110"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                                             | <span data-ttu-id="815ef-111">\[in \] un riferimento a un blocco di memoria condivisa di dimensioni *structByteStride* \* *structCount* byte.</span><span class="sxs-lookup"><span data-stu-id="815ef-111">\[in\] A reference to a block of shared memory of size *structByteStride* \* *structCount* bytes.</span></span> <br/> |
| <span data-ttu-id="815ef-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="815ef-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="815ef-113">\[nello \] stride della struttura.</span><span class="sxs-lookup"><span data-stu-id="815ef-113">\[in\] The structure stride.</span></span> <span data-ttu-id="815ef-114">Questo valore è un uint in byte e deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="815ef-114">This value is a uint in bytes and must be a multiple of 4.</span></span> <br/>           |
| <span data-ttu-id="815ef-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span><span class="sxs-lookup"><span data-stu-id="815ef-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span></span><br/>                     | <span data-ttu-id="815ef-116">\[nel \] numero di strutture.</span><span class="sxs-lookup"><span data-stu-id="815ef-116">\[in\] The number of structures.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="815ef-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="815ef-117">Remarks</span></span>

<span data-ttu-id="815ef-118">Lo spazio di archiviazione totale per tutte le g \# deve essere <= la quantità di memoria condivisa disponibile per gruppo di thread, ovvero 32 KB, o scalari a 8192 32 bit.</span><span class="sxs-lookup"><span data-stu-id="815ef-118">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB, or 8192 32-bit scalars.</span></span>

<span data-ttu-id="815ef-119">In un caso estremo, è possibile dichiarare il totale di 8192 g \# s, se ogni *structByteStride* ha un valore pari a 4 e un *structCount* di 1.</span><span class="sxs-lookup"><span data-stu-id="815ef-119">In an extreme case, you can declare 8192 total g\# s, if each has a *structByteStride* of 4 and a *structCount* of 1.</span></span>

<span data-ttu-id="815ef-120">Nell'estremo opposto è possibile dichiarare un singolo g \# con uno stride della struttura di 32 KB e un conteggio di struttura pari a 1.</span><span class="sxs-lookup"><span data-stu-id="815ef-120">In the opposite extreme, you can declare a single g\# with a structure stride of 32kB and a structure count of 1.</span></span>

<span data-ttu-id="815ef-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="815ef-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="815ef-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="815ef-122">Vertex</span></span> | <span data-ttu-id="815ef-123">Hull</span><span class="sxs-lookup"><span data-stu-id="815ef-123">Hull</span></span> | <span data-ttu-id="815ef-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="815ef-124">Domain</span></span> | <span data-ttu-id="815ef-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="815ef-125">Geometry</span></span> | <span data-ttu-id="815ef-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="815ef-126">Pixel</span></span> | <span data-ttu-id="815ef-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="815ef-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="815ef-128">X</span><span class="sxs-lookup"><span data-stu-id="815ef-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="815ef-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="815ef-129">Minimum Shader Model</span></span>

<span data-ttu-id="815ef-130">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="815ef-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="815ef-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="815ef-131">Shader Model</span></span>                                              | <span data-ttu-id="815ef-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="815ef-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="815ef-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="815ef-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="815ef-134">sì</span><span class="sxs-lookup"><span data-stu-id="815ef-134">yes</span></span>       |
| [<span data-ttu-id="815ef-135">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="815ef-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="815ef-136">no</span><span class="sxs-lookup"><span data-stu-id="815ef-136">no</span></span>        |
| [<span data-ttu-id="815ef-137">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="815ef-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="815ef-138">no</span><span class="sxs-lookup"><span data-stu-id="815ef-138">no</span></span>        |
| [<span data-ttu-id="815ef-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="815ef-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="815ef-140">no</span><span class="sxs-lookup"><span data-stu-id="815ef-140">no</span></span>        |
| [<span data-ttu-id="815ef-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="815ef-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="815ef-142">no</span><span class="sxs-lookup"><span data-stu-id="815ef-142">no</span></span>        |
| [<span data-ttu-id="815ef-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="815ef-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="815ef-144">no</span><span class="sxs-lookup"><span data-stu-id="815ef-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="815ef-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="815ef-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="815ef-146">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="815ef-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





