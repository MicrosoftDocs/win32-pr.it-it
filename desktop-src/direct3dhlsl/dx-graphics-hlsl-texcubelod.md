---
title: texCUBElod
description: Campiona una trama del cubo con mipmap. Il mipmap LOD è specificato in t.w.
ms.assetid: fa7b236d-2c52-42bd-9123-919541f9e675
keywords:
- HLSL texCUBElod
topic_type:
- apiref
api_name:
- texCUBElod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72635211263085f03b87c2e013ea57d1b6a21464
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976839"
---
# <a name="texcubelod"></a><span data-ttu-id="b7142-105">texCUBElod</span><span class="sxs-lookup"><span data-stu-id="b7142-105">texCUBElod</span></span>

<span data-ttu-id="b7142-106">Campiona una trama del cubo con mipmap.</span><span class="sxs-lookup"><span data-stu-id="b7142-106">Samples a cube texture with mipmaps.</span></span> <span data-ttu-id="b7142-107">Il mipmap LOD è specificato in t.w.</span><span class="sxs-lookup"><span data-stu-id="b7142-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="b7142-108">texCUBElod RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="b7142-108">ret texCUBElod(s, t)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="b7142-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7142-109">Parameters</span></span>



| <span data-ttu-id="b7142-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b7142-110">Item</span></span>                                                   | <span data-ttu-id="b7142-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7142-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b7142-112"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="b7142-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="b7142-113">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="b7142-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="b7142-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="b7142-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="b7142-115">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="b7142-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b7142-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7142-116">Return Value</span></span>

<span data-ttu-id="b7142-117">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="b7142-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="b7142-118">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="b7142-118">Type Description</span></span>



| <span data-ttu-id="b7142-119">Nome</span><span class="sxs-lookup"><span data-stu-id="b7142-119">Name</span></span> | <span data-ttu-id="b7142-120">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="b7142-120">In/Out</span></span> | [<span data-ttu-id="b7142-121">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="b7142-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="b7142-122">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="b7142-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b7142-123">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b7142-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="b7142-124">s</span><span class="sxs-lookup"><span data-stu-id="b7142-124">s</span></span>    | <span data-ttu-id="b7142-125">in ingresso</span><span class="sxs-lookup"><span data-stu-id="b7142-125">in</span></span>     | [<span data-ttu-id="b7142-126">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="b7142-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b7142-127">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="b7142-127">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="b7142-128">1</span><span class="sxs-lookup"><span data-stu-id="b7142-128">1</span></span>    |
| <span data-ttu-id="b7142-129">u</span><span class="sxs-lookup"><span data-stu-id="b7142-129">t</span></span>    | <span data-ttu-id="b7142-130">in ingresso</span><span class="sxs-lookup"><span data-stu-id="b7142-130">in</span></span>     | [<span data-ttu-id="b7142-131">**vettore**</span><span class="sxs-lookup"><span data-stu-id="b7142-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b7142-132">**float**</span><span class="sxs-lookup"><span data-stu-id="b7142-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7142-133">4</span><span class="sxs-lookup"><span data-stu-id="b7142-133">4</span></span>    |
| <span data-ttu-id="b7142-134">RET</span><span class="sxs-lookup"><span data-stu-id="b7142-134">ret</span></span>  | <span data-ttu-id="b7142-135">in uscita</span><span class="sxs-lookup"><span data-stu-id="b7142-135">out</span></span>    | [<span data-ttu-id="b7142-136">**vettore**</span><span class="sxs-lookup"><span data-stu-id="b7142-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b7142-137">**float**</span><span class="sxs-lookup"><span data-stu-id="b7142-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7142-138">4</span><span class="sxs-lookup"><span data-stu-id="b7142-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b7142-139">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b7142-139">Minimum Shader Model</span></span>

<span data-ttu-id="b7142-140">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b7142-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b7142-141">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b7142-141">Shader Model</span></span>                                              | <span data-ttu-id="b7142-142">Supportato</span><span class="sxs-lookup"><span data-stu-id="b7142-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="b7142-143">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="b7142-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b7142-144">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="b7142-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="b7142-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7142-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b7142-146">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="b7142-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="b7142-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7142-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b7142-148">no</span><span class="sxs-lookup"><span data-stu-id="b7142-148">no</span></span>                      |
| [<span data-ttu-id="b7142-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7142-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b7142-150">no</span><span class="sxs-lookup"><span data-stu-id="b7142-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="b7142-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7142-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7142-152">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b7142-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

