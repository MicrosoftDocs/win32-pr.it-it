---
title: sample_b (SM4-ASM)
description: Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato. | sample_b (SM4-ASM)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234827"
---
# <a name="sample_b-sm4---asm"></a><span data-ttu-id="2ebf1-104">esempio \_ b (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2ebf1-104">sample\_b (sm4 - asm)</span></span>

<span data-ttu-id="2ebf1-105">Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="2ebf1-106">esempio \_ b \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcLODBias. Select \_ Component</span><span class="sxs-lookup"><span data-stu-id="2ebf1-106">sample\_b\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLODBias.select\_component</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2ebf1-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="2ebf1-107">Item</span></span>                                                                                                               | <span data-ttu-id="2ebf1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ebf1-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ebf1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2ebf1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="2ebf1-110">\[nell' \] indirizzo del risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-110">\[in\] The address of the result of the operation.</span></span><br/>                                                              |
| <span data-ttu-id="2ebf1-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="2ebf1-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="2ebf1-112">\[in \] un set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="2ebf1-113">Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="2ebf1-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="2ebf1-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="2ebf1-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="2ebf1-115">\[in \] un registro di trama.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-115">\[in\] A texture register.</span></span> <span data-ttu-id="2ebf1-116">Per ulteriori informazioni, vedere l'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="2ebf1-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="2ebf1-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="2ebf1-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="2ebf1-118">\[in \] un registro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-118">\[in\] A sampler register.</span></span> <span data-ttu-id="2ebf1-119">Per ulteriori informazioni, vedere l'istruzione di **esempio** .</span><span class="sxs-lookup"><span data-stu-id="2ebf1-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="2ebf1-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span><span class="sxs-lookup"><span data-stu-id="2ebf1-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span></span><br/>     | <span data-ttu-id="2ebf1-121">\[\]per informazioni su questo parametro, vedere la sezione **osservazioni** .</span><span class="sxs-lookup"><span data-stu-id="2ebf1-121">\[in\] See the **Remarks** section for information about this parameter.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="2ebf1-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ebf1-122">Remarks</span></span>

<span data-ttu-id="2ebf1-123">I dati di origine possono provenire da qualsiasi tipo di risorsa, ad eccezione dei buffer.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-123">The source data may come from any Resource Type, other than Buffers.</span></span> <span data-ttu-id="2ebf1-124">Viene applicata un'ulteriore distorsione al livello di dettaglio calcolato come parte dell'esecuzione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-124">An additional bias is applied to the level of detail computed as part of the instruction execution.</span></span>

<span data-ttu-id="2ebf1-125">Questa istruzione si comporta come l'istruzione di [esempio](sample--sm4---asm-.md) con l'aggiunta dell'applicazione del valore *srcLODBias* specificato al livello di dettaglio calcolato come parte dell'esecuzione dell'istruzione prima di selezionare le mappe MIP.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-125">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction with the addition of applying the specified *srcLODBias* value to the level of detail value computed as part of the instruction execution prior to selecting the mip map(s).</span></span> <span data-ttu-id="2ebf1-126">Il valore *srcLODBias* viene aggiunto all'oggetto LOD calcolato per ogni pixel, insieme al valore MipLODBias del campionatore, prima del morsetto a MinLOD e MaxLOD.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-126">The *srcLODBias* value is added to the computed LOD on a per-pixel basis, along with the sampler MipLODBias value, prior to the clamp to MinLOD and MaxLOD.</span></span>

### <a name="restrictions"></a><span data-ttu-id="2ebf1-127">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="2ebf1-127">Restrictions</span></span>

-   <span data-ttu-id="2ebf1-128">l' **esempio \_ b** eredita le stesse restrizioni dell'istruzione di [esempio](sample--sm4---asm-.md) , oltre alle restrizioni aggiuntive per il parametro aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-128">**sample\_b** inherits the same restrictions as the [sample](sample--sm4---asm-.md) instruction, plus additional restrictions for its additional parameter.</span></span>
-   <span data-ttu-id="2ebf1-129">L'intervallo di *srcLODBias* è (-16 f a 15.99 f); i valori al di fuori di questo intervallo produrranno risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-129">The range of *srcLODBias* is (-16.0f to 15.99f); values outside of this range will produce undefined results.</span></span>
-   <span data-ttu-id="2ebf1-130">*srcLODBias* deve usare un selettore di componente singolo se non è un controllo immediato scalare.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-130">*srcLODBias* must use a single component selector if it is not a scalar immediate.</span></span>

<span data-ttu-id="2ebf1-131">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ebf1-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2ebf1-132">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="2ebf1-132">Vertex Shader</span></span> | <span data-ttu-id="2ebf1-133">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="2ebf1-133">Geometry Shader</span></span> | <span data-ttu-id="2ebf1-134">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="2ebf1-134">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="2ebf1-135">x</span><span class="sxs-lookup"><span data-stu-id="2ebf1-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2ebf1-136">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2ebf1-136">Minimum Shader Model</span></span>

<span data-ttu-id="2ebf1-137">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="2ebf1-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2ebf1-138">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2ebf1-138">Shader Model</span></span>                                              | <span data-ttu-id="2ebf1-139">Supportato</span><span class="sxs-lookup"><span data-stu-id="2ebf1-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2ebf1-140">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2ebf1-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2ebf1-141">sì</span><span class="sxs-lookup"><span data-stu-id="2ebf1-141">yes</span></span>       |
| [<span data-ttu-id="2ebf1-142">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="2ebf1-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2ebf1-143">sì</span><span class="sxs-lookup"><span data-stu-id="2ebf1-143">yes</span></span>       |
| [<span data-ttu-id="2ebf1-144">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="2ebf1-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2ebf1-145">sì</span><span class="sxs-lookup"><span data-stu-id="2ebf1-145">yes</span></span>       |
| [<span data-ttu-id="2ebf1-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2ebf1-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2ebf1-147">no</span><span class="sxs-lookup"><span data-stu-id="2ebf1-147">no</span></span>        |
| [<span data-ttu-id="2ebf1-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2ebf1-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2ebf1-149">no</span><span class="sxs-lookup"><span data-stu-id="2ebf1-149">no</span></span>        |
| [<span data-ttu-id="2ebf1-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2ebf1-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2ebf1-151">no</span><span class="sxs-lookup"><span data-stu-id="2ebf1-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2ebf1-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ebf1-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ebf1-153">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2ebf1-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





