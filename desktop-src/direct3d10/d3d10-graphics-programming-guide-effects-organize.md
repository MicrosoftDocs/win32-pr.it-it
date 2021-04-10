---
description: "Con Direct3D 10, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture seguenti:"
ms.assetid: 674ed278-102c-43da-a6bf-58e084df151e
title: Organizzazione dello stato in effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79cbea90c4d42d0a24ec7e35815616bf6698f72f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126321"
---
# <a name="organizing-state-in-an-effect-direct3d-10"></a>Organizzazione dello stato in effetto (Direct3D 10)

Con Direct3D 10, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture seguenti:



| Stato della pipeline  | Struttura                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| Assembler input | [**D3D10 \_ \_ elemento input \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| Rasterizzazione   | [**D3D10 \_ rasterizzatore \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| Unione output   | [**D3D10 \_ BLEND \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) e [ **D3D10 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |



 

Per le fasi dello shader, in cui il numero di modifiche di stato deve essere più controllato da un'applicazione, lo stato è stato diviso nello stato del buffer costante, nello stato del campionatore e nello stato delle risorse dello shader. Questo consente a un'applicazione progettata in modo accurato di aggiornare solo lo stato che sta cambiando, migliorando le prestazioni riducendo la quantità di dati che devono essere passati alla GPU.

In che modo è possibile organizzare lo stato della pipeline in un effetto?

La risposta è, l'ordine non è rilevante. Le variabili globali non devono essere posizionate nella parte superiore. Tuttavia, tutti gli esempi nell'SDK seguono lo stesso ordine, in quanto è consigliabile organizzare i dati allo stesso modo. Si tratta quindi di una breve descrizione dell'ordinamento dei dati negli esempi di DirectX SDK.

-   [Variabili globali](#global-variables)
-   [Shader](#shaders)
-   [Tecniche e sessioni](#techniques-and-passes)

## <a name="global-variables"></a>Variabili globali

Analogamente alle procedure standard di C, le variabili globali vengono dichiarate per prime nella parte superiore del file. Spesso si tratta di variabili che verranno inizializzate da un'applicazione e quindi utilizzate in un effetto. In alcuni casi vengono inizializzati e mai modificati, in altre volte vengono aggiornati tutti i frame. Analogamente alle regole di ambito della funzione C, le variabili di effetto dichiarate al di fuori dell'ambito delle funzioni di effetto sono visibili in tutto l'effetto; qualsiasi variabile dichiarata all'interno di una funzione Effect è visibile solo all'interno di tale funzione.

Di seguito è riportato un esempio delle variabili dichiarate in BasicHLSL10. fx.


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



La sintassi per le variabili di effetto è più dettagliata nella [sintassi delle variabili di effetto (Direct3D 10)](d3d10-effect-variable-syntax.md). La sintassi per samples texture Samplers è più dettagliata in [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="shaders"></a>Shader

Gli shader sono programmi eseguibili di piccole dimensioni. È possibile considerare gli shader come incapsulamento dello stato dello shader, perché il codice HLSL implementa la funzionalità shader. La pipeline usa tre tipi diversi di shader.

-   Vertex shaders: opera sui dati dei vertici. Un vertice in restituisce un vertice in uscita.
-   Geometry shaders: operare sui dati primitivi. Una primitiva in può restituire 0, 1 o molte primitive.
-   Pixel shader: operare sui dati in pixel. Un pixel in restituisce 1 pixel, a meno che il pixel non venga eliminato da un rendering.

Gli shader sono funzioni locali e seguono le regole della funzione di tipo C. Quando viene compilato un effetto, ogni shader viene compilato e un puntatore a ogni funzione shader viene archiviato internamente. Quando la compilazione ha esito positivo, viene restituita un'interfaccia ID3D10Effect. A questo punto l'effetto compilato è in un formato intermedio.

Per ulteriori informazioni sugli shader compilati, è necessario utilizzare la reflection dello shader. Questo è essenzialmente come chiedere al runtime di decompilare gli shader e restituire informazioni sul codice dello shader.


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



La sintassi per gli shader effetti è più dettagliata in [effetti sulla sintassi delle funzioni (Direct3D 10)](d3d10-effect-function-syntax.md).

## <a name="techniques-and-passes"></a>Tecniche e sessioni

Una tecnica è una raccolta di passaggi di rendering (deve essere presente almeno un passaggio). Ogni effetto superato (simile all'ambito di un singolo passaggio in un ciclo di rendering) definisce lo stato dello shader e qualsiasi altro stato della pipeline necessario per eseguire il rendering della geometria.

Di seguito è riportato un esempio di una tecnica (che include un passaggio) da BasicHLSL10. fx.


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



La sintassi per gli shader effetti è più dettagliatamente in [effetti sintassi tecnica (Direct3D 10)](d3d10-effect-technique-syntax.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
