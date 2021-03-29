---
title: callc (SM4-ASM)
description: Chiama in modo condizionale una subroutine contrassegnata da where the label l \ appare nel programma.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6bc8c9d1e4a99ce25f99253518482181cdb74d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993072"
---
# <a name="callc-sm4---asm"></a><span data-ttu-id="75171-103">callc (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="75171-103">callc (sm4 - asm)</span></span>

<span data-ttu-id="75171-104">Chiama in modo condizionale una subroutine contrassegnata da dove viene visualizzata l'etichetta **l \#** nel programma.</span><span class="sxs-lookup"><span data-stu-id="75171-104">Conditionally calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="75171-105">callc { \_ z </span><span class="sxs-lookup"><span data-stu-id="75171-105">callc{\_z</span></span>\|<span data-ttu-id="75171-106">\_NZ} src0. Selezionare il \_ componente, l\#</span><span class="sxs-lookup"><span data-stu-id="75171-106">\_nz} src0.select\_component, l\#</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="75171-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="75171-107">Item</span></span>                                                            | <span data-ttu-id="75171-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75171-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="75171-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="75171-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="75171-110">\[nel \] componente su cui eseguire il test della condizione.</span><span class="sxs-lookup"><span data-stu-id="75171-110">\[in\] The component on which to test the condition.</span></span><br/> |
| <span data-ttu-id="75171-111"><span id="l_"></span><span id="L_"></span>*l\#*</span><span class="sxs-lookup"><span data-stu-id="75171-111"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/>      | <span data-ttu-id="75171-112">\[nell' \] etichetta della subroutine.</span><span class="sxs-lookup"><span data-stu-id="75171-112">\[in\] The label of the subroutine.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="75171-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="75171-113">Remarks</span></span>

<span data-ttu-id="75171-114">Quando viene rilevata una [ret](ret--sm4---asm-.md) , restituisce l'esecuzione all'istruzione dopo questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="75171-114">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="75171-115">Il formato del token contiene l'offset dell'etichetta corrispondente nello shader per praticità.</span><span class="sxs-lookup"><span data-stu-id="75171-115">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="75171-116">Nell'esempio seguente viene illustrata l'istruzione Call.</span><span class="sxs-lookup"><span data-stu-id="75171-116">The following example shows the call instruction.</span></span>


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret

```



### <a name="restrictions"></a><span data-ttu-id="75171-117">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="75171-117">Restrictions</span></span>

-   <span data-ttu-id="75171-118">Le subroutine possono annidare 32 a fondo.</span><span class="sxs-lookup"><span data-stu-id="75171-118">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="75171-119">Lo stack degli indirizzi restituiti viene gestito in modo trasparente dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="75171-119">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="75171-120">Se sono già presenti 32 voci nello stack di indirizzi restituiti e viene eseguita una **chiamata** , la chiamata viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="75171-120">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="75171-121">Nessun stack di parametri automatico.</span><span class="sxs-lookup"><span data-stu-id="75171-121">There is no automatic parameter stack.</span></span> <span data-ttu-id="75171-122">L'applicazione può usare una matrice di registro temporanea indicizzabile (x \# \[ \] ) per implementare manualmente uno stack.</span><span class="sxs-lookup"><span data-stu-id="75171-122">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="75171-123">Tuttavia, gli indirizzi restituiti della chiamata subroutine non sono visibili e sono ortogonali a qualsiasi gestione dello stack manuale eseguita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="75171-123">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="75171-124">L'indicizzazione del parametro *l \#* non è consentita.</span><span class="sxs-lookup"><span data-stu-id="75171-124">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="75171-125">Il registro a 32 bit fornito da *src0* viene testato a livello di bit.</span><span class="sxs-lookup"><span data-stu-id="75171-125">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="75171-126">Se un bit è diverso da zero, **callc \_ NZ** eseguirà la chiamata.</span><span class="sxs-lookup"><span data-stu-id="75171-126">If any bit is nonzero, **callc\_nz** will perform the call.</span></span> <span data-ttu-id="75171-127">Se tutti i bit sono zero, **callc \_ z** eseguirà la chiamata.</span><span class="sxs-lookup"><span data-stu-id="75171-127">If all bits are zero, **callc\_z** will perform the call.</span></span>
-   <span data-ttu-id="75171-128">La ricorsione non è consentita.</span><span class="sxs-lookup"><span data-stu-id="75171-128">Recursion is not permitted.</span></span>

<span data-ttu-id="75171-129">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="75171-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="75171-130">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="75171-130">Vertex Shader</span></span> | <span data-ttu-id="75171-131">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="75171-131">Geometry Shader</span></span> | <span data-ttu-id="75171-132">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="75171-132">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="75171-133">x</span><span class="sxs-lookup"><span data-stu-id="75171-133">x</span></span>             | <span data-ttu-id="75171-134">x</span><span class="sxs-lookup"><span data-stu-id="75171-134">x</span></span>               | <span data-ttu-id="75171-135">x</span><span class="sxs-lookup"><span data-stu-id="75171-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="75171-136">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="75171-136">Minimum Shader Model</span></span>

<span data-ttu-id="75171-137">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="75171-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="75171-138">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="75171-138">Shader Model</span></span>                                              | <span data-ttu-id="75171-139">Supportato</span><span class="sxs-lookup"><span data-stu-id="75171-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="75171-140">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="75171-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="75171-141">sì</span><span class="sxs-lookup"><span data-stu-id="75171-141">yes</span></span>       |
| [<span data-ttu-id="75171-142">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="75171-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="75171-143">sì</span><span class="sxs-lookup"><span data-stu-id="75171-143">yes</span></span>       |
| [<span data-ttu-id="75171-144">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="75171-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="75171-145">sì</span><span class="sxs-lookup"><span data-stu-id="75171-145">yes</span></span>       |
| [<span data-ttu-id="75171-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75171-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="75171-147">no</span><span class="sxs-lookup"><span data-stu-id="75171-147">no</span></span>        |
| [<span data-ttu-id="75171-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75171-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="75171-149">no</span><span class="sxs-lookup"><span data-stu-id="75171-149">no</span></span>        |
| [<span data-ttu-id="75171-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75171-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="75171-151">no</span><span class="sxs-lookup"><span data-stu-id="75171-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="75171-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75171-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75171-153">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75171-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





