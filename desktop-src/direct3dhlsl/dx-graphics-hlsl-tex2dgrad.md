---
title: tex2Dgrad
description: Esegue il campionamento di una trama 2D utilizzando una sfumatura per selezionare il livello MIP. | tex2Dgrad
ms.assetid: a9ab7972-3480-4b37-aa10-c5cf811bdd0e
keywords:
- HLSL tex2Dgrad
topic_type:
- apiref
api_name:
- tex2Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74b20f1cf1f6f5d3b2873f4546dd57ef73b23dbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981119"
---
# <a name="tex2dgrad"></a><span data-ttu-id="8caa7-105">tex2Dgrad</span><span class="sxs-lookup"><span data-stu-id="8caa7-105">tex2Dgrad</span></span>

<span data-ttu-id="8caa7-106">Esegue il campionamento di una trama 2D utilizzando una sfumatura per selezionare il livello MIP.</span><span class="sxs-lookup"><span data-stu-id="8caa7-106">Samples a 2D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="8caa7-107">RET tex2Dgrad (s, t, DDX, ddy)</span><span class="sxs-lookup"><span data-stu-id="8caa7-107">ret tex2Dgrad(s, t, ddx, ddy)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="8caa7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8caa7-108">Parameters</span></span>



| <span data-ttu-id="8caa7-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="8caa7-109">Item</span></span>                                                         | <span data-ttu-id="8caa7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8caa7-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8caa7-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="8caa7-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="8caa7-112">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="8caa7-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="8caa7-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="8caa7-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="8caa7-114">\[nelle \] coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="8caa7-114">\[in\] The texture coordinates.</span></span><br/>                                   |
| <span data-ttu-id="8caa7-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="8caa7-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="8caa7-116">\[\]frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="8caa7-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="8caa7-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="8caa7-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="8caa7-118">\[\]frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="8caa7-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8caa7-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8caa7-119">Return Value</span></span>

<span data-ttu-id="8caa7-120">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="8caa7-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="8caa7-121">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="8caa7-121">Type Description</span></span>



