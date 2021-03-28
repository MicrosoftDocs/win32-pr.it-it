---
title: tex2Dproj
description: Esegue il campionamento di una trama 2D usando una divisione proiezioni; la coordinata di trama è divisa per t. w prima che la ricerca avvenga.
ms.assetid: c6b79360-3737-4b74-bdf3-6d46323e8e54
keywords:
- HLSL tex2Dproj
topic_type:
- apiref
api_name:
- tex2Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 365401e4e4eca8703207ffb5c7676748f4a06d30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516864"
---
# <a name="tex2dproj"></a><span data-ttu-id="c2a52-104">tex2Dproj</span><span class="sxs-lookup"><span data-stu-id="c2a52-104">tex2Dproj</span></span>

<span data-ttu-id="c2a52-105">Esegue il campionamento di una trama 2D usando una divisione proiezioni; la coordinata di trama è divisa per t. w prima che la ricerca avvenga.</span><span class="sxs-lookup"><span data-stu-id="c2a52-105">Samples a 2D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="c2a52-106">tex2Dproj RET (s, t)</span><span class="sxs-lookup"><span data-stu-id="c2a52-106">ret tex2Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="c2a52-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2a52-107">Parameters</span></span>



| <span data-ttu-id="c2a52-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c2a52-108">Item</span></span>                                                   | <span data-ttu-id="c2a52-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2a52-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="c2a52-110"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="c2a52-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="c2a52-111">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="c2a52-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="c2a52-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="c2a52-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="c2a52-113">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="c2a52-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c2a52-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2a52-114">Return Value</span></span>

<span data-ttu-id="c2a52-115">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="c2a52-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="c2a52-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="c2a52-116">Type Description</span></span>



| <span data-ttu-id="c2a52-117">Nome</span><span class="sxs-lookup"><span data-stu-id="c2a52-117">Name</span></span> | <span data-ttu-id="c2a52-118">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="c2a52-118">In/Out</span></span> | [<span data-ttu-id="c2a52-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="c2a52-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="c2a52-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="c2a52-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c2a52-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c2a52-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="c2a52-122">s</span><span class="sxs-lookup"><span data-stu-id="c2a52-122">s</span></span>    | <span data-ttu-id="c2a52-123">in ingresso</span><span class="sxs-lookup"><span data-stu-id="c2a52-123">in</span></span>     | [<span data-ttu-id="c2a52-124">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="c2a52-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c2a52-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="c2a52-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="c2a52-126">1</span><span class="sxs-lookup"><span data-stu-id="c2a52-126">1</span></span>    |
| <span data-ttu-id="c2a52-127">u</span><span class="sxs-lookup"><span data-stu-id="c2a52-127">t</span></span>    | <span data-ttu-id="c2a52-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="c2a52-128">in</span></span>     | [<span data-ttu-id="c2a52-129">**vettore**</span><span class="sxs-lookup"><span data-stu-id="c2a52-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c2a52-130">**float**</span><span class="sxs-lookup"><span data-stu-id="c2a52-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c2a52-131">4</span><span class="sxs-lookup"><span data-stu-id="c2a52-131">4</span></span>    |
| <span data-ttu-id="c2a52-132">RET</span><span class="sxs-lookup"><span data-stu-id="c2a52-132">ret</span></span>  | <span data-ttu-id="c2a52-133">in uscita</span><span class="sxs-lookup"><span data-stu-id="c2a52-133">out</span></span>    | [<span data-ttu-id="c2a52-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="c2a52-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="c2a52-135">**float**</span><span class="sxs-lookup"><span data-stu-id="c2a52-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c2a52-136">4</span><span class="sxs-lookup"><span data-stu-id="c2a52-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c2a52-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c2a52-137">Minimum Shader Model</span></span>

<span data-ttu-id="c2a52-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c2a52-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c2a52-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c2a52-139">Shader Model</span></span>                                              | <span data-ttu-id="c2a52-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="c2a52-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="c2a52-141">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="c2a52-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c2a52-142">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="c2a52-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="c2a52-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2a52-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c2a52-144">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="c2a52-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="c2a52-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2a52-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c2a52-146">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="c2a52-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="c2a52-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2a52-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c2a52-148">no</span><span class="sxs-lookup"><span data-stu-id="c2a52-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="c2a52-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2a52-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a52-150">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c2a52-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

