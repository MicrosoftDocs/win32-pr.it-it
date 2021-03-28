---
title: tex1D (riferimento HLSL)-selezionare il livello MIP
description: Campiona una trama 1D utilizzando una sfumatura per selezionare il livello MIP. | tex1D (riferimento HLSL)
ms.assetid: 1fa01f39-1c01-4a2e-9f7d-ca8e887b00bb
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
ms.openlocfilehash: b3ec506bdbc636051e7723af4942f33f2d449ae6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982699"
---
# <a name="tex1d-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="8cde9-105">tex1D (riferimento HLSL)-selezionare il livello MIP</span><span class="sxs-lookup"><span data-stu-id="8cde9-105">tex1D (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="8cde9-106">Campiona una trama 1D utilizzando una sfumatura per selezionare il livello MIP.</span><span class="sxs-lookup"><span data-stu-id="8cde9-106">Samples a 1D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="8cde9-107">RET tex1D (s, t, DDX, ddy)</span><span class="sxs-lookup"><span data-stu-id="8cde9-107">ret tex1D(s, t, ddx, ddy)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="8cde9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8cde9-108">Parameters</span></span>



| <span data-ttu-id="8cde9-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="8cde9-109">Item</span></span>                                                         | <span data-ttu-id="8cde9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cde9-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8cde9-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="8cde9-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="8cde9-112">\[nello \] stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="8cde9-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="8cde9-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="8cde9-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="8cde9-114">\[nella \] coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="8cde9-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="8cde9-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="8cde9-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="8cde9-116">\[\]frequenza di modifica della geometria della superficie nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="8cde9-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="8cde9-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="8cde9-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="8cde9-118">\[\]frequenza di modifica della geometria della superficie nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="8cde9-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8cde9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8cde9-119">Return Value</span></span>

<span data-ttu-id="8cde9-120">Valore dei dati della trama.</span><span class="sxs-lookup"><span data-stu-id="8cde9-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="8cde9-121">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="8cde9-121">Type Description</span></span>



