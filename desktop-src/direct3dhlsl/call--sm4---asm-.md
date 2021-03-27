---
title: chiamata (SM4-ASM)
description: Chiama una subroutine contrassegnata da dove l'etichetta l \ appare nel programma.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dac86fa52140968443f01050cebc57718fea420
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719399"
---
# <a name="call-sm4---asm"></a><span data-ttu-id="cb8a4-103">chiamata (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="cb8a4-103">call (sm4 - asm)</span></span>

<span data-ttu-id="cb8a4-104">Chiama una subroutine contrassegnata da dove viene visualizzata l'etichetta **l \#** nel programma.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-104">Calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="cb8a4-105">chiama l\#</span><span class="sxs-lookup"><span data-stu-id="cb8a4-105">call l\#</span></span> |
|----------|



 



| <span data-ttu-id="cb8a4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="cb8a4-106">Item</span></span>                                                       | <span data-ttu-id="cb8a4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb8a4-107">Description</span></span>                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="cb8a4-108"><span id="l_"></span><span id="L_"></span>*l\#*</span><span class="sxs-lookup"><span data-stu-id="cb8a4-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="cb8a4-109">\[nell' \] etichetta della subroutine.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-109">\[in\] The label of the subroutine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb8a4-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb8a4-110">Remarks</span></span>

<span data-ttu-id="cb8a4-111">Quando viene rilevata una [ret](ret--sm4---asm-.md) , restituisce l'esecuzione all'istruzione dopo questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-111">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="cb8a4-112">Il formato del token contiene l'offset dell'etichetta corrispondente nello shader per praticità.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-112">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="cb8a4-113">Nell'esempio seguente viene illustrata l'istruzione Call.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-113">The following example shows the call instruction.</span></span>


```
                ...
                call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret
```



### <a name="restrictions"></a><span data-ttu-id="cb8a4-114">Restrizioni</span><span class="sxs-lookup"><span data-stu-id="cb8a4-114">Restrictions</span></span>

-   <span data-ttu-id="cb8a4-115">Le subroutine possono annidare 32 a fondo.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-115">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="cb8a4-116">Lo stack degli indirizzi restituiti viene gestito in modo trasparente dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-116">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="cb8a4-117">Se sono già presenti 32 voci nello stack di indirizzi restituiti e viene eseguita una **chiamata** , la chiamata viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-117">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="cb8a4-118">Nessun stack di parametri automatico.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-118">There is no automatic parameter stack.</span></span> <span data-ttu-id="cb8a4-119">L'applicazione può usare una matrice di registro temporanea indicizzabile (x \# \[ \] ) per implementare manualmente uno stack.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-119">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="cb8a4-120">Tuttavia, gli indirizzi restituiti della chiamata subroutine non sono visibili e sono ortogonali a qualsiasi gestione dello stack manuale eseguita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-120">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="cb8a4-121">L'indicizzazione del parametro *l \#* non è consentita.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-121">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="cb8a4-122">La ricorsione non è consentita.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-122">Recursion is not permitted.</span></span>

<span data-ttu-id="cb8a4-123">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb8a4-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cb8a4-124">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="cb8a4-124">Vertex Shader</span></span> | <span data-ttu-id="cb8a4-125">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="cb8a4-125">Geometry Shader</span></span> | <span data-ttu-id="cb8a4-126">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="cb8a4-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="cb8a4-127">x</span><span class="sxs-lookup"><span data-stu-id="cb8a4-127">x</span></span>             | <span data-ttu-id="cb8a4-128">x</span><span class="sxs-lookup"><span data-stu-id="cb8a4-128">x</span></span>               | <span data-ttu-id="cb8a4-129">x</span><span class="sxs-lookup"><span data-stu-id="cb8a4-129">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cb8a4-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="cb8a4-130">Minimum Shader Model</span></span>

<span data-ttu-id="cb8a4-131">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="cb8a4-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cb8a4-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="cb8a4-132">Shader Model</span></span>                                              | <span data-ttu-id="cb8a4-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="cb8a4-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cb8a4-134">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="cb8a4-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cb8a4-135">sì</span><span class="sxs-lookup"><span data-stu-id="cb8a4-135">yes</span></span>       |
| [<span data-ttu-id="cb8a4-136">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="cb8a4-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cb8a4-137">sì</span><span class="sxs-lookup"><span data-stu-id="cb8a4-137">yes</span></span>       |
| [<span data-ttu-id="cb8a4-138">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="cb8a4-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cb8a4-139">sì</span><span class="sxs-lookup"><span data-stu-id="cb8a4-139">yes</span></span>       |
| [<span data-ttu-id="cb8a4-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb8a4-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cb8a4-141">no</span><span class="sxs-lookup"><span data-stu-id="cb8a4-141">no</span></span>        |
| [<span data-ttu-id="cb8a4-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb8a4-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cb8a4-143">no</span><span class="sxs-lookup"><span data-stu-id="cb8a4-143">no</span></span>        |
| [<span data-ttu-id="cb8a4-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb8a4-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cb8a4-145">no</span><span class="sxs-lookup"><span data-stu-id="cb8a4-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cb8a4-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb8a4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb8a4-147">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb8a4-147">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





