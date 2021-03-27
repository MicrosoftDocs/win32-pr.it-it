---
title: tex1Dlod
description: Campiona una trama 1D con mipmap. Il mipmap LOD è specificato in t.w.
ms.assetid: f1700ee6-2f79-4b8b-ad34-30561f319356
keywords:
- HLSL tex1Dlod
topic_type:
- apiref
api_name:
- tex1Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca6379448290d027bba8a8b62f80cac39c84f25
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729159"
---
# <a name="tex1dlod"></a><span data-ttu-id="26305-105">tex1Dlod</span><span class="sxs-lookup"><span data-stu-id="26305-105">tex1Dlod</span></span>

<span data-ttu-id="26305-106">Campiona una trama 1D con mipmap.</span><span class="sxs-lookup"><span data-stu-id="26305-106">Samples a 1D texture with mipmaps.</span></span> <span data-ttu-id="26305-107">Il mipmap LOD è specificato in t.w.</span><span class="sxs-lookup"><span data-stu-id="26305-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="26305-108">tex1Dlod RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="26305-108">ret tex1Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="26305-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="26305-109">Parameters</span></span>



| <span data-ttu-id="26305-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="26305-110">Item</span></span>                                                   | <span data-ttu-id="26305-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26305-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="26305-112"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="26305-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="26305-113">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="26305-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="26305-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="26305-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="26305-115">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="26305-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="26305-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26305-116">Return Value</span></span>

<span data-ttu-id="26305-117">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="26305-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="26305-118">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="26305-118">Type Description</span></span>



| <span data-ttu-id="26305-119">Nome</span><span class="sxs-lookup"><span data-stu-id="26305-119">Name</span></span> | <span data-ttu-id="26305-120">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="26305-120">In/Out</span></span> | [<span data-ttu-id="26305-121">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="26305-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="26305-122">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="26305-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="26305-123">Dimensione</span><span class="sxs-lookup"><span data-stu-id="26305-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="26305-124">s</span><span class="sxs-lookup"><span data-stu-id="26305-124">s</span></span>    | <span data-ttu-id="26305-125">in ingresso</span><span class="sxs-lookup"><span data-stu-id="26305-125">in</span></span>     | [<span data-ttu-id="26305-126">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="26305-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="26305-127">sampler1D</span><span class="sxs-lookup"><span data-stu-id="26305-127">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="26305-128">1</span><span class="sxs-lookup"><span data-stu-id="26305-128">1</span></span>    |
| <span data-ttu-id="26305-129">u</span><span class="sxs-lookup"><span data-stu-id="26305-129">t</span></span>    | <span data-ttu-id="26305-130">in ingresso</span><span class="sxs-lookup"><span data-stu-id="26305-130">in</span></span>     | [<span data-ttu-id="26305-131">**vettore**</span><span class="sxs-lookup"><span data-stu-id="26305-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="26305-132">**float**</span><span class="sxs-lookup"><span data-stu-id="26305-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="26305-133">4</span><span class="sxs-lookup"><span data-stu-id="26305-133">4</span></span>    |
| <span data-ttu-id="26305-134">RET</span><span class="sxs-lookup"><span data-stu-id="26305-134">ret</span></span>  | <span data-ttu-id="26305-135">in uscita</span><span class="sxs-lookup"><span data-stu-id="26305-135">out</span></span>    | [<span data-ttu-id="26305-136">**vettore**</span><span class="sxs-lookup"><span data-stu-id="26305-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="26305-137">**float**</span><span class="sxs-lookup"><span data-stu-id="26305-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="26305-138">4</span><span class="sxs-lookup"><span data-stu-id="26305-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="26305-139">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="26305-139">Minimum Shader Model</span></span>

<span data-ttu-id="26305-140">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="26305-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="26305-141">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="26305-141">Shader Model</span></span>                                              | <span data-ttu-id="26305-142">Supportato</span><span class="sxs-lookup"><span data-stu-id="26305-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="26305-143">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="26305-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="26305-144">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="26305-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="26305-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26305-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="26305-146">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="26305-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="26305-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26305-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="26305-148">no</span><span class="sxs-lookup"><span data-stu-id="26305-148">no</span></span>                      |
| [<span data-ttu-id="26305-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26305-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="26305-150">no</span><span class="sxs-lookup"><span data-stu-id="26305-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="26305-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26305-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26305-152">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="26305-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

