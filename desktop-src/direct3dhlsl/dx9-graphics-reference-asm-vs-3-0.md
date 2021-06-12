---
title: vs_3_0
description: Informazioni su vs_3_0, un vertex shader programmabile, costituito da un set di istruzioni che operano sui dati dei vertici.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 310d64170280053c34766f214969f78d66560ea3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011074"
---
# <a name="vs_3_0"></a><span data-ttu-id="3c433-103">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c433-103">vs\_3\_0</span></span>

<span data-ttu-id="3c433-104">Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="3c433-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="3c433-105">Registra i dati di trasferimento in e all'uscita dall'ALU.</span><span class="sxs-lookup"><span data-stu-id="3c433-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="3c433-106">È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="3c433-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="3c433-107">Vertex shader versione \_ 3 \_ 0 estende il set di funzionalità supportato da vs \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="3c433-107">Vertex shader version vs\_3\_0 extends the feature set supported by vs\_2\_x.</span></span> <span data-ttu-id="3c433-108">Ognuna delle funzionalità in vs 2 X che richiede l'impostazione di un limite, è disponibile in vs \_ \_ \_ 3 \_ 0 senza richiedere il limite.</span><span class="sxs-lookup"><span data-stu-id="3c433-108">Each of the features in vs\_2\_X that requires a cap to be set, is available in vs\_3\_0 without requiring the cap.</span></span>

