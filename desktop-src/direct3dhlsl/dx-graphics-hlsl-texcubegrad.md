---
title: texCUBEgrad
description: Esegue il campionamento di una trama del cubo utilizzando una sfumatura per selezionare il livello MIP. | texCUBEgrad
ms.assetid: ebc5e38a-e314-43b0-9a00-7e4147e24bf0
keywords:
- HLSL texCUBEgrad
topic_type:
- apiref
api_name:
- texCUBEgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 694382488754c221c59df72112678a5971e62c0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058506"
---
# <a name="texcubegrad"></a><span data-ttu-id="16da9-105">texCUBEgrad</span><span class="sxs-lookup"><span data-stu-id="16da9-105">texCUBEgrad</span></span>

<span data-ttu-id="16da9-106">Esegue il campionamento di una trama del cubo utilizzando una sfumatura per selezionare il livello MIP.</span><span class="sxs-lookup"><span data-stu-id="16da9-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="16da9-107">RET texCUBEgrad (s, t, DDX, ddy)</span><span class="sxs-lookup"><span data-stu-id="16da9-107">ret texCUBEgrad(s, t, ddx, ddy)</span></span> |
|---------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="16da9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="16da9-108">Parameters</span></span>



| <span data-ttu-id="16da9-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="16da9-109">Item</span></span>                                                         | <span data-ttu-id="16da9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16da9-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="16da9-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="16da9-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="16da9-112">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="16da9-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="16da9-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="16da9-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="16da9-114">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="16da9-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="16da9-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="16da9-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="16da9-116">\[\]frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="16da9-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="16da9-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="16da9-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="16da9-118">\[\]frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="16da9-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="16da9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16da9-119">Return Value</span></span>

<span data-ttu-id="16da9-120">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="16da9-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="16da9-121">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="16da9-121">Type Description</span></span>



| <span data-ttu-id="16da9-122">Nome</span><span class="sxs-lookup"><span data-stu-id="16da9-122">Name</span></span> | <span data-ttu-id="16da9-123">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="16da9-123">In/Out</span></span> | [<span data-ttu-id="16da9-124">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="16da9-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="16da9-125">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="16da9-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="16da9-126">Dimensione</span><span class="sxs-lookup"><span data-stu-id="16da9-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="16da9-127">s</span><span class="sxs-lookup"><span data-stu-id="16da9-127">s</span></span>    | <span data-ttu-id="16da9-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="16da9-128">in</span></span>     | [<span data-ttu-id="16da9-129">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="16da9-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="16da9-130">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="16da9-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="16da9-131">1</span><span class="sxs-lookup"><span data-stu-id="16da9-131">1</span></span>    |
| <span data-ttu-id="16da9-132">u</span><span class="sxs-lookup"><span data-stu-id="16da9-132">t</span></span>    | <span data-ttu-id="16da9-133">in ingresso</span><span class="sxs-lookup"><span data-stu-id="16da9-133">in</span></span>     | [<span data-ttu-id="16da9-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="16da9-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="16da9-135">**float**</span><span class="sxs-lookup"><span data-stu-id="16da9-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16da9-136">3</span><span class="sxs-lookup"><span data-stu-id="16da9-136">3</span></span>    |
| <span data-ttu-id="16da9-137">DDX</span><span class="sxs-lookup"><span data-stu-id="16da9-137">ddx</span></span>  | <span data-ttu-id="16da9-138">in ingresso</span><span class="sxs-lookup"><span data-stu-id="16da9-138">in</span></span>     | [<span data-ttu-id="16da9-139">**vettore**</span><span class="sxs-lookup"><span data-stu-id="16da9-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="16da9-140">**float**</span><span class="sxs-lookup"><span data-stu-id="16da9-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16da9-141">3</span><span class="sxs-lookup"><span data-stu-id="16da9-141">3</span></span>    |
| <span data-ttu-id="16da9-142">ddy</span><span class="sxs-lookup"><span data-stu-id="16da9-142">ddy</span></span>  | <span data-ttu-id="16da9-143">in ingresso</span><span class="sxs-lookup"><span data-stu-id="16da9-143">in</span></span>     | [<span data-ttu-id="16da9-144">**vettore**</span><span class="sxs-lookup"><span data-stu-id="16da9-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="16da9-145">**float**</span><span class="sxs-lookup"><span data-stu-id="16da9-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16da9-146">3</span><span class="sxs-lookup"><span data-stu-id="16da9-146">3</span></span>    |
| <span data-ttu-id="16da9-147">RET</span><span class="sxs-lookup"><span data-stu-id="16da9-147">ret</span></span>  | <span data-ttu-id="16da9-148">in uscita</span><span class="sxs-lookup"><span data-stu-id="16da9-148">out</span></span>    | [<span data-ttu-id="16da9-149">**vettore**</span><span class="sxs-lookup"><span data-stu-id="16da9-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="16da9-150">**float**</span><span class="sxs-lookup"><span data-stu-id="16da9-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16da9-151">4</span><span class="sxs-lookup"><span data-stu-id="16da9-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="16da9-152">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="16da9-152">Minimum Shader Model</span></span>

<span data-ttu-id="16da9-153">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="16da9-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="16da9-154">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="16da9-154">Shader Model</span></span>                                              | <span data-ttu-id="16da9-155">Supportato</span><span class="sxs-lookup"><span data-stu-id="16da9-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="16da9-156">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="16da9-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="16da9-157">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="16da9-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="16da9-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16da9-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="16da9-159">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="16da9-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="16da9-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16da9-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="16da9-161">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="16da9-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="16da9-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16da9-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="16da9-163">no</span><span class="sxs-lookup"><span data-stu-id="16da9-163">no</span></span>                       |



 

1.  <span data-ttu-id="16da9-164">Il riordino significativo del codice viene eseguito per spostare i calcoli delle sfumature all'esterno del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="16da9-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="16da9-165">Se il limite di D3DPSHADERCAPS2 \_ 0 è impostato su \_ D3DD3DPSHADERCAPS2 0 \_ GRADIENTINSTRUCTIONS, il compilatore esegue il mapping di questa funzione a texldd.</span><span class="sxs-lookup"><span data-stu-id="16da9-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="16da9-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16da9-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16da9-167">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="16da9-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

