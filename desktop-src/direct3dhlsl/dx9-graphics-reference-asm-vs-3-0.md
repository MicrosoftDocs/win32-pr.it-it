---
title: vs_3_0
description: Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22a0e6e84aff34dcec44713dc4382e391ad05c2b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103873069"
---
# <a name="vs_3_0"></a><span data-ttu-id="e4eb9-105">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4eb9-105">vs\_3\_0</span></span>

<span data-ttu-id="e4eb9-106">Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="e4eb9-107">Registra i dati di trasferimento all'interno e all'esterno dell'ALU.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="e4eb9-108">È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="e4eb9-109">Vertex shader versione vs \_ 3 \_ 0 estende il set di funzionalità supportato da vs \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-109">Vertex shader version vs\_3\_0 extends the feature set supported by vs\_2\_x.</span></span> <span data-ttu-id="e4eb9-110">Ogni funzionalità di vs \_ 2 \_ X che richiede l'impostazione di un limite è disponibile in vs \_ 3 \_ 0 senza richiedere il limite.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-110">Each of the features in vs\_2\_X that requires a cap to be set, is available in vs\_3\_0 without requiring the cap.</span></span>

-   <span data-ttu-id="e4eb9-111">[Istruzioni-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contiene un elenco delle istruzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-111">[Instructions - vs\_3\_0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="e4eb9-112">[Registers-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) elenca i diversi tipi di registri usati da vertex shader Alu.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-112">[Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="e4eb9-113">I [modificatori del registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare la modalità di funzionamento di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-113">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="e4eb9-114">I [modificatori del registro di origine vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-114">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="e4eb9-115">Il [Registro di origine swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornisce un controllo aggiuntivo sui componenti di registro letti, copiati o scritti.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-115">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="e4eb9-116">Il [mascheramento del registro di destinazione](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quali componenti del registro di destinazione vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-116">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="e4eb9-117">Nuove funzioni e caratteristiche</span><span class="sxs-lookup"><span data-stu-id="e4eb9-117">New Features</span></span>

<span data-ttu-id="e4eb9-118">\_ \_ Nelle sezioni seguenti sono elencate le nuove funzionalità di vertex shader versione vs 3 0.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-118">New features of vertex shader version vs\_3\_0 are listed in the following sections.</span></span>

### <a name="indexing-registers"></a><span data-ttu-id="e4eb9-119">Indicizzazione di registri</span><span class="sxs-lookup"><span data-stu-id="e4eb9-119">Indexing Registers</span></span>

<span data-ttu-id="e4eb9-120">Nei modelli shader precedenti è possibile indicizzare solo la Banca dei registri costanti.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-120">In the earlier shader models, only the constant register bank could be indexed.</span></span> <span data-ttu-id="e4eb9-121">In questo modello è possibile indicizzare le banche dei registri seguenti, usando il registro del contatore di cicli (aL):</span><span class="sxs-lookup"><span data-stu-id="e4eb9-121">In this model, the following register banks can be indexed, using the loop counter register (aL):</span></span>

-   <span data-ttu-id="e4eb9-122">Registro di input (v \# )</span><span class="sxs-lookup"><span data-stu-id="e4eb9-122">Input register (v\#)</span></span>
-   <span data-ttu-id="e4eb9-123">Registro di output (o \# )</span><span class="sxs-lookup"><span data-stu-id="e4eb9-123">Output register (o\#)</span></span>

### <a name="vertex-textures"></a><span data-ttu-id="e4eb9-124">Trame di vertici</span><span class="sxs-lookup"><span data-stu-id="e4eb9-124">Vertex Textures</span></span>

<span data-ttu-id="e4eb9-125">Questo modello di shader supporta la ricerca di trame nel vertex shader usando texldl.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-125">This shader model supports texture lookup in the vertex shader using texldl.</span></span> <span data-ttu-id="e4eb9-126">Il motore dei vertici prevede quattro fasi del campionatore di trame (distinte dal campionatore della mappa di spostamento e dai sampler di trama nel motore pixel) che possono essere usate per campionare le trame impostate in tali fasi.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-126">The vertex engine has four texture sampler stages (distinct from the displacement map sampler and the texture samplers in the pixel engine) that can be used to sample textures set at those stages.</span></span> <span data-ttu-id="e4eb9-127">Vedere la pagina relativa [alle trame Vertex in vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span><span class="sxs-lookup"><span data-stu-id="e4eb9-127">See [Vertex Textures in vs\_3\_0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span></span>

### <a name="vertex-stream-frequency"></a><span data-ttu-id="e4eb9-128">Frequenza del flusso di vertici</span><span class="sxs-lookup"><span data-stu-id="e4eb9-128">Vertex Stream Frequency</span></span>

<span data-ttu-id="e4eb9-129">Questa funzionalità consente l'inizializzazione di un subset dei registri di input con una frequenza diversa da una volta per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-129">This feature allows a subset of the input registers to be initialized at a rate different from once per vertex.</span></span> <span data-ttu-id="e4eb9-130">Vedere [disegno di geometria non indicizzata](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span><span class="sxs-lookup"><span data-stu-id="e4eb9-130">See [Drawing Non-Indexed Geometry](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span></span>

### <a name="shader-output"></a><span data-ttu-id="e4eb9-131">Output shader</span><span class="sxs-lookup"><span data-stu-id="e4eb9-131">Shader Output</span></span>

<span data-ttu-id="e4eb9-132">Analogamente a vs \_ 2 \_ 0, l'output dello shader può variare con il controllo di flusso statico.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-132">Similar to vs\_2\_0, the output of the shader can vary with static flow control.</span></span> <span data-ttu-id="e4eb9-133">Prestare attenzione alla creazione di rami dinamici, in quanto ciò può causare la variazione degli output dello shader per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-133">Be careful with dynamic branching as this can cause shader outputs to vary per vertex.</span></span> <span data-ttu-id="e4eb9-134">Questa operazione produrrà risultati imprevedibili su hardware diverso.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-134">This will produce unpredictable results on different hardware.</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="e4eb9-135">Controllo dinamico di flusso</span><span class="sxs-lookup"><span data-stu-id="e4eb9-135">Dynamic flow control</span></span>

<span data-ttu-id="e4eb9-136">Sono supportate tutte le istruzioni di controllo dinamico del flusso.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-136">All dynamic flow control instructions are supported.</span></span> <span data-ttu-id="e4eb9-137">Il valore massimo di profondità di annidamento consentito è 24.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-137">The maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="e4eb9-138">Per informazioni dettagliate, vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md) .</span><span class="sxs-lookup"><span data-stu-id="e4eb9-138">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="temporary-registers"></a><span data-ttu-id="e4eb9-139">Registri temporanei</span><span class="sxs-lookup"><span data-stu-id="e4eb9-139">Temporary Registers</span></span>

<span data-ttu-id="e4eb9-140">È supportato un totale di 32 registri temporanei (r \# ).</span><span class="sxs-lookup"><span data-stu-id="e4eb9-140">A total of 32 temporary registers (r\#) is supported.</span></span>

### <a name="static-flow-control"></a><span data-ttu-id="e4eb9-141">Controllo di flusso statico</span><span class="sxs-lookup"><span data-stu-id="e4eb9-141">Static Flow Control</span></span>

<span data-ttu-id="e4eb9-142">La profondità massima di nidificazione per [loop-vs](loop---vs.md) / [Rep-vs](rep---vs.md) è 4.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-142">The maximum nesting depth for [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) is 4.</span></span> <span data-ttu-id="e4eb9-143">La profondità massima di nidificazione per [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz prede-vs](callnz-pred---vs.md) è 4.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-143">The maximum nesting depth for [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[callnz pred - vs](callnz-pred---vs.md) is 4.</span></span> <span data-ttu-id="e4eb9-144">Per [se bool-vs](if-bool---vs.md), il valore di profondità di nidificazione massimo consentito è 24.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-144">For [if bool - vs](if-bool---vs.md), the maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="e4eb9-145">Per informazioni dettagliate, vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md) .</span><span class="sxs-lookup"><span data-stu-id="e4eb9-145">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="predication"></a><span data-ttu-id="e4eb9-146">Predicazione</span><span class="sxs-lookup"><span data-stu-id="e4eb9-146">Predication</span></span>

<span data-ttu-id="e4eb9-147">L'istruzione predicazione è supportata.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-147">Instruction predication is supported.</span></span> <span data-ttu-id="e4eb9-148">Usare [setp \_ comp-vs](setp-comp---vs.md) per impostare il registro del predicato.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-148">Use [setp\_comp - vs](setp-comp---vs.md) to set the predicate register.</span></span>

### <a name="instruction-count"></a><span data-ttu-id="e4eb9-149">Conteggio istruzioni</span><span class="sxs-lookup"><span data-stu-id="e4eb9-149">Instruction Count</span></span>

<span data-ttu-id="e4eb9-150">Ogni vertex shader è consentito da un punto qualsiasi di 512 fino al numero di slot in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="e4eb9-150">Each vertex shader is allowed anywhere from 512 up to the number of slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> <span data-ttu-id="e4eb9-151">Il numero di istruzioni eseguite può essere molto più elevato a causa del supporto ciclo/Rep; Questa operazione è tuttavia limitata da MaxVShaderInstructionsExecuted in D3DCAPS9 che deve essere almeno 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-151">The number of instructions run can be much higher because of the loop/rep support; however, this is capped by MaxVShaderInstructionsExecuted in D3DCAPS9 which should be at least 0xFFFF.</span></span>

### <a name="device-caps"></a><span data-ttu-id="e4eb9-152">Tappi dispositivo</span><span class="sxs-lookup"><span data-stu-id="e4eb9-152">Device Caps</span></span>

<span data-ttu-id="e4eb9-153">Se vertex shader 3 \_ 0 è supportato, i seguenti limiti sono supportati nell'hardware (come minimo):</span><span class="sxs-lookup"><span data-stu-id="e4eb9-153">If Vertex Shader 3\_0 is supported, the following caps are supported in hardware (at a minimum):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e4eb9-154">Limite</span><span class="sxs-lookup"><span data-stu-id="e4eb9-154">Cap</span></span></th>
<th><span data-ttu-id="e4eb9-155">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="e4eb9-155">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4eb9-156">Tappi shader</span><span class="sxs-lookup"><span data-stu-id="e4eb9-156">Shader caps</span></span></td>
<td><ul>
<li><span data-ttu-id="e4eb9-157">DynamicFlowControlDepth è 24</span><span class="sxs-lookup"><span data-stu-id="e4eb9-157">DynamicFlowControlDepth is 24</span></span></li>
<li><span data-ttu-id="e4eb9-158">NumTemps è 32</span><span class="sxs-lookup"><span data-stu-id="e4eb9-158">NumTemps is 32</span></span></li>
<li><span data-ttu-id="e4eb9-159">StaticFlowControlDepth è 4</span><span class="sxs-lookup"><span data-stu-id="e4eb9-159">StaticFlowControlDepth is 4</span></span></li>
<li><span data-ttu-id="e4eb9-160">Predicazione è supportato.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-160">Predication is supported.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4eb9-161">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span><span class="sxs-lookup"><span data-stu-id="e4eb9-161">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span></span></td>
<td><span data-ttu-id="e4eb9-162">8 K</span><span class="sxs-lookup"><span data-stu-id="e4eb9-162">8K</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4eb9-163">VertexShaderVersion</span><span class="sxs-lookup"><span data-stu-id="e4eb9-163">VertexShaderVersion</span></span></td>
<td><span data-ttu-id="e4eb9-164">3_0</span><span class="sxs-lookup"><span data-stu-id="e4eb9-164">3_0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4eb9-165">MaxVertexShaderConst</span><span class="sxs-lookup"><span data-stu-id="e4eb9-165">MaxVertexShaderConst</span></span></td>
<td><span data-ttu-id="e4eb9-166">256</span><span class="sxs-lookup"><span data-stu-id="e4eb9-166">256</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4eb9-167">MaxVertexShader30InstructionSlots</span><span class="sxs-lookup"><span data-stu-id="e4eb9-167">MaxVertexShader30InstructionSlots</span></span></td>
<td><span data-ttu-id="e4eb9-168">512</span><span class="sxs-lookup"><span data-stu-id="e4eb9-168">512</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4eb9-169">Supporto di fog</span><span class="sxs-lookup"><span data-stu-id="e4eb9-169">Fog support</span></span></td>
<td><span data-ttu-id="e4eb9-170">D3DPRASTERCAPS_FOGVERTEX</span><span class="sxs-lookup"><span data-stu-id="e4eb9-170">D3DPRASTERCAPS_FOGVERTEX</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4eb9-171">VertexTextureFilterCaps</span><span class="sxs-lookup"><span data-stu-id="e4eb9-171">VertexTextureFilterCaps</span></span></td>
<td><ul>
<li><span data-ttu-id="e4eb9-172"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="e4eb9-172"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span></span></li>
<li><span data-ttu-id="e4eb9-173"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="e4eb9-173"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e4eb9-174"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span><span class="sxs-lookup"><span data-stu-id="e4eb9-174"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span></span></td>
<td><span data-ttu-id="e4eb9-175">Gli elementi Vertex in una dichiarazione di vertice possono condividere lo stesso offset del flusso.</span><span class="sxs-lookup"><span data-stu-id="e4eb9-175">Vertex elements in a vertex declaration can share the same stream offset.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e4eb9-176">Formati vertici</span><span class="sxs-lookup"><span data-stu-id="e4eb9-176">Vertex formats</span></span></td>
<td><ul>
<li><span data-ttu-id="e4eb9-177">D3DDECLTYPE_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="e4eb9-177">D3DDECLTYPE_UBYTE4</span></span></li>
<li><span data-ttu-id="e4eb9-178">D3DDECLTYPE_UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="e4eb9-178">D3DDECLTYPE_UBYTE4N</span></span></li>
<li><span data-ttu-id="e4eb9-179">D3DDECLTYPE_SHORT2N</span><span class="sxs-lookup"><span data-stu-id="e4eb9-179">D3DDECLTYPE_SHORT2N</span></span></li>
<li><span data-ttu-id="e4eb9-180">D3DDECLTYPE_SHORT4N</span><span class="sxs-lookup"><span data-stu-id="e4eb9-180">D3DDECLTYPE_SHORT4N</span></span></li>
<li><span data-ttu-id="e4eb9-181">D3DDECLTYPE_FLOAT16_2</span><span class="sxs-lookup"><span data-stu-id="e4eb9-181">D3DDECLTYPE_FLOAT16_2</span></span></li>
<li><span data-ttu-id="e4eb9-182">D3DDECLTYPE_FLOAT16_4</span><span class="sxs-lookup"><span data-stu-id="e4eb9-182">D3DDECLTYPE_FLOAT16_4</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e4eb9-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4eb9-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4eb9-184">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="e4eb9-184">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 