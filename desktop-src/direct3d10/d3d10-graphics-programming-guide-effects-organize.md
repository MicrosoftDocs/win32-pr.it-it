---
description: "Con Direct3D 10, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture seguenti:"
ms.assetid: 674ed278-102c-43da-a6bf-58e084df151e
title: Organizzazione dello stato in un effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0fdd4389ce4db34a64e4bc5e39f21998c90481d4a43a06244be2b231cca999
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753751"
---
# <a name="organizing-state-in-an-effect-direct3d-10"></a>Organizzazione dello stato in un effetto (Direct3D 10)

Con Direct3D 10, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture seguenti:



| Stato della pipeline  | Struttura                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| Assembler input | [**ELEMENTO DI INPUT D3D10 \_ \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| Rasterizzazione   | [**D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| Unione output   | [**D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) e [ **D3D10 \_ DEPTH STENCIL \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |



 

Per le fasi dello shader, in cui il numero di modifiche di stato deve essere controllato più da un'applicazione, lo stato è stato suddiviso in stato costante del buffer, stato del campionatore e stato della risorsa shader. In questo modo un'applicazione progettata con attenzione per aggiornare solo lo stato in modifica, che migliora le prestazioni riducendo la quantità di dati che devono essere passati alla GPU.

Come si organizza lo stato della pipeline in un effetto?

La risposta è che l'ordine non è importante. Non è necessario che le variabili globali si trovino nella parte superiore. Tuttavia, tutti gli esempi nell'SDK seguono lo stesso ordine, perché è consigliabile organizzare i dati nello stesso modo. Si tratta quindi di una breve descrizione dell'ordinamento dei dati negli esempi di DirectX SDK.

-   [Variabili globali](#global-variables)
-   [Shader](#shaders)
-   [Tecniche e passaggi](#techniques-and-passes)

## <a name="global-variables"></a>Variabili globali

Analogamente alla procedura C standard, le variabili globali vengono dichiarate per prime all'inizio del file. Nella maggior parte dei casi, si tratta di variabili che verranno inizializzate da un'applicazione e quindi usate in un effetto. A volte vengono inizializzati e non vengono mai modificati, altre volte vengono aggiornati ogni frame. Proprio come le regole di ambito della funzione C, le variabili di effetto dichiarate all'esterno dell'ambito delle funzioni di effetto sono visibili in tutto l'effetto; Qualsiasi variabile dichiarata all'interno di una funzione di effetto è visibile solo all'interno di tale funzione.

Ecco un esempio delle variabili dichiarate in BasicHLSL10.fx.


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix


// Texture samplers
SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};
```



La sintassi per le variabili di effetto è più dettagliata in [Effect Variable Syntax (Direct3D 10) (Sintassi delle variabili degli effetti ( Direct3D 10)](d3d10-effect-variable-syntax.md)). La sintassi per i campionatori di trama degli effetti è più dettagliata in Tipo di campionatore [(DirectX HLSL).](../direct3dhlsl/dx-graphics-hlsl-sampler.md)

## <a name="shaders"></a>Shader

Gli shader sono piccoli programmi eseguibili. È possibile pensare agli shader come a incapsulare lo stato dello shader, perché il codice HLSL implementa la funzionalità dello shader. La pipeline usa tre tipi diversi di shader.

-   Vertex shader: operano sui dati dei vertici. Un vertice in produce un vertice.
-   Shader geometrici: funzionano su dati primitivi. Una primitiva in può produrre 0, 1 o molte primitive.
-   Pixel shader: funzionano sui dati pixel. Un pixel in restituisce 1 pixel (a meno che il pixel non venga estratto da un rendering).

Gli shader sono funzioni locali e seguono le regole delle funzioni di stile C. Quando viene compilato un effetto, ogni shader viene compilato e un puntatore a ogni funzione shader viene archiviato internamente. Quando la compilazione ha esito positivo, viene restituita un'interfaccia ID3D10Effect. A questo punto l'effetto compilato è in un formato intermedio.

Per altre informazioni sugli shader compilati, è necessario usare la reflection dello shader. Questo è essenzialmente come chiedere al runtime di decompilare gli shader e restituire informazioni sul codice dello shader.


```
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
 
    ....    
    
    return Output;    
}


struct PS_OUTPUT
{
    float4 RGBColor : SV_Target;  // Pixel color
};

PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    ....

    return Output;
}
```



La sintassi per gli shader con effetto è più dettagliata in [Effect Function Syntax (Direct3D 10) (Sintassi della funzione effetto - Direct3D 10).](d3d10-effect-function-syntax.md)

## <a name="techniques-and-passes"></a>Tecniche e passaggi

Una tecnica è una raccolta di passaggi di rendering (deve essere presente almeno un passaggio). Ogni passaggio dell'effetto (simile nell'ambito a un singolo passaggio in un ciclo di rendering) definisce lo stato dello shader e qualsiasi altro stato della pipeline necessario per il rendering della geometria.

Di seguito è riportato un esempio di una tecnica (che include un passaggio) da BasicHLSL10.fx.


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



La sintassi per gli shader con effetti è più dettagliata in [Effect Technique Syntax (Direct3D 10) (Sintassi tecnica effetto - Direct3D 10).](d3d10-effect-technique-syntax.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
