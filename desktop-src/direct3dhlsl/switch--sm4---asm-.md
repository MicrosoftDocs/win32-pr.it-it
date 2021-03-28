---
title: Switch (SM4-ASM)
description: Trasferisce il controllo a un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046088"
---
# <a name="switch-sm4---asm"></a><span data-ttu-id="883a5-103">Switch (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="883a5-103">switch (sm4 - asm)</span></span>

<span data-ttu-id="883a5-104">Trasferisce il controllo a un blocco di istruzioni diverso all'interno del corpo del commutatore a seconda del valore di un selettore.</span><span class="sxs-lookup"><span data-stu-id="883a5-104">Transfers control to a different statement block within the switch body depending on the value of a selector.</span></span>



| <span data-ttu-id="883a5-105">cambia il componente src0. Selected \_</span><span class="sxs-lookup"><span data-stu-id="883a5-105">switch src0.selected\_component</span></span> |
|---------------------------------|



 



| <span data-ttu-id="883a5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="883a5-106">Item</span></span>                                                            | <span data-ttu-id="883a5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="883a5-107">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="883a5-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="883a5-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="883a5-109">\[nel \] selettore per l'istruzione switch.</span><span class="sxs-lookup"><span data-stu-id="883a5-109">\[in\] The selector for the switch statement.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="883a5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="883a5-110">Remarks</span></span>

<span data-ttu-id="883a5-111">Un  / costrutto Switch [endswitch](endswitch--sm4---asm-.md) si comporta esattamente come un costrutto **Switch** nel linguaggio C, con la seguente eccezione: per le istruzioni predefinite del [case](case--sm4---asm-.md)d3d11 che passano fino / [](default--sm4---asm-.md) al  / **valore predefinito** del case successivo senza [interruzioni](break--sm4---asm-.md) non possono contenere codice.</span><span class="sxs-lookup"><span data-stu-id="883a5-111">A **switch**/[endswitch](endswitch--sm4---asm-.md) construct behaves exactly as a **switch** construct in the C language, with the following exception: for D3D11 [case](case--sm4---asm-.md)/[default](default--sm4---asm-.md) statements that fall through to the next **case**/**default** without a [break](break--sm4---asm-.md) cannot have any code in them.</span></span> <span data-ttu-id="883a5-112">È consentita la visualizzazione sequenziale di più istruzioni **case** , inclusa quella **predefinita**, che condividono lo stesso blocco di codice.</span><span class="sxs-lookup"><span data-stu-id="883a5-112">It is permitted for multiple **case** statements, including **default**, to appear sequentially, sharing the same code block.</span></span>

<span data-ttu-id="883a5-113">La condizione deve essere un componente di registro a 32 bit o una quantità immediata.</span><span class="sxs-lookup"><span data-stu-id="883a5-113">The condition must be a 32-bit register component or immediate quantity.</span></span> <span data-ttu-id="883a5-114">Il confronto di uguaglianza è bit per bit (Integer).</span><span class="sxs-lookup"><span data-stu-id="883a5-114">The equality comparison is bitwise (integer).</span></span>

<span data-ttu-id="883a5-115">Come per qualsiasi istruzione shader in D3D11, l'hardware può o meno implementare direttamente il costrutto **Switch** .</span><span class="sxs-lookup"><span data-stu-id="883a5-115">As with any Shader instruction in the D3D11, hardware may or may not implement the **switch** construct directly.</span></span>

<span data-ttu-id="883a5-116">Le istruzioni **Switch** possono essere annidate.</span><span class="sxs-lookup"><span data-stu-id="883a5-116">**Switch** statements can be nested.</span></span> <span data-ttu-id="883a5-117">Ogni blocco **Switch** viene conteggiato come 1 livello rispetto al limite di profondità di nidificazione del controllo di flusso di 64 per subroutine e Main, indipendentemente dal numero di istruzioni **case** .</span><span class="sxs-lookup"><span data-stu-id="883a5-117">Each **switch** block counts as 1 level against the flow control nesting depth limit of 64 per subroutine and main, independent of the number of **case** statements.</span></span> <span data-ttu-id="883a5-118">Il compilatore HLSL non genererà subroutine che superano questo limite.</span><span class="sxs-lookup"><span data-stu-id="883a5-118">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="883a5-119">Il comportamento delle istruzioni del flusso di controllo oltre 64 livelli di profondità per subroutine non è definito.</span><span class="sxs-lookup"><span data-stu-id="883a5-119">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="883a5-120">Nell'esempio seguente viene illustrato come utilizzare questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="883a5-120">The following example shows how to use this instruction.</span></span>

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
```

<span data-ttu-id="883a5-121">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="883a5-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="883a5-122">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="883a5-122">Vertex Shader</span></span> | <span data-ttu-id="883a5-123">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="883a5-123">Geometry Shader</span></span> | <span data-ttu-id="883a5-124">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="883a5-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="883a5-125">x</span><span class="sxs-lookup"><span data-stu-id="883a5-125">x</span></span>             | <span data-ttu-id="883a5-126">x</span><span class="sxs-lookup"><span data-stu-id="883a5-126">x</span></span>               | <span data-ttu-id="883a5-127">x</span><span class="sxs-lookup"><span data-stu-id="883a5-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="883a5-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="883a5-128">Minimum Shader Model</span></span>

<span data-ttu-id="883a5-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="883a5-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="883a5-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="883a5-130">Shader Model</span></span>                                              | <span data-ttu-id="883a5-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="883a5-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="883a5-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="883a5-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="883a5-133">sì</span><span class="sxs-lookup"><span data-stu-id="883a5-133">yes</span></span>       |
| [<span data-ttu-id="883a5-134">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="883a5-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="883a5-135">sì</span><span class="sxs-lookup"><span data-stu-id="883a5-135">yes</span></span>       |
| [<span data-ttu-id="883a5-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="883a5-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="883a5-137">sì</span><span class="sxs-lookup"><span data-stu-id="883a5-137">yes</span></span>       |
| [<span data-ttu-id="883a5-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="883a5-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="883a5-139">no</span><span class="sxs-lookup"><span data-stu-id="883a5-139">no</span></span>        |
| [<span data-ttu-id="883a5-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="883a5-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="883a5-141">no</span><span class="sxs-lookup"><span data-stu-id="883a5-141">no</span></span>        |
| [<span data-ttu-id="883a5-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="883a5-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="883a5-143">no</span><span class="sxs-lookup"><span data-stu-id="883a5-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="883a5-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="883a5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="883a5-145">Assembly Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="883a5-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





