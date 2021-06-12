---
title: vs_2_x
description: Informazioni su vs_2_x, un vertex shader programmabile, costituito da un set di istruzioni che operano sui dati dei vertici.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3449ae4c1e1eb3b977916f6fb1d19303e9d21a4e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010715"
---
# <a name="vs_2_x"></a><span data-ttu-id="e3ede-103">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e3ede-103">vs\_2\_x</span></span>

<span data-ttu-id="e3ede-104">Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="e3ede-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="e3ede-105">Registra i dati di trasferimento in e da ALU.</span><span class="sxs-lookup"><span data-stu-id="e3ede-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="e3ede-106">È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="e3ede-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="e3ede-107">La versione vertex shader rispetto \_ alla versione 2 \_ x estende il set di funzionalità supportato da vs \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="e3ede-107">Vertex shader version vs\_2\_x extends the feature set supported by vs\_2\_0.</span></span> <span data-ttu-id="e3ede-108">Ogni funzionalità aggiuntiva è rappresentata da un limite corrispondente nella [**struttura D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) all'interno di [D3DVS20CAPS.](/windows/desktop/direct3d9/d3dvs20caps)</span><span class="sxs-lookup"><span data-stu-id="e3ede-108">Each additional feature is represented by a corresponding cap in the [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure within [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span></span> <span data-ttu-id="e3ede-109">Per usare una qualsiasi delle funzionalità avanzate rappresentate da queste estremità, la versione del vertex shader deve essere specificata come \_ vs 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="e3ede-109">To use any of the enhanced features represented by these caps, the vertex shader version must be specified as vs\_2\_x.</span></span>

