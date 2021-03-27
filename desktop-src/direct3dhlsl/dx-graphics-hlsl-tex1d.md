---
title: tex1D (riferimento HLSL)
description: Campiona una trama 1D.
ms.assetid: 587be0fd-af12-4bf0-862b-84988435e90e
keywords:
- HLSL tex1D
topic_type:
- apiref
api_name:
- tex1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dec5cc8a35b18c35076f99443ad3c1166fcf410
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728202"
---
# <a name="tex1d-hlsl-reference"></a><span data-ttu-id="fe646-104">tex1D (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe646-104">tex1D (HLSL reference)</span></span>

<span data-ttu-id="fe646-105">Campiona una trama 1D.</span><span class="sxs-lookup"><span data-stu-id="fe646-105">Samples a 1D texture.</span></span>



| <span data-ttu-id="fe646-106">tex1D RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="fe646-106">ret tex1D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="fe646-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe646-107">Parameters</span></span>



| <span data-ttu-id="fe646-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="fe646-108">Item</span></span>                                                   | <span data-ttu-id="fe646-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe646-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="fe646-110"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="fe646-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="fe646-111">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="fe646-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="fe646-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="fe646-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="fe646-113">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="fe646-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fe646-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe646-114">Return Value</span></span>

<span data-ttu-id="fe646-115">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="fe646-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="fe646-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="fe646-116">Type Description</span></span>



| <span data-ttu-id="fe646-117">Nome</span><span class="sxs-lookup"><span data-stu-id="fe646-117">Name</span></span> | <span data-ttu-id="fe646-118">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="fe646-118">In/Out</span></span> | [<span data-ttu-id="fe646-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="fe646-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="fe646-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="fe646-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="fe646-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="fe646-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="fe646-122">s</span><span class="sxs-lookup"><span data-stu-id="fe646-122">s</span></span>    | <span data-ttu-id="fe646-123">in ingresso</span><span class="sxs-lookup"><span data-stu-id="fe646-123">in</span></span>     | [<span data-ttu-id="fe646-124">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="fe646-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fe646-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="fe646-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="fe646-126">1</span><span class="sxs-lookup"><span data-stu-id="fe646-126">1</span></span>    |
| <span data-ttu-id="fe646-127">u</span><span class="sxs-lookup"><span data-stu-id="fe646-127">t</span></span>    | <span data-ttu-id="fe646-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="fe646-128">in</span></span>     | [<span data-ttu-id="fe646-129">**scalare**</span><span class="sxs-lookup"><span data-stu-id="fe646-129">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fe646-130">**float**</span><span class="sxs-lookup"><span data-stu-id="fe646-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fe646-131">1</span><span class="sxs-lookup"><span data-stu-id="fe646-131">1</span></span>    |
| <span data-ttu-id="fe646-132">RET</span><span class="sxs-lookup"><span data-stu-id="fe646-132">ret</span></span>  | <span data-ttu-id="fe646-133">in uscita</span><span class="sxs-lookup"><span data-stu-id="fe646-133">out</span></span>    | [<span data-ttu-id="fe646-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="fe646-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="fe646-135">**float**</span><span class="sxs-lookup"><span data-stu-id="fe646-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fe646-136">4</span><span class="sxs-lookup"><span data-stu-id="fe646-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fe646-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="fe646-137">Minimum Shader Model</span></span>

<span data-ttu-id="fe646-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="fe646-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fe646-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="fe646-139">Shader Model</span></span>                                              | <span data-ttu-id="fe646-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="fe646-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe646-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="fe646-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fe646-142">Sì (solo pixel shader), ma è necessario usare l' [opzione di compilazione legacy](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="fe646-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="fe646-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe646-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fe646-144">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="fe646-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="fe646-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe646-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fe646-146">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="fe646-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="fe646-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe646-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fe646-148">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="fe646-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="fe646-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe646-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe646-150">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fe646-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

