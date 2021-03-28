---
title: texCUBE (riferimento HLSL)-selezionare il livello MIP
description: Esegue il campionamento di una trama del cubo utilizzando una sfumatura per selezionare il livello MIP. | texCUBE (riferimento HLSL)
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
keywords:
- HLSL texCUBE
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6286b4fedb94b9fd5c84c76171e9478f06e16ce4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982675"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="46acc-105">texCUBE (riferimento HLSL)-selezionare il livello MIP</span><span class="sxs-lookup"><span data-stu-id="46acc-105">texCUBE (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="46acc-106">Esegue il campionamento di una trama del cubo utilizzando una sfumatura per selezionare il livello MIP.</span><span class="sxs-lookup"><span data-stu-id="46acc-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="46acc-107">RET texCUBE (s, t, DDX, ddy)</span><span class="sxs-lookup"><span data-stu-id="46acc-107">ret texCUBE(s, t, ddx, ddy)</span></span> |
|-----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="46acc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46acc-108">Parameters</span></span>



| <span data-ttu-id="46acc-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="46acc-109">Item</span></span>                                                         | <span data-ttu-id="46acc-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46acc-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="46acc-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="46acc-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="46acc-112">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="46acc-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="46acc-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="46acc-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="46acc-114">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="46acc-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="46acc-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="46acc-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="46acc-116">\[\]frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="46acc-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="46acc-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="46acc-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="46acc-118">\[\]frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="46acc-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="46acc-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46acc-119">Return Value</span></span>

<span data-ttu-id="46acc-120">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="46acc-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="46acc-121">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="46acc-121">Type Description</span></span>



| <span data-ttu-id="46acc-122">Nome</span><span class="sxs-lookup"><span data-stu-id="46acc-122">Name</span></span> | <span data-ttu-id="46acc-123">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="46acc-123">In/Out</span></span> | [<span data-ttu-id="46acc-124">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="46acc-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="46acc-125">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="46acc-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="46acc-126">Dimensione</span><span class="sxs-lookup"><span data-stu-id="46acc-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="46acc-127">s</span><span class="sxs-lookup"><span data-stu-id="46acc-127">s</span></span>    | <span data-ttu-id="46acc-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="46acc-128">in</span></span>     | [<span data-ttu-id="46acc-129">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="46acc-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="46acc-130">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="46acc-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="46acc-131">1</span><span class="sxs-lookup"><span data-stu-id="46acc-131">1</span></span>    |
| <span data-ttu-id="46acc-132">u</span><span class="sxs-lookup"><span data-stu-id="46acc-132">t</span></span>    | <span data-ttu-id="46acc-133">in ingresso</span><span class="sxs-lookup"><span data-stu-id="46acc-133">in</span></span>     | [<span data-ttu-id="46acc-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="46acc-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="46acc-135">**float**</span><span class="sxs-lookup"><span data-stu-id="46acc-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="46acc-136">3</span><span class="sxs-lookup"><span data-stu-id="46acc-136">3</span></span>    |
| <span data-ttu-id="46acc-137">DDX</span><span class="sxs-lookup"><span data-stu-id="46acc-137">ddx</span></span>  | <span data-ttu-id="46acc-138">in ingresso</span><span class="sxs-lookup"><span data-stu-id="46acc-138">in</span></span>     | [<span data-ttu-id="46acc-139">**vettore**</span><span class="sxs-lookup"><span data-stu-id="46acc-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="46acc-140">**float**</span><span class="sxs-lookup"><span data-stu-id="46acc-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="46acc-141">3</span><span class="sxs-lookup"><span data-stu-id="46acc-141">3</span></span>    |
| <span data-ttu-id="46acc-142">ddy</span><span class="sxs-lookup"><span data-stu-id="46acc-142">ddy</span></span>  | <span data-ttu-id="46acc-143">in ingresso</span><span class="sxs-lookup"><span data-stu-id="46acc-143">in</span></span>     | [<span data-ttu-id="46acc-144">**vettore**</span><span class="sxs-lookup"><span data-stu-id="46acc-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="46acc-145">**float**</span><span class="sxs-lookup"><span data-stu-id="46acc-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="46acc-146">3</span><span class="sxs-lookup"><span data-stu-id="46acc-146">3</span></span>    |
| <span data-ttu-id="46acc-147">RET</span><span class="sxs-lookup"><span data-stu-id="46acc-147">ret</span></span>  | <span data-ttu-id="46acc-148">in uscita</span><span class="sxs-lookup"><span data-stu-id="46acc-148">out</span></span>    | [<span data-ttu-id="46acc-149">**vettore**</span><span class="sxs-lookup"><span data-stu-id="46acc-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="46acc-150">**float**</span><span class="sxs-lookup"><span data-stu-id="46acc-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="46acc-151">4</span><span class="sxs-lookup"><span data-stu-id="46acc-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="46acc-152">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="46acc-152">Minimum Shader Model</span></span>

<span data-ttu-id="46acc-153">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="46acc-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="46acc-154">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="46acc-154">Shader Model</span></span>                                              | <span data-ttu-id="46acc-155">Supportato</span><span class="sxs-lookup"><span data-stu-id="46acc-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="46acc-156">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="46acc-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="46acc-157">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="46acc-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="46acc-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46acc-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="46acc-159">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="46acc-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="46acc-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46acc-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="46acc-161">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="46acc-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="46acc-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="46acc-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="46acc-163">no</span><span class="sxs-lookup"><span data-stu-id="46acc-163">no</span></span>                       |



 

1.  <span data-ttu-id="46acc-164">Il riordino significativo del codice viene eseguito per spostare i calcoli delle sfumature all'esterno del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="46acc-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="46acc-165">Se il limite di D3DPSHADERCAPS2 \_ 0 è impostato su \_ D3DD3DPSHADERCAPS2 0 \_ GRADIENTINSTRUCTIONS, il compilatore esegue il mapping di questa funzione a texldd.</span><span class="sxs-lookup"><span data-stu-id="46acc-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="46acc-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46acc-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46acc-167">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="46acc-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

