---
title: tex2Dbias
description: Esegue il campionamento di una trama 2D dopo la distorsione del livello MIP per t.w.
ms.assetid: adf2891a-732a-4953-875b-df315c19748b
keywords:
- HLSL tex2Dbias
topic_type:
- apiref
api_name:
- tex2Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cfaec24e1d188460d36a24d68b0fde8ddcb45c29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338846"
---
# <a name="tex2dbias"></a><span data-ttu-id="a185e-104">tex2Dbias</span><span class="sxs-lookup"><span data-stu-id="a185e-104">tex2Dbias</span></span>

<span data-ttu-id="a185e-105">Esegue il campionamento di una trama 2D dopo la distorsione del livello MIP per t.w.</span><span class="sxs-lookup"><span data-stu-id="a185e-105">Samples a 2D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="a185e-106">tex2Dbias RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="a185e-106">ret tex2Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="a185e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a185e-107">Parameters</span></span>



| <span data-ttu-id="a185e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a185e-108">Item</span></span>                                                   | <span data-ttu-id="a185e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a185e-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="a185e-110"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="a185e-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="a185e-111">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="a185e-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="a185e-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="a185e-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="a185e-113">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="a185e-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a185e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a185e-114">Return Value</span></span>

<span data-ttu-id="a185e-115">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="a185e-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="a185e-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="a185e-116">Type Description</span></span>



| <span data-ttu-id="a185e-117">Nome</span><span class="sxs-lookup"><span data-stu-id="a185e-117">Name</span></span> | <span data-ttu-id="a185e-118">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="a185e-118">In/Out</span></span> | [<span data-ttu-id="a185e-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="a185e-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="a185e-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="a185e-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a185e-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a185e-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="a185e-122">s</span><span class="sxs-lookup"><span data-stu-id="a185e-122">s</span></span>    | <span data-ttu-id="a185e-123">in ingresso</span><span class="sxs-lookup"><span data-stu-id="a185e-123">in</span></span>     | [<span data-ttu-id="a185e-124">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="a185e-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="a185e-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="a185e-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="a185e-126">1</span><span class="sxs-lookup"><span data-stu-id="a185e-126">1</span></span>    |
| <span data-ttu-id="a185e-127">u</span><span class="sxs-lookup"><span data-stu-id="a185e-127">t</span></span>    | <span data-ttu-id="a185e-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="a185e-128">in</span></span>     | [<span data-ttu-id="a185e-129">**vettore**</span><span class="sxs-lookup"><span data-stu-id="a185e-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="a185e-130">**float**</span><span class="sxs-lookup"><span data-stu-id="a185e-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a185e-131">4</span><span class="sxs-lookup"><span data-stu-id="a185e-131">4</span></span>    |
| <span data-ttu-id="a185e-132">RET</span><span class="sxs-lookup"><span data-stu-id="a185e-132">ret</span></span>  | <span data-ttu-id="a185e-133">in uscita</span><span class="sxs-lookup"><span data-stu-id="a185e-133">out</span></span>    | [<span data-ttu-id="a185e-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="a185e-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="a185e-135">**float**</span><span class="sxs-lookup"><span data-stu-id="a185e-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a185e-136">4</span><span class="sxs-lookup"><span data-stu-id="a185e-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a185e-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a185e-137">Minimum Shader Model</span></span>

<span data-ttu-id="a185e-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="a185e-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a185e-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a185e-139">Shader Model</span></span>                                              | <span data-ttu-id="a185e-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="a185e-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="a185e-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="a185e-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a185e-142">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="a185e-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="a185e-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a185e-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a185e-144">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="a185e-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="a185e-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a185e-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a185e-146">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="a185e-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="a185e-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a185e-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a185e-148">no</span><span class="sxs-lookup"><span data-stu-id="a185e-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="a185e-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a185e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a185e-150">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a185e-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

