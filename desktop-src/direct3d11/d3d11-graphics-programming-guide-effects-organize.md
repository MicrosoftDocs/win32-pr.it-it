---
title: Organizzazione dello stato in un effetto (Direct3D 11)
description: Con Direct3D 11, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture.
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a0523dd8abdabde29a5485b8d3b1e6d13b9429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993472"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a>Organizzazione dello stato in un effetto (Direct3D 11)

Con Direct3D 11, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture. Di seguito sono riportate le strutture:



| Stato della pipeline | Struttura                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| Rasterizzazione  | [**D3D11 \_ rasterizzatore \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| Unione output  | [**D3d11 \_ BLEND \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) e [ **d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) |
| Shader        | Vedere di seguito                                                                                                          |



 

Per le fasi dello shader, in cui il numero di modifiche di stato deve essere più controllato da un'applicazione, lo stato è stato diviso nello stato del buffer costante, nello stato del campionatore, nello stato delle risorse dello shader e nello stato di visualizzazione dell'accesso non ordinato (per pixel e compute shader). Questo consente a un'applicazione progettata in modo accurato di aggiornare solo lo stato che sta cambiando, migliorando le prestazioni riducendo la quantità di dati che devono essere passati alla GPU.

In che modo è possibile organizzare lo stato della pipeline in un effetto?

La risposta è, l'ordine non è rilevante. Le variabili globali non devono essere posizionate nella parte superiore. Tuttavia, tutti gli esempi nell'SDK seguono lo stesso ordine, in quanto è consigliabile organizzare i dati allo stesso modo. Si tratta quindi di una breve descrizione dell'ordinamento dei dati negli esempi di DirectX SDK.

-   [Variabili globali](#global-variables)
-   [Shader](#shaders)
-   [Gruppi, tecniche e sessioni](#groups-techniques-and-passes)

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



La sintassi per le variabili di effetto è più dettagliata nella [sintassi delle variabili di effetto (Direct3D 11)](d3d11-effect-variable-syntax.md). La sintassi per samples texture Samplers è più dettagliata in [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

## <a name="shaders"></a>Shader

Gli shader sono programmi eseguibili di piccole dimensioni. È possibile considerare gli shader come incapsulamento dello stato dello shader, perché il codice HLSL implementa la funzionalità shader. La pipeline grafica è costituita da un massimo di cinque tipi diversi di shader.

-   Vertex shaders: opera sui dati dei vertici. Un vertice in restituisce un vertice in uscita.
-   Hull shaders-opera sui dati della patch. Fase del punto di controllo: una chiamata restituisce un punto di controllo; Per ogni fase di fork e join: una patch restituisce una certa quantità di dati costanti di patch.
-   Domain shaders: opera sui dati primitivi. Una primitiva può restituire 0, 1 o molte primitive.
-   Geometry shaders: operare sui dati primitivi. Una primitiva in può restituire 0, 1 o molte primitive.
-   Pixel shader: operare sui dati in pixel. Un pixel in restituisce 1 pixel, a meno che il pixel non venga eliminato da un rendering.

La pipeline compute shader usa uno shader:

-   Compute Shaders: operare su qualsiasi tipo di dati. L'output è indipendente dal numero di thread.

Gli shader sono funzioni locali e seguono le regole della funzione di tipo C. Quando viene compilato un effetto, ogni shader viene compilato e un puntatore a ogni funzione shader viene archiviato internamente. Quando la compilazione ha esito positivo, viene restituita un'interfaccia ID3D11Effect. A questo punto l'effetto compilato è in un formato intermedio.

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



La sintassi per gli shader effetti è più dettagliata in [effetti sulla sintassi delle funzioni (Direct3D 11)](d3d11-effect-function-syntax.md).

## <a name="groups-techniques-and-passes"></a>Gruppi, tecniche e sessioni

Un gruppo è una raccolta di tecniche. Una tecnica è una raccolta di passaggi di rendering (deve essere presente almeno un passaggio). Ogni effetto superato (simile all'ambito di un singolo passaggio in un ciclo di rendering) definisce lo stato dello shader e qualsiasi altro stato della pipeline necessario per eseguire il rendering della geometria.

I gruppi sono facoltativi. È presente un singolo gruppo senza nome che comprende tutte le tecniche globali. Tutti gli altri gruppi devono essere denominati.

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

fxgroup g0
{
    technique11 RunComputeShader
    {
        pass P0
        {
            SetComputeShader( CompileShader( cs_5_0, CS() ) );
        }
    }
}

```



La sintassi per gli shader effetti è più dettagliatamente in [effetti sintassi tecnica (Direct3D 11)](d3d11-effect-technique-syntax.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 