---
title: ps_2_x
description: Informazioni su ps_2_x, un pixel shader programmabile, costituito da un set di istruzioni che operano sui dati pixel.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9efedc6011cb63b6465fd2d3ced4a7807c09f4da
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010874"
---
# <a name="ps_2_x"></a><span data-ttu-id="87688-103">ps \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="87688-103">ps\_2\_x</span></span>

<span data-ttu-id="87688-104">Un'pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel.</span><span class="sxs-lookup"><span data-stu-id="87688-104">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="87688-105">Registra i dati di trasferimento in e all'uscita dall'ALU.</span><span class="sxs-lookup"><span data-stu-id="87688-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="87688-106">È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="87688-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="87688-107">[ps \_ 2 \_ x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contiene un elenco delle istruzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="87688-107">[ps\_2\_x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="87688-108">[ps \_ 2 \_ x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) elenca i diversi tipi di registri usati dal vertex shader ALU.</span><span class="sxs-lookup"><span data-stu-id="87688-108">[ps\_2\_x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="87688-109">[Modificatori](dx9-graphics-reference-asm-ps-registers-modifiers.md) Vengono usati per modificare il funzionamento di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="87688-109">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="87688-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quali componenti del registro di destinazione vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="87688-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="87688-111">[I modificatori del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) pixel shader modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="87688-111">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="87688-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.</span><span class="sxs-lookup"><span data-stu-id="87688-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="dynamic-flow-control"></a><span data-ttu-id="87688-113">Controllo dinamico del flusso</span><span class="sxs-lookup"><span data-stu-id="87688-113">Dynamic Flow Control</span></span>

