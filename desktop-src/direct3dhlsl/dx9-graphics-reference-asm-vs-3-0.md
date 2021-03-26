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
# <a name="vs_3_0"></a>vs \_ 3 \_ 0

Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.

Vertex shader versione vs \_ 3 \_ 0 estende il set di funzionalità supportato da vs \_ 2 \_ x. Ogni funzionalità di vs \_ 2 \_ X che richiede l'impostazione di un limite è disponibile in vs \_ 3 \_ 0 senza richiedere il limite.

-   [Istruzioni-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contiene un elenco delle istruzioni disponibili.
-   [Registers-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) elenca i diversi tipi di registri usati da vertex shader Alu.
-   I [modificatori del registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare la modalità di funzionamento di un'istruzione.
-   I [modificatori del registro di origine vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   Il [Registro di origine swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornisce un controllo aggiuntivo sui componenti di registro letti, copiati o scritti.
-   Il [mascheramento del registro di destinazione](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quali componenti del registro di destinazione vengono scritti.

## <a name="new-features"></a>Nuove funzioni e caratteristiche

\_ \_ Nelle sezioni seguenti sono elencate le nuove funzionalità di vertex shader versione vs 3 0.

### <a name="indexing-registers"></a>Indicizzazione di registri

Nei modelli shader precedenti è possibile indicizzare solo la Banca dei registri costanti. In questo modello è possibile indicizzare le banche dei registri seguenti, usando il registro del contatore di cicli (aL):

-   Registro di input (v \# )
-   Registro di output (o \# )

### <a name="vertex-textures"></a>Trame di vertici

Questo modello di shader supporta la ricerca di trame nel vertex shader usando texldl. Il motore dei vertici prevede quattro fasi del campionatore di trame (distinte dal campionatore della mappa di spostamento e dai sampler di trama nel motore pixel) che possono essere usate per campionare le trame impostate in tali fasi. Vedere la pagina relativa [alle trame Vertex in vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).

### <a name="vertex-stream-frequency"></a>Frequenza del flusso di vertici

Questa funzionalità consente l'inizializzazione di un subset dei registri di input con una frequenza diversa da una volta per ogni vertice. Vedere [disegno di geometria non indicizzata](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).

### <a name="shader-output"></a>Output shader

Analogamente a vs \_ 2 \_ 0, l'output dello shader può variare con il controllo di flusso statico. Prestare attenzione alla creazione di rami dinamici, in quanto ciò può causare la variazione degli output dello shader per ogni vertice. Questa operazione produrrà risultati imprevedibili su hardware diverso.

### <a name="dynamic-flow-control"></a>Controllo dinamico di flusso

Sono supportate tutte le istruzioni di controllo dinamico del flusso. Il valore massimo di profondità di annidamento consentito è 24. Per informazioni dettagliate, vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md) .

### <a name="temporary-registers"></a>Registri temporanei

È supportato un totale di 32 registri temporanei (r \# ).

### <a name="static-flow-control"></a>Controllo di flusso statico

La profondità massima di nidificazione per [loop-vs](loop---vs.md) / [Rep-vs](rep---vs.md) è 4. La profondità massima di nidificazione per [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz prede-vs](callnz-pred---vs.md) è 4. Per [se bool-vs](if-bool---vs.md), il valore di profondità di nidificazione massimo consentito è 24. Per informazioni dettagliate, vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md) .

### <a name="predication"></a>Predicazione

L'istruzione predicazione è supportata. Usare [setp \_ comp-vs](setp-comp---vs.md) per impostare il registro del predicato.

### <a name="instruction-count"></a>Conteggio istruzioni

Ogni vertex shader è consentito da un punto qualsiasi di 512 fino al numero di slot in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). Il numero di istruzioni eseguite può essere molto più elevato a causa del supporto ciclo/Rep; Questa operazione è tuttavia limitata da MaxVShaderInstructionsExecuted in D3DCAPS9 che deve essere almeno 0xFFFF.

### <a name="device-caps"></a>Tappi dispositivo

Se vertex shader 3 \_ 0 è supportato, i seguenti limiti sono supportati nell'hardware (come minimo):



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Limite</th>
<th>Funzionalità</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tappi shader</td>
<td><ul>
<li>DynamicFlowControlDepth è 24</li>
<li>NumTemps è 32</li>
<li>StaticFlowControlDepth è 4</li>
<li>Predicazione è supportato.</li>
</ul></td>
</tr>
<tr class="even">
<td>GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</td>
<td>8 K</td>
</tr>
<tr class="odd">
<td>VertexShaderVersion</td>
<td>3_0</td>
</tr>
<tr class="even">
<td>MaxVertexShaderConst</td>
<td>256</td>
</tr>
<tr class="odd">
<td>MaxVertexShader30InstructionSlots</td>
<td>512</td>
</tr>
<tr class="even">
<td>Supporto di fog</td>
<td>D3DPRASTERCAPS_FOGVERTEX</td>
</tr>
<tr class="odd">
<td>VertexTextureFilterCaps</td>
<td><ul>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></li>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></td>
<td>Gli elementi Vertex in una dichiarazione di vertice possono condividere lo stesso offset del flusso.</td>
</tr>
<tr class="odd">
<td>Formati vertici</td>
<td><ul>
<li>D3DDECLTYPE_UBYTE4</li>
<li>D3DDECLTYPE_UBYTE4N</li>
<li>D3DDECLTYPE_SHORT2N</li>
<li>D3DDECLTYPE_SHORT4N</li>
<li>D3DDECLTYPE_FLOAT16_2</li>
<li>D3DDECLTYPE_FLOAT16_4</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 