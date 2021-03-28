---
title: texCUBEbias
description: Esegue il campionamento di una trama del cubo dopo la distorsione del livello MIP per t.w.
ms.assetid: dad27cff-6b10-45db-b70f-c4ad78c64e76
keywords:
- HLSL texCUBEbias
topic_type:
- apiref
api_name:
- texCUBEbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0129c20db1da320e9cb85aacfc4490124be28f8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117834"
---
# <a name="texcubebias"></a><span data-ttu-id="c9345-104">texCUBEbias</span><span class="sxs-lookup"><span data-stu-id="c9345-104">texCUBEbias</span></span>

<span data-ttu-id="c9345-105">Esegue il campionamento di una trama del cubo dopo la distorsione del livello MIP per t.w.</span><span class="sxs-lookup"><span data-stu-id="c9345-105">Samples a cube texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="c9345-106">texCUBEbias RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="c9345-106">ret texCUBEbias(s, t)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="c9345-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9345-107">Parameters</span></span>



| <span data-ttu-id="c9345-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9345-108">Item</span></span>                                                   | <span data-ttu-id="c9345-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9345-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="c9345-110"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="c9345-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="c9345-111">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="c9345-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="c9345-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="c9345-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="c9345-113">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="c9345-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c9345-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9345-114">Return Value</span></span>

<span data-ttu-id="c9345-115">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="c9345-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="c9345-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="c9345-116">Type Description</span></span>



| <span data-ttu-id="c9345-117">Nome</span><span class="sxs-lookup"><span data-stu-id="c9345-117">Name</span></span> | <span data-ttu-id="c9345-118">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="c9345-118">In/Out</span></span> | [<span data-ttu-id="c9345-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="c9345-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="c9345-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="c9345-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c9345-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c9345-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="c9345-122">s</span><span class="sxs-lookup"><span data-stu-id="c9345-122">s</span></span>    | <span data-ttu-id="c9345-123">in ingresso</span><span class="sxs-lookup"><span data-stu-id="c9345-123">in</span></span>     | [<span data-ttu-id="c9345-124">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="c9345-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c9345-125">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="c9345-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="c9345-126">1</span><span class="sxs-lookup"><span data-stu-id="c9345-126">1</span></span>    |
| <span data-ttu-id="c9345-127">u</span><span class="sxs-lookup"><span data-stu-id="c9345-127">t</span></span>    | <span data-ttu-id="c9345-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="c9345-128">in</span></span>     | [<span data-ttu-id="c9345-129">**vettore**</span><span class="sxs-lookup"><span data-stu-id="c9345-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c9345-130">**float**</span><span class="sxs-lookup"><span data-stu-id="c9345-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c9345-131">4</span><span class="sxs-lookup"><span data-stu-id="c9345-131">4</span></span>    |
| <span data-ttu-id="c9345-132">RET</span><span class="sxs-lookup"><span data-stu-id="c9345-132">ret</span></span>  | <span data-ttu-id="c9345-133">in uscita</span><span class="sxs-lookup"><span data-stu-id="c9345-133">out</span></span>    | [<span data-ttu-id="c9345-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="c9345-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c9345-135">**float**</span><span class="sxs-lookup"><span data-stu-id="c9345-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c9345-136">4</span><span class="sxs-lookup"><span data-stu-id="c9345-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c9345-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c9345-137">Minimum Shader Model</span></span>

<span data-ttu-id="c9345-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9345-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c9345-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c9345-139">Shader Model</span></span>                                              | <span data-ttu-id="c9345-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="c9345-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="c9345-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="c9345-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c9345-142">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="c9345-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="c9345-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9345-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c9345-144">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="c9345-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="c9345-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9345-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c9345-146">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="c9345-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="c9345-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9345-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c9345-148">no</span><span class="sxs-lookup"><span data-stu-id="c9345-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="c9345-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9345-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9345-150">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c9345-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

