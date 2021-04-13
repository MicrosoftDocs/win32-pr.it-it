---
title: tex3Dlod
description: Campiona una trama 3D con mipmap. Il mipmap LOD è specificato in t.w.
ms.assetid: 9bdd8fa1-8c02-4765-8f4d-61ceb532354e
keywords:
- HLSL tex3Dlod
topic_type:
- apiref
api_name:
- tex3Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc25af449f7f32e94d4ca344bf5ef3a4d09b376c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976666"
---
# <a name="tex3dlod"></a><span data-ttu-id="5e4e4-105">tex3Dlod</span><span class="sxs-lookup"><span data-stu-id="5e4e4-105">tex3Dlod</span></span>

<span data-ttu-id="5e4e4-106">Campiona una trama 3D con mipmap.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-106">Samples a 3D texture with mipmaps.</span></span> <span data-ttu-id="5e4e4-107">Il mipmap LOD è specificato in t.w.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="5e4e4-108">tex3Dlod RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="5e4e4-108">ret tex3Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="5e4e4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e4e4-109">Parameters</span></span>



| <span data-ttu-id="5e4e4-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="5e4e4-110">Item</span></span>                                                   | <span data-ttu-id="5e4e4-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e4e4-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="5e4e4-112"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="5e4e4-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="5e4e4-113">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="5e4e4-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="5e4e4-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="5e4e4-115">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5e4e4-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e4e4-116">Return Value</span></span>

<span data-ttu-id="5e4e4-117">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="5e4e4-118">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="5e4e4-118">Type Description</span></span>



| <span data-ttu-id="5e4e4-119">Nome</span><span class="sxs-lookup"><span data-stu-id="5e4e4-119">Name</span></span> | <span data-ttu-id="5e4e4-120">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="5e4e4-120">In/Out</span></span> | [<span data-ttu-id="5e4e4-121">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="5e4e4-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="5e4e4-122">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="5e4e4-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="5e4e4-123">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5e4e4-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="5e4e4-124">s</span><span class="sxs-lookup"><span data-stu-id="5e4e4-124">s</span></span>    | <span data-ttu-id="5e4e4-125">in ingresso</span><span class="sxs-lookup"><span data-stu-id="5e4e4-125">in</span></span>     | [<span data-ttu-id="5e4e4-126">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="5e4e4-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5e4e4-127">sampler3D</span><span class="sxs-lookup"><span data-stu-id="5e4e4-127">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="5e4e4-128">1</span><span class="sxs-lookup"><span data-stu-id="5e4e4-128">1</span></span>    |
| <span data-ttu-id="5e4e4-129">u</span><span class="sxs-lookup"><span data-stu-id="5e4e4-129">t</span></span>    | <span data-ttu-id="5e4e4-130">in ingresso</span><span class="sxs-lookup"><span data-stu-id="5e4e4-130">in</span></span>     | [<span data-ttu-id="5e4e4-131">**vettore**</span><span class="sxs-lookup"><span data-stu-id="5e4e4-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5e4e4-132">**float**</span><span class="sxs-lookup"><span data-stu-id="5e4e4-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5e4e4-133">4</span><span class="sxs-lookup"><span data-stu-id="5e4e4-133">4</span></span>    |
| <span data-ttu-id="5e4e4-134">RET</span><span class="sxs-lookup"><span data-stu-id="5e4e4-134">ret</span></span>  | <span data-ttu-id="5e4e4-135">in uscita</span><span class="sxs-lookup"><span data-stu-id="5e4e4-135">out</span></span>    | [<span data-ttu-id="5e4e4-136">**vettore**</span><span class="sxs-lookup"><span data-stu-id="5e4e4-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5e4e4-137">**float**</span><span class="sxs-lookup"><span data-stu-id="5e4e4-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5e4e4-138">4</span><span class="sxs-lookup"><span data-stu-id="5e4e4-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5e4e4-139">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="5e4e4-139">Minimum Shader Model</span></span>

<span data-ttu-id="5e4e4-140">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="5e4e4-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5e4e4-141">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="5e4e4-141">Shader Model</span></span>                                              | <span data-ttu-id="5e4e4-142">Supportato</span><span class="sxs-lookup"><span data-stu-id="5e4e4-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="5e4e4-143">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="5e4e4-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5e4e4-144">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="5e4e4-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="5e4e4-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e4e4-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5e4e4-146">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="5e4e4-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="5e4e4-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e4e4-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5e4e4-148">no</span><span class="sxs-lookup"><span data-stu-id="5e4e4-148">no</span></span>                      |
| [<span data-ttu-id="5e4e4-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e4e4-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5e4e4-150">no</span><span class="sxs-lookup"><span data-stu-id="5e4e4-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="5e4e4-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e4e4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e4e4-152">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="5e4e4-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

