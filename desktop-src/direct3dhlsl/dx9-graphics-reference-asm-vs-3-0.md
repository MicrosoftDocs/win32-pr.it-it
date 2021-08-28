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
ms.openlocfilehash: fd10f6d726118679f395f01714233c7096fd5189
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476417"
---
# <a name="vs_3_0"></a>vs \_ 3 \_ 0

Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici. Registra i dati di trasferimento in e all'uscita dall'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.

Vertex shader versione \_ 3 \_ 0 estende il set di funzionalità supportato da vs \_ 2 \_ x. Ognuna delle funzionalità in vs 2 X che richiede l'impostazione di un limite, è disponibile in vs \_ \_ \_ 3 \_ 0 senza richiedere il limite.

-   [Istruzioni : rispetto \_ a 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contiene un elenco delle istruzioni disponibili.
-   [Registri: rispetto a \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) sono elencati i diversi tipi di registri usati dal vertex shader ALU.
-   [I modificatori di registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare il funzionamento di un'istruzione.
-   [I modificatori del registro di origine vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.
-   [Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quali componenti del registro di destinazione vengono scritti.

## <a name="new-features"></a>Nuove funzioni e caratteristiche

Le nuove funzionalità di vertex shader versione \_ 3 \_ 0 sono elencate nelle sezioni seguenti.

### <a name="indexing-registers"></a>Registri di indicizzazione

Nei modelli shader precedenti è possibile indicizzare solo la banca dei registri costanti. In questo modello è possibile indicizzare le banche di registro seguenti usando il registro dei contatori del ciclo (aL):

-   Registro di input (v \# )
-   Registro di output (o \# )

### <a name="vertex-textures"></a>Trame dei vertici

Questo modello shader supporta la ricerca di trame nel vertex shader usando texldl. Il motore dei vertici ha quattro fasi del campionatore di trama (distinte dal campionatore mappa di spostamento e dai campionatori di trama nel motore pixel) che possono essere usate per campionare le trame impostate in tali fasi. Vedere [Trame vertice in vs \_ 3 \_ 0 (DirectX HLSL).](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)

### <a name="vertex-stream-frequency"></a>Frequenza del flusso dei vertici

Questa funzionalità consente l'inizializzazione di un subset dei registri di input a una velocità diversa da una volta per vertice. Vedere [Disegno di geometrie non indicizzate.](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry)

### <a name="shader-output"></a>Shader Output

Analogamente a vs \_ 2 \_ 0, l'output dello shader può variare con il controllo di flusso statico. Prestare attenzione alla diramazione dinamica, in quanto ciò può causare variazioni degli output dello shader per vertice. Ciò produrrà risultati imprevedibili su hardware diverso.

### <a name="dynamic-flow-control"></a>Controllo dinamico del flusso

Tutte le istruzioni di controllo dinamico del flusso sono supportate. Il valore massimo di profondità di annidamento consentito è 24. Per informazioni [dettagliate, Flow limiti di annidamento del](dx9-graphics-reference-asm-vs-instructions-flow-control.md) controllo.

### <a name="temporary-registers"></a>Registri temporanei

È supportato un totale di 32 registri temporanei (r \# ).

### <a name="static-flow-control"></a>Controllo Flow statico

La profondità massima di annidamento [per il ciclo - vs](loop---vs.md)rep - rispetto / [a](rep---vs.md) 4. La profondità di annidamento massima [per call - vs](call---vs.md) / [callnz bool - vs](callnz-bool---vs.md) / [callnz pred - rispetto a](callnz-pred---vs.md) 4. Per [se bool - vs](if-bool---vs.md), il valore massimo di profondità di annidamento consentito è 24. Per informazioni [dettagliate, Flow limiti di annidamento del](dx9-graphics-reference-asm-vs-instructions-flow-control.md) controllo.

### <a name="predication"></a>Predicazione

La predicazione dell'istruzione è supportata. Usare [setp \_ comp - vs per](setp-comp---vs.md) impostare il registro predicati.

### <a name="instruction-count"></a>Conteggio istruzioni

Ogni vertex shader è consentito da 512 fino al numero di slot in MaxVertexShader30InstructionSlots in [**D3DCAPS9.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) Il numero di istruzioni eseguite può essere molto più elevato a causa del supporto di ciclo/ripetizione. tuttavia, questo limite è limitato da MaxVShaderInstructionsExecuted in D3DCAPS9, che deve essere almeno 0xFFFF.

### <a name="device-caps"></a>Tappi dispositivo

Se Vertex Shader 3 0 è supportato, nell'hardware sono supportati almeno i limiti \_ seguenti:




| Cap | Funzionalità | 
|-----|------------|
| Estremità dello shader | <ul><li>DynamicFlowControlDepth è 24</li><li>NumTemps è 32</li><li>StaticFlowControlDepth è 4</li><li>La predicazione è supportata.</li></ul> | 
| GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom | 8 K | 
| VertexShaderVersion | 3_0 | 
| MaxVertexShaderConst | 256 | 
| MaxVertexShader30InstructionSlots | 512 | 
| Supporto di Osanna | D3DPRASTERCAPS_FOGVERTEX | 
| VertexTextureFilterCaps | <ul><li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></li><li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></li></ul> | 
| <a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a> | Gli elementi vertice in una dichiarazione di vertice possono condividere lo stesso offset del flusso. | 
| Formati dei vertici | <ul><li>D3DDECLTYPE_UBYTE4</li><li>D3DDECLTYPE_UBYTE4N</li><li>D3DDECLTYPE_SHORT2N</li><li>D3DDECLTYPE_SHORT4N</li><li>D3DDECLTYPE_FLOAT16_2</li><li>D3DDECLTYPE_FLOAT16_4</li></ul> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex Shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 