-   <span data-ttu-id="e3ede-110">[Instructions - vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contiene un elenco delle istruzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="e3ede-110">[Instructions - vs\_2\_x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="e3ede-111">[Registri: rispetto \_ a 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) elenca i diversi tipi di registri usati dal vertex shader ALU.</span><span class="sxs-lookup"><span data-stu-id="e3ede-111">[Registers - vs\_2\_x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="e3ede-112">[I modificatori di registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare il funzionamento di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="e3ede-112">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="e3ede-113">[I modificatori del registro di origine vertex shader modificano](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) i dati del registro di origine prima dell'esecuzione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="e3ede-113">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="e3ede-114">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.</span><span class="sxs-lookup"><span data-stu-id="e3ede-114">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="e3ede-115">[Destination Register Masking determina](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) quali componenti del registro di destinazione vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="e3ede-115">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="e3ede-116">Nuove funzioni e caratteristiche</span><span class="sxs-lookup"><span data-stu-id="e3ede-116">New Features</span></span>

<span data-ttu-id="e3ede-117">Le nuove funzionalità sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3ede-117">New features are as follows:</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="e3ede-118">Controllo dinamico del flusso</span><span class="sxs-lookup"><span data-stu-id="e3ede-118">Dynamic Flow Control</span></span>

<span data-ttu-id="e3ede-119">Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, sono supportate le istruzioni di controllo dinamico del flusso seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3ede-119">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, then the following dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="e3ede-120">if \_ comp - vs</span><span class="sxs-lookup"><span data-stu-id="e3ede-120">if\_comp - vs</span></span>](if-comp---vs.md)
-   [<span data-ttu-id="e3ede-121">break - vs</span><span class="sxs-lookup"><span data-stu-id="e3ede-121">break - vs</span></span>](break---vs.md)
-   [<span data-ttu-id="e3ede-122">break \_ comp - vs</span><span class="sxs-lookup"><span data-stu-id="e3ede-122">break\_comp - vs</span></span>](break-comp---vs.md)

<span data-ttu-id="e3ede-123">Se [è impostato anche D3DVS20CAPS,](/windows/desktop/direct3d9/d3dvs20caps) sono supportate le istruzioni di controllo di flusso aggiuntive seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3ede-123">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is also set, the following additional flow control instructions are supported:</span></span>

-   [<span data-ttu-id="e3ede-124">setp \_ comp - vs</span><span class="sxs-lookup"><span data-stu-id="e3ede-124">setp\_comp - vs</span></span>](setp-comp---vs.md)
-   [<span data-ttu-id="e3ede-125">if pred - vs</span><span class="sxs-lookup"><span data-stu-id="e3ede-125">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="e3ede-126">callnz pred - vs</span><span class="sxs-lookup"><span data-stu-id="e3ede-126">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="e3ede-127">breakp - vs</span><span class="sxs-lookup"><span data-stu-id="e3ede-127">breakp - vs</span></span>](breakp---vs.md)

<span data-ttu-id="e3ede-128">L'intervallo di valori per la profondità del controllo dinamico del flusso è compreso tra 0 [](dx9-graphics-reference-asm-vs-instructions-flow-control.md) e 24 ed è uguale alla profondità di annidamento delle istruzioni di controllo dinamico del flusso.Per informazioni dettagliate, vedere Limiti di annidamento del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="e3ede-128">The range of values for dynamic flow control depth is 0 to 24 and is equal to the nesting depth of the dynamic flow control instructions (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span> <span data-ttu-id="e3ede-129">Se questo limite è zero, il dispositivo non supporta le istruzioni di controllo dinamico del flusso.</span><span class="sxs-lookup"><span data-stu-id="e3ede-129">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

### <a name="number-of-temporary-registers"></a><span data-ttu-id="e3ede-130">Numero di registri temporanei</span><span class="sxs-lookup"><span data-stu-id="e3ede-130">Number of Temporary Registers</span></span>

<span data-ttu-id="e3ede-131">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) rappresenta il [numero](dx9-graphics-reference-asm-vs-registers-temporary.md)di registri temporanei supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3ede-131">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s supported by the device.</span></span> <span data-ttu-id="e3ede-132">L'intervallo di valori per questo limite è compreso tra 12 e 32.</span><span class="sxs-lookup"><span data-stu-id="e3ede-132">The range of values for this cap is 12 to 32.</span></span>

### <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="e3ede-133">Profondità di annidamento del controllo di flusso statico</span><span class="sxs-lookup"><span data-stu-id="e3ede-133">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="e3ede-134">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) rappresenta la profondità di annidamento di due tipi di istruzioni di controllo di flusso statiche: [loop -](loop---vs.md)vs rep - vs e call - vs callnz bool - vs if bool - vs . loop - vs/rep - vs instructions può essere annidato fino a / [](rep---vs.md) [](call---vs.md) / [](callnz-bool---vs.md) / [](if-bool---vs.md)D3DVS20CAPS deep.</span><span class="sxs-lookup"><span data-stu-id="e3ede-134">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the nesting depth of two types of static flow control instructions: [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) and [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[if bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="e3ede-135">In modo indipendente, chiamare - vs/callnz bool - e le istruzioni possono essere annidate fino a D3DVS20CAPS deep.</span><span class="sxs-lookup"><span data-stu-id="e3ede-135">Independently, call - vs/callnz bool - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="e3ede-136">Se è impostato anche D3DVS20CAPS, chiamare [pred](callnz-pred---vs.md) - vs viene conteggiato per la profondità di annidamento della chiamata [](dx9-graphics-reference-asm-vs-instructions-flow-control.md) - vs/callnz bool - vs/if bool - vs (vedere Limiti di annidamento del controllo di flusso per informazioni dettagliate).</span><span class="sxs-lookup"><span data-stu-id="e3ede-136">If D3DVS20CAPS is also set, then [callnz pred - vs](callnz-pred---vs.md) is counted toward the nesting depth of call - vs/callnz bool - vs/if bool - vs (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span>

### <a name="predication"></a><span data-ttu-id="e3ede-137">Predicazione</span><span class="sxs-lookup"><span data-stu-id="e3ede-137">Predication</span></span>

<span data-ttu-id="e3ede-138">Se [è impostato D3DVS20CAPS,](/windows/desktop/direct3d9/d3dvs20caps) il dispositivo supporta [setp comp - \_ e](setp-comp---vs.md) il predicato dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="e3ede-138">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is set, the device supports [setp\_comp - vs](setp-comp---vs.md) and instruction predication.</span></span> <span data-ttu-id="e3ede-139">Se anche D3DVS20CAPS è maggiore di 0, sono supportate le istruzioni di controllo dinamico del flusso aggiuntive seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3ede-139">If D3DVS20CAPS is also greater than 0, then the following additional dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="e3ede-140">if pred - vs</span><span class="sxs-lookup"><span data-stu-id="e3ede-140">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="e3ede-141">callnz pred - vs</span><span class="sxs-lookup"><span data-stu-id="e3ede-141">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="e3ede-142">breakp - vs</span><span class="sxs-lookup"><span data-stu-id="e3ede-142">breakp - vs</span></span>](breakp---vs.md)

### <a name="instruction-count"></a><span data-ttu-id="e3ede-143">Conteggio istruzioni</span><span class="sxs-lookup"><span data-stu-id="e3ede-143">Instruction Count</span></span>

<span data-ttu-id="e3ede-144">Ogni vertex shader può contenere fino a 256 istruzioni archiviate.</span><span class="sxs-lookup"><span data-stu-id="e3ede-144">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="e3ede-145">Il numero di istruzioni eseguite può essere molto più elevato (a causa del supporto per cicli/rep) ed è limitato da [**D3DCAPS9,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)che deve essere almeno 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="e3ede-145">The number of instructions run can be much higher (because of the loop/rep support), and is capped by [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3ede-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3ede-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3ede-147">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="e3ede-147">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 