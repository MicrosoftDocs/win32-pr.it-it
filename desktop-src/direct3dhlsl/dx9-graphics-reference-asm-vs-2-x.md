---
title: vs_2_x
description: Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d09af016ca4fd399de0f2aeec1267343b9d11574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473755"
---
# <a name="vs_2_x"></a><span data-ttu-id="f1eb6-105">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f1eb6-105">vs\_2\_x</span></span>

<span data-ttu-id="f1eb6-106">Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="f1eb6-107">Registra i dati di trasferimento all'interno e all'esterno dell'ALU.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="f1eb6-108">È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="f1eb6-109">Vertex shader versione vs \_ 2 \_ x estende il set di funzionalità supportato da vs \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-109">Vertex shader version vs\_2\_x extends the feature set supported by vs\_2\_0.</span></span> <span data-ttu-id="f1eb6-110">Ogni funzionalità aggiuntiva è rappresentata da un limite corrispondente nella struttura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) all'interno di [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span><span class="sxs-lookup"><span data-stu-id="f1eb6-110">Each additional feature is represented by a corresponding cap in the [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure within [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span></span> <span data-ttu-id="f1eb6-111">Per usare una delle funzionalità avanzate rappresentate da questi limiti, è necessario specificare la versione di vertex shader come vs \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-111">To use any of the enhanced features represented by these caps, the vertex shader version must be specified as vs\_2\_x.</span></span>

-   <span data-ttu-id="f1eb6-112">[Istruzioni: vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contiene un elenco delle istruzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-112">[Instructions - vs\_2\_x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="f1eb6-113">[Registers-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) elenca i diversi tipi di registri usati da vertex shader Alu.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-113">[Registers - vs\_2\_x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="f1eb6-114">I [modificatori del registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare la modalità di funzionamento di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-114">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="f1eb6-115">I [modificatori del registro di origine vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-115">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="f1eb6-116">Il [Registro di origine swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornisce un controllo aggiuntivo sui componenti di registro letti, copiati o scritti.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-116">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="f1eb6-117">Il [mascheramento del registro di destinazione](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quali componenti del registro di destinazione vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-117">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="f1eb6-118">Nuove funzioni e caratteristiche</span><span class="sxs-lookup"><span data-stu-id="f1eb6-118">New Features</span></span>

<span data-ttu-id="f1eb6-119">Le nuove funzionalità sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1eb6-119">New features are as follows:</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="f1eb6-120">Controllo dinamico di flusso</span><span class="sxs-lookup"><span data-stu-id="f1eb6-120">Dynamic Flow Control</span></span>

<span data-ttu-id="f1eb6-121">Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, sono supportate le istruzioni seguenti per il controllo dinamico del flusso:</span><span class="sxs-lookup"><span data-stu-id="f1eb6-121">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, then the following dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="f1eb6-122">Se \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="f1eb6-122">if\_comp - vs</span></span>](if-comp---vs.md)
-   [<span data-ttu-id="f1eb6-123">Break-vs</span><span class="sxs-lookup"><span data-stu-id="f1eb6-123">break - vs</span></span>](break---vs.md)
-   [<span data-ttu-id="f1eb6-124">Interrompi \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="f1eb6-124">break\_comp - vs</span></span>](break-comp---vs.md)

<span data-ttu-id="f1eb6-125">Se si imposta anche [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) , sono supportate le istruzioni aggiuntive per il controllo di flusso seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1eb6-125">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is also set, the following additional flow control instructions are supported:</span></span>

-   [<span data-ttu-id="f1eb6-126">setp \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="f1eb6-126">setp\_comp - vs</span></span>](setp-comp---vs.md)
-   [<span data-ttu-id="f1eb6-127">Se prede-vs</span><span class="sxs-lookup"><span data-stu-id="f1eb6-127">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="f1eb6-128">callnz Predator-vs</span><span class="sxs-lookup"><span data-stu-id="f1eb6-128">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="f1eb6-129">Breakp-vs</span><span class="sxs-lookup"><span data-stu-id="f1eb6-129">breakp - vs</span></span>](breakp---vs.md)

<span data-ttu-id="f1eb6-130">L'intervallo di valori per la profondità del controllo di flusso dinamico è compreso tra 0 e 24 ed è uguale alla profondità di annidamento delle istruzioni di controllo del flusso dinamico. per informazioni dettagliate, vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md) .</span><span class="sxs-lookup"><span data-stu-id="f1eb6-130">The range of values for dynamic flow control depth is 0 to 24 and is equal to the nesting depth of the dynamic flow control instructions (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span> <span data-ttu-id="f1eb6-131">Se questo limite è pari a zero, il dispositivo non supporta le istruzioni per il controllo dinamico dei flussi.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-131">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

### <a name="number-of-temporary-registers"></a><span data-ttu-id="f1eb6-132">Numero di registri temporanei</span><span class="sxs-lookup"><span data-stu-id="f1eb6-132">Number of Temporary Registers</span></span>

<span data-ttu-id="f1eb6-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) rappresenta il numero di [registri temporanei](dx9-graphics-reference-asm-vs-registers-temporary.md)supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s supported by the device.</span></span> <span data-ttu-id="f1eb6-134">L'intervallo di valori per questo limite è 12-32.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-134">The range of values for this cap is 12 to 32.</span></span>

### <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="f1eb6-135">Profondità di annidamento del controllo di flusso statico</span><span class="sxs-lookup"><span data-stu-id="f1eb6-135">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="f1eb6-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) rappresenta la profondità di annidamento di due tipi di istruzioni di controllo di flusso statiche: le istruzioni [loop-vs](loop---vs.md) / [Rep-vs](rep---vs.md) e [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [se bool-vs](if-bool---vs.md). loop-vs/Rep-vs possono essere nidificate fino a D3DVS20CAPS Deep.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the nesting depth of two types of static flow control instructions: [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) and [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[if bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="f1eb6-137">In modo indipendente, le istruzioni Call-vs/callnz bool-vs possono essere nidificate fino a D3DVS20CAPS Deep.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-137">Independently, call - vs/callnz bool - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="f1eb6-138">Se viene impostato anche D3DVS20CAPS, [callnz prede-vs](callnz-pred---vs.md) viene conteggiato nella profondità di annidamento di Call-vs/callnz bool-vs/if bool-vs (vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md) per informazioni dettagliate).</span><span class="sxs-lookup"><span data-stu-id="f1eb6-138">If D3DVS20CAPS is also set, then [callnz pred - vs](callnz-pred---vs.md) is counted toward the nesting depth of call - vs/callnz bool - vs/if bool - vs (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span>

### <a name="predication"></a><span data-ttu-id="f1eb6-139">Predicazione</span><span class="sxs-lookup"><span data-stu-id="f1eb6-139">Predication</span></span>

<span data-ttu-id="f1eb6-140">Se è impostato [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) , il dispositivo supporta [setp \_ comp-vs](setp-comp---vs.md) e l'istruzione predicazione.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-140">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is set, the device supports [setp\_comp - vs](setp-comp---vs.md) and instruction predication.</span></span> <span data-ttu-id="f1eb6-141">Se anche D3DVS20CAPS è maggiore di 0, sono supportate le istruzioni aggiuntive per il controllo di flusso dinamico seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1eb6-141">If D3DVS20CAPS is also greater than 0, then the following additional dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="f1eb6-142">Se prede-vs</span><span class="sxs-lookup"><span data-stu-id="f1eb6-142">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="f1eb6-143">callnz Predator-vs</span><span class="sxs-lookup"><span data-stu-id="f1eb6-143">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="f1eb6-144">Breakp-vs</span><span class="sxs-lookup"><span data-stu-id="f1eb6-144">breakp - vs</span></span>](breakp---vs.md)

### <a name="instruction-count"></a><span data-ttu-id="f1eb6-145">Conteggio istruzioni</span><span class="sxs-lookup"><span data-stu-id="f1eb6-145">Instruction Count</span></span>

<span data-ttu-id="f1eb6-146">Ogni vertex shader può avere fino a 256 istruzioni archiviate.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-146">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="f1eb6-147">Il numero di istruzioni eseguite può essere molto più alto (a causa del supporto ciclo/Rep) ed è limitato da [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), che deve essere almeno 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="f1eb6-147">The number of instructions run can be much higher (because of the loop/rep support), and is capped by [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1eb6-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1eb6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1eb6-149">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="f1eb6-149">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 