| <span data-ttu-id="8cde9-122">Nome</span><span class="sxs-lookup"><span data-stu-id="8cde9-122">Name</span></span> | <span data-ttu-id="8cde9-123">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="8cde9-123">In/Out</span></span> | [<span data-ttu-id="8cde9-124">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="8cde9-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="8cde9-125">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="8cde9-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8cde9-126">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8cde9-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="8cde9-127">s</span><span class="sxs-lookup"><span data-stu-id="8cde9-127">s</span></span>    | <span data-ttu-id="8cde9-128">in ingresso</span><span class="sxs-lookup"><span data-stu-id="8cde9-128">in</span></span>     | [<span data-ttu-id="8cde9-129">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="8cde9-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8cde9-130">sampler1D</span><span class="sxs-lookup"><span data-stu-id="8cde9-130">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="8cde9-131">1</span><span class="sxs-lookup"><span data-stu-id="8cde9-131">1</span></span>    |
| <span data-ttu-id="8cde9-132">u</span><span class="sxs-lookup"><span data-stu-id="8cde9-132">t</span></span>    | <span data-ttu-id="8cde9-133">in ingresso</span><span class="sxs-lookup"><span data-stu-id="8cde9-133">in</span></span>     | [<span data-ttu-id="8cde9-134">**vettore**</span><span class="sxs-lookup"><span data-stu-id="8cde9-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8cde9-135">**float**</span><span class="sxs-lookup"><span data-stu-id="8cde9-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8cde9-136">1</span><span class="sxs-lookup"><span data-stu-id="8cde9-136">1</span></span>    |
| <span data-ttu-id="8cde9-137">DDX</span><span class="sxs-lookup"><span data-stu-id="8cde9-137">ddx</span></span>  | <span data-ttu-id="8cde9-138">in ingresso</span><span class="sxs-lookup"><span data-stu-id="8cde9-138">in</span></span>     | [<span data-ttu-id="8cde9-139">**vettore**</span><span class="sxs-lookup"><span data-stu-id="8cde9-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8cde9-140">**float**</span><span class="sxs-lookup"><span data-stu-id="8cde9-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8cde9-141">1</span><span class="sxs-lookup"><span data-stu-id="8cde9-141">1</span></span>    |
| <span data-ttu-id="8cde9-142">ddy</span><span class="sxs-lookup"><span data-stu-id="8cde9-142">ddy</span></span>  | <span data-ttu-id="8cde9-143">in ingresso</span><span class="sxs-lookup"><span data-stu-id="8cde9-143">in</span></span>     | [<span data-ttu-id="8cde9-144">**vettore**</span><span class="sxs-lookup"><span data-stu-id="8cde9-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8cde9-145">**float**</span><span class="sxs-lookup"><span data-stu-id="8cde9-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8cde9-146">1</span><span class="sxs-lookup"><span data-stu-id="8cde9-146">1</span></span>    |
| <span data-ttu-id="8cde9-147">RET</span><span class="sxs-lookup"><span data-stu-id="8cde9-147">ret</span></span>  | <span data-ttu-id="8cde9-148">in uscita</span><span class="sxs-lookup"><span data-stu-id="8cde9-148">out</span></span>    | [<span data-ttu-id="8cde9-149">**vettore**</span><span class="sxs-lookup"><span data-stu-id="8cde9-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8cde9-150">**float**</span><span class="sxs-lookup"><span data-stu-id="8cde9-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8cde9-151">4</span><span class="sxs-lookup"><span data-stu-id="8cde9-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8cde9-152">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8cde9-152">Minimum Shader Model</span></span>

<span data-ttu-id="8cde9-153">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8cde9-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8cde9-154">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8cde9-154">Shader Model</span></span>                                              | <span data-ttu-id="8cde9-155">Supportato</span><span class="sxs-lookup"><span data-stu-id="8cde9-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="8cde9-156">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="8cde9-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8cde9-157">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8cde9-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="8cde9-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cde9-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8cde9-159">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8cde9-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="8cde9-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cde9-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8cde9-161">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8cde9-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="8cde9-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cde9-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8cde9-163">no</span><span class="sxs-lookup"><span data-stu-id="8cde9-163">no</span></span>                       |



 

1.  <span data-ttu-id="8cde9-164">Il riordino significativo del codice viene eseguito per spostare i calcoli delle sfumature all'esterno del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="8cde9-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="8cde9-165">Se il limite di D3DPSHADERCAPS2 \_ 0 è impostato su \_ D3DD3DPSHADERCAPS2 0 \_ GRADIENTINSTRUCTIONS, il compilatore esegue il mapping di questa funzione a texldd.</span><span class="sxs-lookup"><span data-stu-id="8cde9-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cde9-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="8cde9-166">Remarks</span></span>

<span data-ttu-id="8cde9-167">Quando il controllo di flusso è presente in uno shader, il risultato di un calcolo della sfumatura richiesto all'interno di un percorso di branch specificato è ambiguo quando i pixel adiacenti possono passare a percorsi di controllo di flusso separati.</span><span class="sxs-lookup"><span data-stu-id="8cde9-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="8cde9-168">Pertanto, viene considerato non valido utilizzare qualsiasi operazione di pixel shader che richiede un calcolo di sfumatura in una posizione all'interno di un costrutto di controllo di flusso che può variare tra i pixel per una determinata primitiva che viene rasterizzata.</span><span class="sxs-lookup"><span data-stu-id="8cde9-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="8cde9-169">Se uno dei lati di un'istruzione **if** con l'attributo Branch usa una funzione gradiente, è possibile che venga generato un errore del compilatore.</span><span class="sxs-lookup"><span data-stu-id="8cde9-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="8cde9-170">Vedere l' [istruzione if (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="8cde9-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8cde9-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cde9-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cde9-172">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8cde9-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