-   <span data-ttu-id="3c433-109">[Istruzioni : rispetto \_ a 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contiene un elenco delle istruzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="3c433-109">[Instructions - vs\_3\_0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="3c433-110">[Registri: rispetto a \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) sono elencati i diversi tipi di registri usati dal vertex shader ALU.</span><span class="sxs-lookup"><span data-stu-id="3c433-110">[Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="3c433-111">[I modificatori di registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare il funzionamento di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="3c433-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="3c433-112">[I modificatori del registro di origine vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="3c433-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="3c433-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.</span><span class="sxs-lookup"><span data-stu-id="3c433-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="3c433-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quali componenti del registro di destinazione vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="3c433-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="3c433-115">Nuove funzioni e caratteristiche</span><span class="sxs-lookup"><span data-stu-id="3c433-115">New Features</span></span>

<span data-ttu-id="3c433-116">Le nuove funzionalità di vertex shader versione \_ 3 \_ 0 sono elencate nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3c433-116">New features of vertex shader version vs\_3\_0 are listed in the following sections.</span></span>

### <a name="indexing-registers"></a><span data-ttu-id="3c433-117">Registri di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="3c433-117">Indexing Registers</span></span>

<span data-ttu-id="3c433-118">Nei modelli shader precedenti è possibile indicizzare solo la banca dei registri costanti.</span><span class="sxs-lookup"><span data-stu-id="3c433-118">In the earlier shader models, only the constant register bank could be indexed.</span></span> <span data-ttu-id="3c433-119">In questo modello è possibile indicizzare le banche di registro seguenti usando il registro dei contatori del ciclo (aL):</span><span class="sxs-lookup"><span data-stu-id="3c433-119">In this model, the following register banks can be indexed, using the loop counter register (aL):</span></span>

-   <span data-ttu-id="3c433-120">Registro di input (v \# )</span><span class="sxs-lookup"><span data-stu-id="3c433-120">Input register (v\#)</span></span>
-   <span data-ttu-id="3c433-121">Registro di output (o \# )</span><span class="sxs-lookup"><span data-stu-id="3c433-121">Output register (o\#)</span></span>

### <a name="vertex-textures"></a><span data-ttu-id="3c433-122">Trame dei vertici</span><span class="sxs-lookup"><span data-stu-id="3c433-122">Vertex Textures</span></span>

<span data-ttu-id="3c433-123">Questo modello shader supporta la ricerca di trame nel vertex shader usando texldl.</span><span class="sxs-lookup"><span data-stu-id="3c433-123">This shader model supports texture lookup in the vertex shader using texldl.</span></span> <span data-ttu-id="3c433-124">Il motore dei vertici ha quattro fasi del campionatore di trama (distinte dal campionatore mappa di spostamento e dai campionatori di trama nel motore pixel) che possono essere usate per campionare le trame impostate in tali fasi.</span><span class="sxs-lookup"><span data-stu-id="3c433-124">The vertex engine has four texture sampler stages (distinct from the displacement map sampler and the texture samplers in the pixel engine) that can be used to sample textures set at those stages.</span></span> <span data-ttu-id="3c433-125">Vedere [Trame vertice in vs \_ 3 \_ 0 (DirectX HLSL).](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)</span><span class="sxs-lookup"><span data-stu-id="3c433-125">See [Vertex Textures in vs\_3\_0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span></span>

### <a name="vertex-stream-frequency"></a><span data-ttu-id="3c433-126">Frequenza del flusso dei vertici</span><span class="sxs-lookup"><span data-stu-id="3c433-126">Vertex Stream Frequency</span></span>

<span data-ttu-id="3c433-127">Questa funzionalità consente l'inizializzazione di un subset dei registri di input a una velocità diversa da una volta per vertice.</span><span class="sxs-lookup"><span data-stu-id="3c433-127">This feature allows a subset of the input registers to be initialized at a rate different from once per vertex.</span></span> <span data-ttu-id="3c433-128">Vedere [Disegno di geometrie non indicizzate.](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry)</span><span class="sxs-lookup"><span data-stu-id="3c433-128">See [Drawing Non-Indexed Geometry](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span></span>

### <a name="shader-output"></a><span data-ttu-id="3c433-129">Shader Output</span><span class="sxs-lookup"><span data-stu-id="3c433-129">Shader Output</span></span>

<span data-ttu-id="3c433-130">Analogamente a vs \_ 2 \_ 0, l'output dello shader può variare con il controllo di flusso statico.</span><span class="sxs-lookup"><span data-stu-id="3c433-130">Similar to vs\_2\_0, the output of the shader can vary with static flow control.</span></span> <span data-ttu-id="3c433-131">Prestare attenzione con la diramazione dinamica, in quanto ciò può causare variazioni degli output dello shader per vertice.</span><span class="sxs-lookup"><span data-stu-id="3c433-131">Be careful with dynamic branching as this can cause shader outputs to vary per vertex.</span></span> <span data-ttu-id="3c433-132">Ciò produrrà risultati imprevedibili su hardware diverso.</span><span class="sxs-lookup"><span data-stu-id="3c433-132">This will produce unpredictable results on different hardware.</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="3c433-133">Controllo dinamico del flusso</span><span class="sxs-lookup"><span data-stu-id="3c433-133">Dynamic flow control</span></span>

<span data-ttu-id="3c433-134">Tutte le istruzioni di controllo dinamico del flusso sono supportate.</span><span class="sxs-lookup"><span data-stu-id="3c433-134">All dynamic flow control instructions are supported.</span></span> <span data-ttu-id="3c433-135">Il valore massimo di profondità di annidamento consentito è 24.</span><span class="sxs-lookup"><span data-stu-id="3c433-135">The maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="3c433-136">Per informazioni [dettagliate, vedere Limiti di annidamento del](dx9-graphics-reference-asm-vs-instructions-flow-control.md) controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="3c433-136">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="temporary-registers"></a><span data-ttu-id="3c433-137">Registri temporanei</span><span class="sxs-lookup"><span data-stu-id="3c433-137">Temporary Registers</span></span>

<span data-ttu-id="3c433-138">È supportato un totale di 32 registri temporanei (r \# ).</span><span class="sxs-lookup"><span data-stu-id="3c433-138">A total of 32 temporary registers (r\#) is supported.</span></span>

### <a name="static-flow-control"></a><span data-ttu-id="3c433-139">Controllo di flusso statico</span><span class="sxs-lookup"><span data-stu-id="3c433-139">Static Flow Control</span></span>

<span data-ttu-id="3c433-140">La profondità massima di annidamento [per il ciclo - vs](loop---vs.md)rep - rispetto / [a](rep---vs.md) 4.</span><span class="sxs-lookup"><span data-stu-id="3c433-140">The maximum nesting depth for [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) is 4.</span></span> <span data-ttu-id="3c433-141">La profondità di annidamento massima [per call - vs](call---vs.md) / [callnz bool - vs](callnz-bool---vs.md) / [callnz pred - rispetto a](callnz-pred---vs.md) 4.</span><span class="sxs-lookup"><span data-stu-id="3c433-141">The maximum nesting depth for [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[callnz pred - vs](callnz-pred---vs.md) is 4.</span></span> <span data-ttu-id="3c433-142">Per [se bool - vs](if-bool---vs.md), il valore massimo di profondità di annidamento consentito è 24.</span><span class="sxs-lookup"><span data-stu-id="3c433-142">For [if bool - vs](if-bool---vs.md), the maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="3c433-143">Per informazioni [dettagliate, vedere Limiti di annidamento del](dx9-graphics-reference-asm-vs-instructions-flow-control.md) controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="3c433-143">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="predication"></a><span data-ttu-id="3c433-144">Predicazione</span><span class="sxs-lookup"><span data-stu-id="3c433-144">Predication</span></span>

<span data-ttu-id="3c433-145">La predicazione dell'istruzione è supportata.</span><span class="sxs-lookup"><span data-stu-id="3c433-145">Instruction predication is supported.</span></span> <span data-ttu-id="3c433-146">Usare [setp \_ comp - vs per](setp-comp---vs.md) impostare il registro predicati.</span><span class="sxs-lookup"><span data-stu-id="3c433-146">Use [setp\_comp - vs](setp-comp---vs.md) to set the predicate register.</span></span>

### <a name="instruction-count"></a><span data-ttu-id="3c433-147">Conteggio istruzioni</span><span class="sxs-lookup"><span data-stu-id="3c433-147">Instruction Count</span></span>

<span data-ttu-id="3c433-148">Ogni vertex shader è consentito da 512 fino al numero di slot in MaxVertexShader30InstructionSlots in [**D3DCAPS9.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="3c433-148">Each vertex shader is allowed anywhere from 512 up to the number of slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> <span data-ttu-id="3c433-149">Il numero di istruzioni eseguite può essere molto più elevato a causa del supporto di ciclo/ripetizione. Tuttavia, questo limite è limitato da MaxVShaderInstructionsExecuted in D3DCAPS9, che deve essere almeno 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="3c433-149">The number of instructions run can be much higher because of the loop/rep support; however, this is capped by MaxVShaderInstructionsExecuted in D3DCAPS9 which should be at least 0xFFFF.</span></span>

### <a name="device-caps"></a><span data-ttu-id="3c433-150">Tappi dispositivo</span><span class="sxs-lookup"><span data-stu-id="3c433-150">Device Caps</span></span>

<span data-ttu-id="3c433-151">Se Vertex Shader 3 0 è supportato, nell'hardware sono supportati almeno i limiti \_ seguenti:</span><span class="sxs-lookup"><span data-stu-id="3c433-151">If Vertex Shader 3\_0 is supported, the following caps are supported in hardware (at a minimum):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c433-152">Cap</span><span class="sxs-lookup"><span data-stu-id="3c433-152">Cap</span></span></th>
<th><span data-ttu-id="3c433-153">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="3c433-153">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c433-154">Estremità dello shader</span><span class="sxs-lookup"><span data-stu-id="3c433-154">Shader caps</span></span></td>
<td><ul>
<li><span data-ttu-id="3c433-155">DynamicFlowControlDepth è 24</span><span class="sxs-lookup"><span data-stu-id="3c433-155">DynamicFlowControlDepth is 24</span></span></li>
<li><span data-ttu-id="3c433-156">NumTemps è 32</span><span class="sxs-lookup"><span data-stu-id="3c433-156">NumTemps is 32</span></span></li>
<li><span data-ttu-id="3c433-157">StaticFlowControlDepth è 4</span><span class="sxs-lookup"><span data-stu-id="3c433-157">StaticFlowControlDepth is 4</span></span></li>
<li><span data-ttu-id="3c433-158">La predicazione è supportata.</span><span class="sxs-lookup"><span data-stu-id="3c433-158">Predication is supported.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c433-159">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span><span class="sxs-lookup"><span data-stu-id="3c433-159">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span></span></td>
<td><span data-ttu-id="3c433-160">8 K</span><span class="sxs-lookup"><span data-stu-id="3c433-160">8K</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c433-161">VertexShaderVersion</span><span class="sxs-lookup"><span data-stu-id="3c433-161">VertexShaderVersion</span></span></td>
<td><span data-ttu-id="3c433-162">3_0</span><span class="sxs-lookup"><span data-stu-id="3c433-162">3_0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c433-163">MaxVertexShaderConst</span><span class="sxs-lookup"><span data-stu-id="3c433-163">MaxVertexShaderConst</span></span></td>
<td><span data-ttu-id="3c433-164">256</span><span class="sxs-lookup"><span data-stu-id="3c433-164">256</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c433-165">MaxVertexShader30InstructionSlots</span><span class="sxs-lookup"><span data-stu-id="3c433-165">MaxVertexShader30InstructionSlots</span></span></td>
<td><span data-ttu-id="3c433-166">512</span><span class="sxs-lookup"><span data-stu-id="3c433-166">512</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c433-167">Supporto di Osanna</span><span class="sxs-lookup"><span data-stu-id="3c433-167">Fog support</span></span></td>
<td><span data-ttu-id="3c433-168">D3DPRASTERCAPS_FOGVERTEX</span><span class="sxs-lookup"><span data-stu-id="3c433-168">D3DPRASTERCAPS_FOGVERTEX</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c433-169">VertexTextureFilterCaps</span><span class="sxs-lookup"><span data-stu-id="3c433-169">VertexTextureFilterCaps</span></span></td>
<td><ul>
<li><span data-ttu-id="3c433-170"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="3c433-170"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span></span></li>
<li><span data-ttu-id="3c433-171"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="3c433-171"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c433-172"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span><span class="sxs-lookup"><span data-stu-id="3c433-172"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span></span></td>
<td><span data-ttu-id="3c433-173">Gli elementi vertice in una dichiarazione di vertice possono condividere lo stesso offset del flusso.</span><span class="sxs-lookup"><span data-stu-id="3c433-173">Vertex elements in a vertex declaration can share the same stream offset.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c433-174">Formati dei vertici</span><span class="sxs-lookup"><span data-stu-id="3c433-174">Vertex formats</span></span></td>
<td><ul>
<li><span data-ttu-id="3c433-175">D3DDECLTYPE_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="3c433-175">D3DDECLTYPE_UBYTE4</span></span></li>
<li><span data-ttu-id="3c433-176">D3DDECLTYPE_UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="3c433-176">D3DDECLTYPE_UBYTE4N</span></span></li>
<li><span data-ttu-id="3c433-177">D3DDECLTYPE_SHORT2N</span><span class="sxs-lookup"><span data-stu-id="3c433-177">D3DDECLTYPE_SHORT2N</span></span></li>
<li><span data-ttu-id="3c433-178">D3DDECLTYPE_SHORT4N</span><span class="sxs-lookup"><span data-stu-id="3c433-178">D3DDECLTYPE_SHORT4N</span></span></li>
<li><span data-ttu-id="3c433-179">D3DDECLTYPE_FLOAT16_2</span><span class="sxs-lookup"><span data-stu-id="3c433-179">D3DDECLTYPE_FLOAT16_2</span></span></li>
<li><span data-ttu-id="3c433-180">D3DDECLTYPE_FLOAT16_4</span><span class="sxs-lookup"><span data-stu-id="3c433-180">D3DDECLTYPE_FLOAT16_4</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3c433-181">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c433-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c433-182">Vertex Shader</span><span class="sxs-lookup"><span data-stu-id="3c433-182">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 