| <span data-ttu-id="8caa7-122">Nome</span><span class="sxs-lookup"><span data-stu-id="8caa7-122">Name</span></span> | <span data-ttu-id="8caa7-123">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="8caa7-123">In/Out</span></span> | [<span data-ttu-id="8caa7-124">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="8caa7-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="8caa7-125">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="8caa7-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8caa7-126">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8caa7-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="8caa7-127">s</span><span class="sxs-lookup"><span data-stu-id="8caa7-127">s</span></span>    | <span data-ttu-id="8caa7-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="8caa7-128">in</span></span>     | [<span data-ttu-id="8caa7-129">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="8caa7-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8caa7-130">sampler2D</span><span class="sxs-lookup"><span data-stu-id="8caa7-130">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="8caa7-131">1</span><span class="sxs-lookup"><span data-stu-id="8caa7-131">1</span></span>    |
| <span data-ttu-id="8caa7-132">u</span><span class="sxs-lookup"><span data-stu-id="8caa7-132">t</span></span>    | <span data-ttu-id="8caa7-133">in ingresso</span><span class="sxs-lookup"><span data-stu-id="8caa7-133">in</span></span>     | [<span data-ttu-id="8caa7-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="8caa7-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8caa7-135">**float**</span><span class="sxs-lookup"><span data-stu-id="8caa7-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8caa7-136">2</span><span class="sxs-lookup"><span data-stu-id="8caa7-136">2</span></span>    |
| <span data-ttu-id="8caa7-137">DDX</span><span class="sxs-lookup"><span data-stu-id="8caa7-137">ddx</span></span>  | <span data-ttu-id="8caa7-138">in ingresso</span><span class="sxs-lookup"><span data-stu-id="8caa7-138">in</span></span>     | [<span data-ttu-id="8caa7-139">**vettore**</span><span class="sxs-lookup"><span data-stu-id="8caa7-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8caa7-140">**float**</span><span class="sxs-lookup"><span data-stu-id="8caa7-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8caa7-141">2</span><span class="sxs-lookup"><span data-stu-id="8caa7-141">2</span></span>    |
| <span data-ttu-id="8caa7-142">ddy</span><span class="sxs-lookup"><span data-stu-id="8caa7-142">ddy</span></span>  | <span data-ttu-id="8caa7-143">in ingresso</span><span class="sxs-lookup"><span data-stu-id="8caa7-143">in</span></span>     | [<span data-ttu-id="8caa7-144">**vettore**</span><span class="sxs-lookup"><span data-stu-id="8caa7-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8caa7-145">**float**</span><span class="sxs-lookup"><span data-stu-id="8caa7-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8caa7-146">2</span><span class="sxs-lookup"><span data-stu-id="8caa7-146">2</span></span>    |
| <span data-ttu-id="8caa7-147">RET</span><span class="sxs-lookup"><span data-stu-id="8caa7-147">ret</span></span>  | <span data-ttu-id="8caa7-148">in uscita</span><span class="sxs-lookup"><span data-stu-id="8caa7-148">out</span></span>    | [<span data-ttu-id="8caa7-149">**vettore**</span><span class="sxs-lookup"><span data-stu-id="8caa7-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8caa7-150">**float**</span><span class="sxs-lookup"><span data-stu-id="8caa7-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8caa7-151">4</span><span class="sxs-lookup"><span data-stu-id="8caa7-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8caa7-152">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8caa7-152">Minimum Shader Model</span></span>

<span data-ttu-id="8caa7-153">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8caa7-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8caa7-154">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8caa7-154">Shader Model</span></span>                                              | <span data-ttu-id="8caa7-155">Supportato</span><span class="sxs-lookup"><span data-stu-id="8caa7-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="8caa7-156">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="8caa7-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8caa7-157">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8caa7-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="8caa7-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8caa7-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8caa7-159">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8caa7-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="8caa7-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8caa7-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8caa7-161">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8caa7-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="8caa7-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8caa7-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8caa7-163">no</span><span class="sxs-lookup"><span data-stu-id="8caa7-163">no</span></span>                       |



 

1.  <span data-ttu-id="8caa7-164">Il riordino significativo del codice viene eseguito per spostare i calcoli delle sfumature all'esterno del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="8caa7-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="8caa7-165">Se il limite di D3DPSHADERCAPS2 \_ 0 è impostato su \_ D3DD3DPSHADERCAPS2 0 \_ GRADIENTINSTRUCTIONS, il compilatore esegue il mapping di questa funzione a texldd.</span><span class="sxs-lookup"><span data-stu-id="8caa7-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="8caa7-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="8caa7-166">Remarks</span></span>

<span data-ttu-id="8caa7-167">Quando il controllo di flusso è presente in uno shader, il risultato di un calcolo della sfumatura richiesto all'interno di un percorso di branch specificato è ambiguo quando i pixel adiacenti possono passare a percorsi di controllo di flusso separati.</span><span class="sxs-lookup"><span data-stu-id="8caa7-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="8caa7-168">Pertanto, viene considerato non valido utilizzare qualsiasi operazione di pixel shader che richiede un calcolo di sfumatura in una posizione all'interno di un costrutto di controllo di flusso che può variare tra i pixel per una determinata primitiva che viene rasterizzata.</span><span class="sxs-lookup"><span data-stu-id="8caa7-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="8caa7-169">Se uno dei lati di un'istruzione **if** con l'attributo Branch usa una funzione gradiente, è possibile che venga generato un errore del compilatore.</span><span class="sxs-lookup"><span data-stu-id="8caa7-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="8caa7-170">Vedere l' [istruzione if (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="8caa7-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8caa7-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8caa7-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8caa7-172">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8caa7-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

