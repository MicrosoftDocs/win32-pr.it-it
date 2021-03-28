---
title: tex3Dgrad
description: Esegue il campionamento di una trama 3D utilizzando una sfumatura per selezionare il livello MIP. | tex3Dgrad
ms.assetid: 230c42cc-31b7-4f57-ade4-14f069094d46
keywords:
- HLSL tex3Dgrad
topic_type:
- apiref
api_name:
- tex3Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cd8188b7f39cc2b79eb2e961857732cd8dae9f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981570"
---
# <a name="tex3dgrad"></a><span data-ttu-id="b95d8-105">tex3Dgrad</span><span class="sxs-lookup"><span data-stu-id="b95d8-105">tex3Dgrad</span></span>

<span data-ttu-id="b95d8-106">Esegue il campionamento di una trama 3D utilizzando una sfumatura per selezionare il livello MIP.</span><span class="sxs-lookup"><span data-stu-id="b95d8-106">Samples a 3D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="b95d8-107">RET tex3Dgrad (s, t, DDX, ddy)</span><span class="sxs-lookup"><span data-stu-id="b95d8-107">ret tex3Dgrad(s, t, ddx, ddy)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="b95d8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b95d8-108">Parameters</span></span>



| <span data-ttu-id="b95d8-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="b95d8-109">Item</span></span>                                                         | <span data-ttu-id="b95d8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b95d8-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b95d8-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="b95d8-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="b95d8-112">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="b95d8-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="b95d8-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="b95d8-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="b95d8-114">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="b95d8-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="b95d8-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="b95d8-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="b95d8-116">\[\]frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="b95d8-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="b95d8-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="b95d8-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="b95d8-118">\[\]frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="b95d8-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b95d8-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b95d8-119">Return Value</span></span>

<span data-ttu-id="b95d8-120">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="b95d8-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="b95d8-121">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="b95d8-121">Type Description</span></span>



| <span data-ttu-id="b95d8-122">Nome</span><span class="sxs-lookup"><span data-stu-id="b95d8-122">Name</span></span> | <span data-ttu-id="b95d8-123">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="b95d8-123">In/Out</span></span> | [<span data-ttu-id="b95d8-124">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="b95d8-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="b95d8-125">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="b95d8-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b95d8-126">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b95d8-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="b95d8-127">s</span><span class="sxs-lookup"><span data-stu-id="b95d8-127">s</span></span>    | <span data-ttu-id="b95d8-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="b95d8-128">in</span></span>     | [<span data-ttu-id="b95d8-129">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="b95d8-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b95d8-130">sampler3D</span><span class="sxs-lookup"><span data-stu-id="b95d8-130">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="b95d8-131">1</span><span class="sxs-lookup"><span data-stu-id="b95d8-131">1</span></span>    |
| <span data-ttu-id="b95d8-132">u</span><span class="sxs-lookup"><span data-stu-id="b95d8-132">t</span></span>    | <span data-ttu-id="b95d8-133">in ingresso</span><span class="sxs-lookup"><span data-stu-id="b95d8-133">in</span></span>     | [<span data-ttu-id="b95d8-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="b95d8-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b95d8-135">**float**</span><span class="sxs-lookup"><span data-stu-id="b95d8-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b95d8-136">3</span><span class="sxs-lookup"><span data-stu-id="b95d8-136">3</span></span>    |
| <span data-ttu-id="b95d8-137">DDX</span><span class="sxs-lookup"><span data-stu-id="b95d8-137">ddx</span></span>  | <span data-ttu-id="b95d8-138">in ingresso</span><span class="sxs-lookup"><span data-stu-id="b95d8-138">in</span></span>     | [<span data-ttu-id="b95d8-139">**vettore**</span><span class="sxs-lookup"><span data-stu-id="b95d8-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b95d8-140">**float**</span><span class="sxs-lookup"><span data-stu-id="b95d8-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b95d8-141">3</span><span class="sxs-lookup"><span data-stu-id="b95d8-141">3</span></span>    |
| <span data-ttu-id="b95d8-142">ddy</span><span class="sxs-lookup"><span data-stu-id="b95d8-142">ddy</span></span>  | <span data-ttu-id="b95d8-143">in ingresso</span><span class="sxs-lookup"><span data-stu-id="b95d8-143">in</span></span>     | [<span data-ttu-id="b95d8-144">**vettore**</span><span class="sxs-lookup"><span data-stu-id="b95d8-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b95d8-145">**float**</span><span class="sxs-lookup"><span data-stu-id="b95d8-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b95d8-146">3</span><span class="sxs-lookup"><span data-stu-id="b95d8-146">3</span></span>    |
| <span data-ttu-id="b95d8-147">RET</span><span class="sxs-lookup"><span data-stu-id="b95d8-147">ret</span></span>  | <span data-ttu-id="b95d8-148">in uscita</span><span class="sxs-lookup"><span data-stu-id="b95d8-148">out</span></span>    | [<span data-ttu-id="b95d8-149">**vettore**</span><span class="sxs-lookup"><span data-stu-id="b95d8-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b95d8-150">**float**</span><span class="sxs-lookup"><span data-stu-id="b95d8-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b95d8-151">4</span><span class="sxs-lookup"><span data-stu-id="b95d8-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b95d8-152">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b95d8-152">Minimum Shader Model</span></span>

<span data-ttu-id="b95d8-153">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b95d8-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b95d8-154">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b95d8-154">Shader Model</span></span>                                              | <span data-ttu-id="b95d8-155">Supportato</span><span class="sxs-lookup"><span data-stu-id="b95d8-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="b95d8-156">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="b95d8-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b95d8-157">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="b95d8-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="b95d8-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b95d8-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b95d8-159">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="b95d8-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="b95d8-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b95d8-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b95d8-161">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="b95d8-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="b95d8-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b95d8-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b95d8-163">no</span><span class="sxs-lookup"><span data-stu-id="b95d8-163">no</span></span>                       |



 

1.  <span data-ttu-id="b95d8-164">Il riordino significativo del codice viene eseguito per spostare i calcoli delle sfumature all'esterno del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="b95d8-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="b95d8-165">Se il limite di D3DPSHADERCAPS2 \_ 0 è impostato su \_ D3DD3DPSHADERCAPS2 0 \_ GRADIENTINSTRUCTIONS, il compilatore esegue il mapping di questa funzione a texldd.</span><span class="sxs-lookup"><span data-stu-id="b95d8-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="b95d8-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="b95d8-166">Remarks</span></span>

<span data-ttu-id="b95d8-167">Quando il controllo di flusso è presente in uno shader, il risultato di un calcolo della sfumatura richiesto all'interno di un percorso di branch specificato è ambiguo quando i pixel adiacenti possono passare a percorsi di controllo di flusso separati.</span><span class="sxs-lookup"><span data-stu-id="b95d8-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="b95d8-168">Pertanto, viene considerato non valido utilizzare qualsiasi operazione di pixel shader che richiede un calcolo di sfumatura in una posizione all'interno di un costrutto di controllo di flusso che può variare tra i pixel per una determinata primitiva che viene rasterizzata.</span><span class="sxs-lookup"><span data-stu-id="b95d8-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="b95d8-169">Se uno dei lati di un'istruzione **if** con l'attributo Branch usa una funzione gradiente, è possibile che venga generato un errore del compilatore.</span><span class="sxs-lookup"><span data-stu-id="b95d8-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="b95d8-170">Vedere l' [istruzione if (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="b95d8-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b95d8-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b95d8-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b95d8-172">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b95d8-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

