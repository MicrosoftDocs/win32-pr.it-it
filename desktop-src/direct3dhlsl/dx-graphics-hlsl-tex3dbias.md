---
title: tex3Dbias
description: Esegue il campionamento di una trama 3D dopo la distorsione del livello MIP per t.w.
ms.assetid: 6a506036-90d1-420c-a712-a373068c8c16
keywords:
- HLSL tex3Dbias
topic_type:
- apiref
api_name:
- tex3Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53fb0a196831a9dd9d7f7cbe7c34c56259f9a0e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399666"
---
# <a name="tex3dbias"></a><span data-ttu-id="c93cf-104">tex3Dbias</span><span class="sxs-lookup"><span data-stu-id="c93cf-104">tex3Dbias</span></span>

<span data-ttu-id="c93cf-105">Esegue il campionamento di una trama 3D dopo la distorsione del livello MIP per t.w.</span><span class="sxs-lookup"><span data-stu-id="c93cf-105">Samples a 3D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="c93cf-106">tex3Dbias RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="c93cf-106">ret tex3Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="c93cf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c93cf-107">Parameters</span></span>



| <span data-ttu-id="c93cf-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c93cf-108">Item</span></span>                                                   | <span data-ttu-id="c93cf-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c93cf-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="c93cf-110"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="c93cf-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="c93cf-111">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="c93cf-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="c93cf-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="c93cf-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="c93cf-113">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="c93cf-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c93cf-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c93cf-114">Return Value</span></span>

<span data-ttu-id="c93cf-115">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="c93cf-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="c93cf-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="c93cf-116">Type Description</span></span>



| <span data-ttu-id="c93cf-117">Nome</span><span class="sxs-lookup"><span data-stu-id="c93cf-117">Name</span></span> | <span data-ttu-id="c93cf-118">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="c93cf-118">In/Out</span></span> | [<span data-ttu-id="c93cf-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="c93cf-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="c93cf-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="c93cf-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c93cf-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c93cf-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="c93cf-122">s</span><span class="sxs-lookup"><span data-stu-id="c93cf-122">s</span></span>    | <span data-ttu-id="c93cf-123">in ingresso</span><span class="sxs-lookup"><span data-stu-id="c93cf-123">in</span></span>     | [<span data-ttu-id="c93cf-124">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="c93cf-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c93cf-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="c93cf-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="c93cf-126">1</span><span class="sxs-lookup"><span data-stu-id="c93cf-126">1</span></span>    |
| <span data-ttu-id="c93cf-127">u</span><span class="sxs-lookup"><span data-stu-id="c93cf-127">t</span></span>    | <span data-ttu-id="c93cf-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="c93cf-128">in</span></span>     | [<span data-ttu-id="c93cf-129">**vettore**</span><span class="sxs-lookup"><span data-stu-id="c93cf-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c93cf-130">**float**</span><span class="sxs-lookup"><span data-stu-id="c93cf-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c93cf-131">4</span><span class="sxs-lookup"><span data-stu-id="c93cf-131">4</span></span>    |
| <span data-ttu-id="c93cf-132">RET</span><span class="sxs-lookup"><span data-stu-id="c93cf-132">ret</span></span>  | <span data-ttu-id="c93cf-133">in uscita</span><span class="sxs-lookup"><span data-stu-id="c93cf-133">out</span></span>    | [<span data-ttu-id="c93cf-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="c93cf-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c93cf-135">**float**</span><span class="sxs-lookup"><span data-stu-id="c93cf-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c93cf-136">4</span><span class="sxs-lookup"><span data-stu-id="c93cf-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c93cf-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c93cf-137">Minimum Shader Model</span></span>

<span data-ttu-id="c93cf-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c93cf-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c93cf-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c93cf-139">Shader Model</span></span>                                              | <span data-ttu-id="c93cf-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="c93cf-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="c93cf-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="c93cf-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c93cf-142">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="c93cf-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="c93cf-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c93cf-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c93cf-144">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="c93cf-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="c93cf-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c93cf-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c93cf-146">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="c93cf-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="c93cf-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c93cf-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c93cf-148">no</span><span class="sxs-lookup"><span data-stu-id="c93cf-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="c93cf-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c93cf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93cf-150">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c93cf-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

