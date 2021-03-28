---
title: tex1Dproj
description: Campiona una trama 1D usando una divisione proiezioni; la coordinata di trama è divisa per t. w prima che la ricerca avvenga.
ms.assetid: 7cfe996d-3967-40da-b0e7-e03938478594
keywords:
- HLSL tex1Dproj
topic_type:
- apiref
api_name:
- tex1Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34fc1c019ab5479fe8a23446c94073e19ca68de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976783"
---
# <a name="tex1dproj"></a><span data-ttu-id="8cf41-104">tex1Dproj</span><span class="sxs-lookup"><span data-stu-id="8cf41-104">tex1Dproj</span></span>

<span data-ttu-id="8cf41-105">Campiona una trama 1D usando una divisione proiezioni; la coordinata di trama è divisa per t. w prima che la ricerca avvenga.</span><span class="sxs-lookup"><span data-stu-id="8cf41-105">Samples a 1D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="8cf41-106">tex1Dproj RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="8cf41-106">ret tex1Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="8cf41-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8cf41-107">Parameters</span></span>



| <span data-ttu-id="8cf41-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8cf41-108">Item</span></span>                                                   | <span data-ttu-id="8cf41-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cf41-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="8cf41-110"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="8cf41-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="8cf41-111">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="8cf41-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="8cf41-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="8cf41-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="8cf41-113">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="8cf41-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8cf41-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8cf41-114">Return Value</span></span>

<span data-ttu-id="8cf41-115">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="8cf41-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="8cf41-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="8cf41-116">Type Description</span></span>



| <span data-ttu-id="8cf41-117">Nome</span><span class="sxs-lookup"><span data-stu-id="8cf41-117">Name</span></span> | <span data-ttu-id="8cf41-118">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="8cf41-118">In/Out</span></span> | [<span data-ttu-id="8cf41-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="8cf41-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="8cf41-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="8cf41-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8cf41-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8cf41-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="8cf41-122">s</span><span class="sxs-lookup"><span data-stu-id="8cf41-122">s</span></span>    | <span data-ttu-id="8cf41-123">in ingresso</span><span class="sxs-lookup"><span data-stu-id="8cf41-123">in</span></span>     | [<span data-ttu-id="8cf41-124">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="8cf41-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8cf41-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="8cf41-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="8cf41-126">1</span><span class="sxs-lookup"><span data-stu-id="8cf41-126">1</span></span>    |
| <span data-ttu-id="8cf41-127">u</span><span class="sxs-lookup"><span data-stu-id="8cf41-127">t</span></span>    | <span data-ttu-id="8cf41-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="8cf41-128">in</span></span>     | [<span data-ttu-id="8cf41-129">**vettore**</span><span class="sxs-lookup"><span data-stu-id="8cf41-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8cf41-130">**float**</span><span class="sxs-lookup"><span data-stu-id="8cf41-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8cf41-131">4</span><span class="sxs-lookup"><span data-stu-id="8cf41-131">4</span></span>    |
| <span data-ttu-id="8cf41-132">RET</span><span class="sxs-lookup"><span data-stu-id="8cf41-132">ret</span></span>  | <span data-ttu-id="8cf41-133">in uscita</span><span class="sxs-lookup"><span data-stu-id="8cf41-133">out</span></span>    | [<span data-ttu-id="8cf41-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="8cf41-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8cf41-135">**float**</span><span class="sxs-lookup"><span data-stu-id="8cf41-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8cf41-136">4</span><span class="sxs-lookup"><span data-stu-id="8cf41-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8cf41-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8cf41-137">Minimum Shader Model</span></span>

<span data-ttu-id="8cf41-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8cf41-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8cf41-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8cf41-139">Shader Model</span></span>                                              | <span data-ttu-id="8cf41-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="8cf41-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="8cf41-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="8cf41-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8cf41-142">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8cf41-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="8cf41-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cf41-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8cf41-144">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8cf41-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="8cf41-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cf41-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8cf41-146">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8cf41-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="8cf41-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cf41-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8cf41-148">no</span><span class="sxs-lookup"><span data-stu-id="8cf41-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="8cf41-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cf41-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf41-150">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8cf41-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

