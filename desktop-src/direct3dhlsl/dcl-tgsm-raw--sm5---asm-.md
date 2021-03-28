---
title: dcl_tgsm_raw (SM5-ASM)
description: Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread compute shader.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719465"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a><span data-ttu-id="eeef1-103">\_RAW DCL TGSM \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="eeef1-103">dcl\_tgsm\_raw (sm5 - asm)</span></span>

<span data-ttu-id="eeef1-104">Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread compute shader.</span><span class="sxs-lookup"><span data-stu-id="eeef1-104">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span>



| <span data-ttu-id="eeef1-105">DCL \_ TGSM \_ RAW g \# , GetByteCount</span><span class="sxs-lookup"><span data-stu-id="eeef1-105">dcl\_tgsm\_raw g\#, byteCount</span></span> |
|-------------------------------|



 



| <span data-ttu-id="eeef1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="eeef1-106">Item</span></span>                                                                                                       | <span data-ttu-id="eeef1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeef1-107">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeef1-108"><span id="g_"></span><span id="G_"></span>*g\#*</span><span class="sxs-lookup"><span data-stu-id="eeef1-108"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                 | <span data-ttu-id="eeef1-109">\[in \] un riferimento a un blocco di dimensioni  non tipizzate della memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="eeef1-109">\[in\] A reference to a block of size *byteCount* of untyped shared memory.</span></span> <br/> |
| <span data-ttu-id="eeef1-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span><span class="sxs-lookup"><span data-stu-id="eeef1-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span></span><br/> | <span data-ttu-id="eeef1-111">\[in \] deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="eeef1-111">\[in\] Must be a multiple of 4.</span></span> <br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="eeef1-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="eeef1-112">Remarks</span></span>

<span data-ttu-id="eeef1-113">Lo spazio di archiviazione totale per tutti i g \# deve essere <= la quantità di memoria condivisa disponibile per ogni gruppo di thread, ovvero 32 KB.</span><span class="sxs-lookup"><span data-stu-id="eeef1-113">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB.</span></span>

<span data-ttu-id="eeef1-114">In un caso estremo, è possibile dichiarare il totale di 8192 g \# s, ognuno  con un valore di i/o di 4.</span><span class="sxs-lookup"><span data-stu-id="eeef1-114">In an extreme case, you can declare 8192 total g\# s, each with a *byteCount* of 4.</span></span>

<span data-ttu-id="eeef1-115">Nell'estremo opposto è possibile dichiarare un singolo g \# con un valore di  32768.</span><span class="sxs-lookup"><span data-stu-id="eeef1-115">In the opposite extreme, you can declare a single g\# with a *byteCount* of 32768.</span></span>

> [!Note]  
> <span data-ttu-id="eeef1-116">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano [DCL \_ TGSM \_ strutturate](dcl-tgsm-structured--sm5---asm-.md), ma **non \_ TGSM DCL \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="eeef1-116">cs\_4\_0 and cs\_4\_1 supports [dcl\_tgsm\_structured](dcl-tgsm-structured--sm5---asm-.md), but not **dcl\_tgsm\_raw**.</span></span>

 

<span data-ttu-id="eeef1-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="eeef1-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eeef1-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="eeef1-118">Vertex</span></span> | <span data-ttu-id="eeef1-119">Hull</span><span class="sxs-lookup"><span data-stu-id="eeef1-119">Hull</span></span> | <span data-ttu-id="eeef1-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="eeef1-120">Domain</span></span> | <span data-ttu-id="eeef1-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="eeef1-121">Geometry</span></span> | <span data-ttu-id="eeef1-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="eeef1-122">Pixel</span></span> | <span data-ttu-id="eeef1-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="eeef1-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="eeef1-124">X</span><span class="sxs-lookup"><span data-stu-id="eeef1-124">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eeef1-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="eeef1-125">Minimum Shader Model</span></span>

<span data-ttu-id="eeef1-126">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="eeef1-126">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="eeef1-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="eeef1-127">Shader Model</span></span>                                              | <span data-ttu-id="eeef1-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="eeef1-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eeef1-129">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="eeef1-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eeef1-130">sì</span><span class="sxs-lookup"><span data-stu-id="eeef1-130">yes</span></span>       |
| [<span data-ttu-id="eeef1-131">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="eeef1-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eeef1-132">no</span><span class="sxs-lookup"><span data-stu-id="eeef1-132">no</span></span>        |
| [<span data-ttu-id="eeef1-133">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="eeef1-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eeef1-134">no</span><span class="sxs-lookup"><span data-stu-id="eeef1-134">no</span></span>        |
| [<span data-ttu-id="eeef1-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eeef1-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eeef1-136">no</span><span class="sxs-lookup"><span data-stu-id="eeef1-136">no</span></span>        |
| [<span data-ttu-id="eeef1-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eeef1-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eeef1-138">no</span><span class="sxs-lookup"><span data-stu-id="eeef1-138">no</span></span>        |
| [<span data-ttu-id="eeef1-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eeef1-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eeef1-140">no</span><span class="sxs-lookup"><span data-stu-id="eeef1-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eeef1-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eeef1-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeef1-142">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eeef1-142">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





