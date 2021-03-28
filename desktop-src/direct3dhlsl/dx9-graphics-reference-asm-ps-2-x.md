---
title: ps_2_x
description: Un pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13e5daf7c3a4b41e5b27b1c20f8b1f5f8355c325
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993504"
---
# <a name="ps_2_x"></a><span data-ttu-id="4158d-105">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4158d-105">ps\_2\_x</span></span>

<span data-ttu-id="4158d-106">Un pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel.</span><span class="sxs-lookup"><span data-stu-id="4158d-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="4158d-107">Registra i dati di trasferimento all'interno e all'esterno dell'ALU.</span><span class="sxs-lookup"><span data-stu-id="4158d-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="4158d-108">È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="4158d-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="4158d-109">[le \_ istruzioni di PS 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contengono un elenco delle istruzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="4158d-109">[ps\_2\_x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="4158d-110">[i \_ registri di PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) elencano i diversi tipi di registri usati da vertex shader Alu.</span><span class="sxs-lookup"><span data-stu-id="4158d-110">[ps\_2\_x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="4158d-111">[Modificatori](dx9-graphics-reference-asm-ps-registers-modifiers.md) Consentono di modificare la modalità di funzionamento di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="4158d-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="4158d-112">La [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quali componenti del registro di destinazione vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="4158d-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="4158d-113">I [modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="4158d-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="4158d-114">Il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornisce un controllo aggiuntivo sui componenti di registro letti, copiati o scritti.</span><span class="sxs-lookup"><span data-stu-id="4158d-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="dynamic-flow-control"></a><span data-ttu-id="4158d-115">Controllo dinamico di flusso</span><span class="sxs-lookup"><span data-stu-id="4158d-115">Dynamic Flow Control</span></span>

<span data-ttu-id="4158d-116">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) rappresenta la profondità di annidamento delle istruzioni di controllo del flusso dinamico: [if](if-bool---ps.md), if [ \_ comp](if-comp---ps.md), [if \_ prede](if-pred---ps.md), [break-PS](break---ps.md)e [break \_ comp-PS](break-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="4158d-116">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of dynamic flow control instructions: [if](if-bool---ps.md), [if\_comp](if-comp---ps.md), [if\_pred](if-pred---ps.md), [break - ps](break---ps.md), and [break\_comp - ps](break-comp---ps.md).</span></span> <span data-ttu-id="4158d-117">Il valore è uguale alla profondità di nidificazione del blocco if \_ comp.</span><span class="sxs-lookup"><span data-stu-id="4158d-117">The value is equal to the nesting depth of the if\_comp block.</span></span> <span data-ttu-id="4158d-118">Se questo limite è pari a zero, il dispositivo non supporta le istruzioni per il controllo dinamico dei flussi.</span><span class="sxs-lookup"><span data-stu-id="4158d-118">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

## <a name="number-of-temporary-registers"></a><span data-ttu-id="4158d-119">Numero di registri temporanei</span><span class="sxs-lookup"><span data-stu-id="4158d-119">Number of Temporary Registers</span></span>

<span data-ttu-id="4158d-120">Numero di registri temporanei supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4158d-120">The number of temporary registers supported by the device.</span></span> <span data-ttu-id="4158d-121">L'intervallo è compreso tra 12 e 32.</span><span class="sxs-lookup"><span data-stu-id="4158d-121">The range is from 12 to 32.</span></span>

## <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="4158d-122">Profondità di annidamento del controllo di flusso statico</span><span class="sxs-lookup"><span data-stu-id="4158d-122">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="4158d-123">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) rappresenta la profondità di annidamento di due tipi di istruzioni di controllo di flusso statiche: Rep del [ciclo](loop---ps.md)  / [](rep---ps.md) e [chiamata](call---ps.md)  / [callnz](callnz-bool---ps.md).</span><span class="sxs-lookup"><span data-stu-id="4158d-123">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of two types of static flow control instructions: [loop](loop---ps.md) /[rep](rep---ps.md) And [call](call---ps.md) /[callnz](callnz-bool---ps.md).</span></span> <span data-ttu-id="4158d-124">le istruzioni Loop/Rep possono essere nidificate fino a **StaticFlowControlDepth** Deep.</span><span class="sxs-lookup"><span data-stu-id="4158d-124">loop /rep instructions can be nested up to **StaticFlowControlDepth** deep.</span></span> <span data-ttu-id="4158d-125">In modo indipendente, le istruzioni Call/callnz possono essere annidate fino a **StaticFlowControlDepth** Deep.</span><span class="sxs-lookup"><span data-stu-id="4158d-125">Independently, call /callnz instructions can be nested up to **StaticFlowControlDepth** deep.</span></span>

## <a name="number-of-instruction-slots"></a><span data-ttu-id="4158d-126">Numero di slot di istruzioni</span><span class="sxs-lookup"><span data-stu-id="4158d-126">Number of Instruction Slots</span></span>

<span data-ttu-id="4158d-127">Il numero di slot di istruzioni può essere compreso tra 96 e un massimo di 512 e viene specificato da [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span><span class="sxs-lookup"><span data-stu-id="4158d-127">The number of instruction slots can range from 96 to a maximum of 512, and is specified by the [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span></span> <span data-ttu-id="4158d-128">Il numero totale di istruzioni che è possibile eseguire è definito da **MaxPixelShaderInstructionsExecuted**.</span><span class="sxs-lookup"><span data-stu-id="4158d-128">The total number of instructions that can run is defined by **MaxPixelShaderInstructionsExecuted**.</span></span> <span data-ttu-id="4158d-129">Può essere maggiore del numero di slot di istruzioni a causa delle chiamate di ciclo e subroutine.</span><span class="sxs-lookup"><span data-stu-id="4158d-129">This can be larger than the number of instruction slots due to looping and subroutine calls.</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="4158d-130">Swizzle arbitrario</span><span class="sxs-lookup"><span data-stu-id="4158d-130">Arbitrary Swizzle</span></span>

<span data-ttu-id="4158d-131">Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , il swizzle arbitrario è supportato.</span><span class="sxs-lookup"><span data-stu-id="4158d-131">If [**D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, arbitrary swizzle is supported.</span></span> <span data-ttu-id="4158d-132">Vedere il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="4158d-132">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="gradient-instructions"></a><span data-ttu-id="4158d-133">Istruzioni gradiente</span><span class="sxs-lookup"><span data-stu-id="4158d-133">Gradient Instructions</span></span>

<span data-ttu-id="4158d-134">Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , sono supportate le istruzioni per la sfumatura.</span><span class="sxs-lookup"><span data-stu-id="4158d-134">If [**D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, gradient instructions are supported.</span></span> <span data-ttu-id="4158d-135">Vedere [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)e [texldd-PS](texldd---ps.md).</span><span class="sxs-lookup"><span data-stu-id="4158d-135">See [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md), and [texldd - ps](texldd---ps.md).</span></span>

## <a name="predication"></a><span data-ttu-id="4158d-136">Predicazione</span><span class="sxs-lookup"><span data-stu-id="4158d-136">Predication</span></span>

<span data-ttu-id="4158d-137">Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ predicazione**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , l'istruzione predicazione è supportata.</span><span class="sxs-lookup"><span data-stu-id="4158d-137">If [**D3DD3DPSHADERCAPS2\_0\_PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, instruction predication is supported.</span></span> <span data-ttu-id="4158d-138">Vedere [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="4158d-138">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

## <a name="dependent-read-limit"></a><span data-ttu-id="4158d-139">Limite di lettura dipendente</span><span class="sxs-lookup"><span data-stu-id="4158d-139">Dependent Read Limit</span></span>

<span data-ttu-id="4158d-140">Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , non esistono limiti di lettura dipendenti.</span><span class="sxs-lookup"><span data-stu-id="4158d-140">If [**D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there are no dependent read limits.</span></span>

## <a name="texture-instruction-limit"></a><span data-ttu-id="4158d-141">Limite istruzioni trama</span><span class="sxs-lookup"><span data-stu-id="4158d-141">Texture Instruction Limit</span></span>

<span data-ttu-id="4158d-142">Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , non esiste alcun limite per le istruzioni di trama.</span><span class="sxs-lookup"><span data-stu-id="4158d-142">If [**D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there is no limit on texture instructions.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="4158d-143">Numero di campionatori</span><span class="sxs-lookup"><span data-stu-id="4158d-143">Sampler Count</span></span>

<span data-ttu-id="4158d-144">Il numero di campioni di trama disponibili è 16.</span><span class="sxs-lookup"><span data-stu-id="4158d-144">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4158d-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4158d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4158d-146">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="4158d-146">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 