<span data-ttu-id="87688-114">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) rappresenta la profondità di annidamento delle istruzioni di controllo dinamico del flusso: [se](if-bool---ps.md), [se \_ comp](if-comp---ps.md), [se \_ pred](if-pred---ps.md), [break - ps](break---ps.md)e break comp - [ \_ ps](break-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="87688-114">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of dynamic flow control instructions: [if](if-bool---ps.md), [if\_comp](if-comp---ps.md), [if\_pred](if-pred---ps.md), [break - ps](break---ps.md), and [break\_comp - ps](break-comp---ps.md).</span></span> <span data-ttu-id="87688-115">Il valore è uguale alla profondità di annidamento del blocco se \_ comp.</span><span class="sxs-lookup"><span data-stu-id="87688-115">The value is equal to the nesting depth of the if\_comp block.</span></span> <span data-ttu-id="87688-116">Se questo limite è zero, il dispositivo non supporta le istruzioni di controllo dinamico del flusso.</span><span class="sxs-lookup"><span data-stu-id="87688-116">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

## <a name="number-of-temporary-registers"></a><span data-ttu-id="87688-117">Numero di registri temporanei</span><span class="sxs-lookup"><span data-stu-id="87688-117">Number of Temporary Registers</span></span>

<span data-ttu-id="87688-118">Numero di registri temporanei supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87688-118">The number of temporary registers supported by the device.</span></span> <span data-ttu-id="87688-119">L'intervallo è compreso tra 12 e 32.</span><span class="sxs-lookup"><span data-stu-id="87688-119">The range is from 12 to 32.</span></span>

## <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="87688-120">Profondità di annidamento del controllo flusso statico</span><span class="sxs-lookup"><span data-stu-id="87688-120">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="87688-121">[**StaticFlowControlDepth rappresenta**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) la profondità di annidamento di due tipi di istruzioni di controllo di flusso statiche: [ripetizione](loop---ps.md)del ciclo  / [](rep---ps.md) e [chiamata](call---ps.md)  / [callnz](callnz-bool---ps.md).</span><span class="sxs-lookup"><span data-stu-id="87688-121">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of two types of static flow control instructions: [loop](loop---ps.md) /[rep](rep---ps.md) And [call](call---ps.md) /[callnz](callnz-bool---ps.md).</span></span> <span data-ttu-id="87688-122">Le istruzioni loop /rep possono essere annidate fino a **StaticFlowControlDepth** deep.</span><span class="sxs-lookup"><span data-stu-id="87688-122">loop /rep instructions can be nested up to **StaticFlowControlDepth** deep.</span></span> <span data-ttu-id="87688-123">In modo indipendente, le istruzioni call /callnz possono essere annidate fino a **StaticFlowControlDepth** deep.</span><span class="sxs-lookup"><span data-stu-id="87688-123">Independently, call /callnz instructions can be nested up to **StaticFlowControlDepth** deep.</span></span>

## <a name="number-of-instruction-slots"></a><span data-ttu-id="87688-124">Numero di slot di istruzioni</span><span class="sxs-lookup"><span data-stu-id="87688-124">Number of Instruction Slots</span></span>

<span data-ttu-id="87688-125">Il numero di slot di istruzioni può variare da 96 a un massimo di 512 ed è specificato da [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span><span class="sxs-lookup"><span data-stu-id="87688-125">The number of instruction slots can range from 96 to a maximum of 512, and is specified by the [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span></span> <span data-ttu-id="87688-126">Il numero totale di istruzioni che è possibile eseguire è definito da **MaxPixelShaderInstructionsExecuted**.</span><span class="sxs-lookup"><span data-stu-id="87688-126">The total number of instructions that can run is defined by **MaxPixelShaderInstructionsExecuted**.</span></span> <span data-ttu-id="87688-127">Può essere maggiore del numero di slot di istruzioni a causa di chiamate a cicli e subroutine.</span><span class="sxs-lookup"><span data-stu-id="87688-127">This can be larger than the number of instruction slots due to looping and subroutine calls.</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="87688-128">Swizzle arbitrario</span><span class="sxs-lookup"><span data-stu-id="87688-128">Arbitrary Swizzle</span></span>

<span data-ttu-id="87688-129">Se [**è impostato D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) è supportato lo scorrimento arbitrario.</span><span class="sxs-lookup"><span data-stu-id="87688-129">If [**D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, arbitrary swizzle is supported.</span></span> <span data-ttu-id="87688-130">Vedere [Swizzling del registro di origine.](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)</span><span class="sxs-lookup"><span data-stu-id="87688-130">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="gradient-instructions"></a><span data-ttu-id="87688-131">Istruzioni per la sfumatura</span><span class="sxs-lookup"><span data-stu-id="87688-131">Gradient Instructions</span></span>

<span data-ttu-id="87688-132">Se [**è impostato D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) sono supportate le istruzioni per la sfumatura.</span><span class="sxs-lookup"><span data-stu-id="87688-132">If [**D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, gradient instructions are supported.</span></span> <span data-ttu-id="87688-133">Vedere [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)e [texldd - ps](texldd---ps.md).</span><span class="sxs-lookup"><span data-stu-id="87688-133">See [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md), and [texldd - ps](texldd---ps.md).</span></span>

## <a name="predication"></a><span data-ttu-id="87688-134">Predicazione</span><span class="sxs-lookup"><span data-stu-id="87688-134">Predication</span></span>

<span data-ttu-id="87688-135">Se [**la predicazione D3DD3DPSHADERCAPS2 \_ 0 \_**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) è impostata, la predicazione dell'istruzione è supportata.</span><span class="sxs-lookup"><span data-stu-id="87688-135">If [**D3DD3DPSHADERCAPS2\_0\_PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, instruction predication is supported.</span></span> <span data-ttu-id="87688-136">Vedere [Registro predicati](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="87688-136">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

## <a name="dependent-read-limit"></a><span data-ttu-id="87688-137">Limite di lettura dipendente</span><span class="sxs-lookup"><span data-stu-id="87688-137">Dependent Read Limit</span></span>

<span data-ttu-id="87688-138">Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) è impostato, non sono previsti limiti di lettura dipendenti.</span><span class="sxs-lookup"><span data-stu-id="87688-138">If [**D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there are no dependent read limits.</span></span>

## <a name="texture-instruction-limit"></a><span data-ttu-id="87688-139">Limite istruzioni trama</span><span class="sxs-lookup"><span data-stu-id="87688-139">Texture Instruction Limit</span></span>

<span data-ttu-id="87688-140">Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) è impostato, non esiste alcun limite per le istruzioni di trama.</span><span class="sxs-lookup"><span data-stu-id="87688-140">If [**D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there is no limit on texture instructions.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="87688-141">Conteggio campionatore</span><span class="sxs-lookup"><span data-stu-id="87688-141">Sampler Count</span></span>

<span data-ttu-id="87688-142">Il numero di campionatori di trama disponibili è 16.</span><span class="sxs-lookup"><span data-stu-id="87688-142">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87688-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87688-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87688-144">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="87688-144">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 