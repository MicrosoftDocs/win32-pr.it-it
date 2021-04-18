---
title: tex1Dbias
description: Campiona una trama 1D dopo aver polarizzato il livello MIP per t.w.
ms.assetid: 2619ae23-e4b2-4699-b2ac-5ee711f9569a
keywords:
- HLSL tex1Dbias
topic_type:
- apiref
api_name:
- tex1Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0328b9328a1406177fa26bd566c0fbf7d384db63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117930"
---
# <a name="tex1dbias"></a><span data-ttu-id="e8b5b-104">tex1Dbias</span><span class="sxs-lookup"><span data-stu-id="e8b5b-104">tex1Dbias</span></span>

<span data-ttu-id="e8b5b-105">Campiona una trama 1D dopo aver polarizzato il livello MIP per t.w.</span><span class="sxs-lookup"><span data-stu-id="e8b5b-105">Samples a 1D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="e8b5b-106">tex1Dbias RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="e8b5b-106">ret tex1Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="e8b5b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8b5b-107">Parameters</span></span>



| <span data-ttu-id="e8b5b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e8b5b-108">Item</span></span>                                                   | <span data-ttu-id="e8b5b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8b5b-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="e8b5b-110"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="e8b5b-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="e8b5b-111">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="e8b5b-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="e8b5b-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="e8b5b-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="e8b5b-113">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="e8b5b-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e8b5b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8b5b-114">Return Value</span></span>

<span data-ttu-id="e8b5b-115">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="e8b5b-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="e8b5b-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="e8b5b-116">Type Description</span></span>



| <span data-ttu-id="e8b5b-117">Nome</span><span class="sxs-lookup"><span data-stu-id="e8b5b-117">Name</span></span> | <span data-ttu-id="e8b5b-118">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="e8b5b-118">In/Out</span></span> | [<span data-ttu-id="e8b5b-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="e8b5b-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="e8b5b-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="e8b5b-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e8b5b-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e8b5b-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="e8b5b-122">s</span><span class="sxs-lookup"><span data-stu-id="e8b5b-122">s</span></span>    | <span data-ttu-id="e8b5b-123">in ingresso</span><span class="sxs-lookup"><span data-stu-id="e8b5b-123">in</span></span>     | [<span data-ttu-id="e8b5b-124">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="e8b5b-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e8b5b-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="e8b5b-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="e8b5b-126">1</span><span class="sxs-lookup"><span data-stu-id="e8b5b-126">1</span></span>    |
| <span data-ttu-id="e8b5b-127">u</span><span class="sxs-lookup"><span data-stu-id="e8b5b-127">t</span></span>    | <span data-ttu-id="e8b5b-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="e8b5b-128">in</span></span>     | [<span data-ttu-id="e8b5b-129">**vettore**</span><span class="sxs-lookup"><span data-stu-id="e8b5b-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e8b5b-130">**float**</span><span class="sxs-lookup"><span data-stu-id="e8b5b-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e8b5b-131">4</span><span class="sxs-lookup"><span data-stu-id="e8b5b-131">4</span></span>    |
| <span data-ttu-id="e8b5b-132">RET</span><span class="sxs-lookup"><span data-stu-id="e8b5b-132">ret</span></span>  | <span data-ttu-id="e8b5b-133">in uscita</span><span class="sxs-lookup"><span data-stu-id="e8b5b-133">out</span></span>    | [<span data-ttu-id="e8b5b-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="e8b5b-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e8b5b-135">**float**</span><span class="sxs-lookup"><span data-stu-id="e8b5b-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e8b5b-136">4</span><span class="sxs-lookup"><span data-stu-id="e8b5b-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e8b5b-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e8b5b-137">Minimum Shader Model</span></span>

<span data-ttu-id="e8b5b-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8b5b-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e8b5b-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e8b5b-139">Shader Model</span></span>                                              | <span data-ttu-id="e8b5b-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="e8b5b-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="e8b5b-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="e8b5b-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e8b5b-142">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="e8b5b-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="e8b5b-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8b5b-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e8b5b-144">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="e8b5b-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="e8b5b-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8b5b-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e8b5b-146">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="e8b5b-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="e8b5b-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8b5b-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e8b5b-148">no</span><span class="sxs-lookup"><span data-stu-id="e8b5b-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="e8b5b-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8b5b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b5b-150">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e8b5b-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

