---
title: tex3Dproj
description: Esegue il campionamento di una trama 3D utilizzando una divisione proiezioni; la coordinata di trama è divisa per t. w prima che la ricerca avvenga.
ms.assetid: c7062ef0-3169-4cbe-b47b-4efc80944963
keywords:
- HLSL tex3Dproj
topic_type:
- apiref
api_name:
- tex3Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 519477b7dba4f746dc1720a08c2ce581ab7b7205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517031"
---
# <a name="tex3dproj"></a><span data-ttu-id="46ec1-104">tex3Dproj</span><span class="sxs-lookup"><span data-stu-id="46ec1-104">tex3Dproj</span></span>

<span data-ttu-id="46ec1-105">Esegue il campionamento di una trama 3D utilizzando una divisione proiezioni; la coordinata di trama è divisa per t. w prima che la ricerca avvenga.</span><span class="sxs-lookup"><span data-stu-id="46ec1-105">Samples a 3D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="46ec1-106">tex3Dproj RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="46ec1-106">ret tex3Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="46ec1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="46ec1-107">Parameters</span></span>



| <span data-ttu-id="46ec1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="46ec1-108">Item</span></span>                                                   | <span data-ttu-id="46ec1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46ec1-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="46ec1-110"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="46ec1-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="46ec1-111">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="46ec1-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="46ec1-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="46ec1-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="46ec1-113">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="46ec1-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="46ec1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46ec1-114">Return Value</span></span>

<span data-ttu-id="46ec1-115">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="46ec1-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="46ec1-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="46ec1-116">Type Description</span></span>



| <span data-ttu-id="46ec1-117">Nome</span><span class="sxs-lookup"><span data-stu-id="46ec1-117">Name</span></span> | <span data-ttu-id="46ec1-118">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="46ec1-118">In/Out</span></span> | [<span data-ttu-id="46ec1-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="46ec1-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="46ec1-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="46ec1-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="46ec1-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="46ec1-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="46ec1-122">s</span><span class="sxs-lookup"><span data-stu-id="46ec1-122">s</span></span>    | <span data-ttu-id="46ec1-123">in ingresso</span><span class="sxs-lookup"><span data-stu-id="46ec1-123">in</span></span>     | [<span data-ttu-id="46ec1-124">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="46ec1-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="46ec1-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="46ec1-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="46ec1-126">1</span><span class="sxs-lookup"><span data-stu-id="46ec1-126">1</span></span>    |
| <span data-ttu-id="46ec1-127">u</span><span class="sxs-lookup"><span data-stu-id="46ec1-127">t</span></span>    | <span data-ttu-id="46ec1-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="46ec1-128">in</span></span>     | [<span data-ttu-id="46ec1-129">**vettore**</span><span class="sxs-lookup"><span data-stu-id="46ec1-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="46ec1-130">**float**</span><span class="sxs-lookup"><span data-stu-id="46ec1-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="46ec1-131">4</span><span class="sxs-lookup"><span data-stu-id="46ec1-131">4</span></span>    |
| <span data-ttu-id="46ec1-132">RET</span><span class="sxs-lookup"><span data-stu-id="46ec1-132">ret</span></span>  | <span data-ttu-id="46ec1-133">in uscita</span><span class="sxs-lookup"><span data-stu-id="46ec1-133">out</span></span>    | [<span data-ttu-id="46ec1-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="46ec1-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="46ec1-135">**float**</span><span class="sxs-lookup"><span data-stu-id="46ec1-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="46ec1-136">4</span><span class="sxs-lookup"><span data-stu-id="46ec1-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="46ec1-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="46ec1-137">Minimum Shader Model</span></span>

<span data-ttu-id="46ec1-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="46ec1-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="46ec1-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="46ec1-139">Shader Model</span></span>                                              | <span data-ttu-id="46ec1-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="46ec1-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="46ec1-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="46ec1-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="46ec1-142">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="46ec1-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="46ec1-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46ec1-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="46ec1-144">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="46ec1-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="46ec1-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46ec1-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="46ec1-146">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="46ec1-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="46ec1-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46ec1-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="46ec1-148">no</span><span class="sxs-lookup"><span data-stu-id="46ec1-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="46ec1-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46ec1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ec1-150">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="46ec1-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

