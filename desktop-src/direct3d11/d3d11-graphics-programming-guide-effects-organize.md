---
title: Organizzazione dello stato in un effetto (Direct3D 11)
description: Con Direct3D 11, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture.
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d36bf99887e96dc5854778edb24f0ceacbc0cdf5a7994532bc2ebd94137fe8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126095"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a>Organizzazione dello stato in un effetto (Direct3D 11)

Con Direct3D 11, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture. Ecco le strutture:



| Stato della pipeline | Struttura                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| Rasterizzazione  | [**D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| Unione output  | [**D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) e [ **D3D11 \_ DEPTH STENCIL \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) |
| Shader        | Vedere di seguito                                                                                                          |



 

Per le fasi dello shader, in cui il numero di modifiche dello stato deve essere più controllato da un'applicazione, lo stato è stato suddiviso in stato costante del buffer, stato del campionatore, stato della risorsa shader e stato di visualizzazione di accesso non ordinato (per shader pixel e di calcolo). Ciò consente a un'applicazione progettata con attenzione di aggiornare solo lo stato che sta cambiando, riducendo le prestazioni riducendo la quantità di dati che devono essere passati alla GPU.

Come si organizza lo stato della pipeline in un effetto?

La risposta è che l'ordine non è importante. Non è necessario che le variabili globali si trovino nella parte superiore. Tuttavia, tutti gli esempi nell'SDK seguono lo stesso ordine, perché è buona norma organizzare i dati nello stesso modo. Si tratta quindi di una breve descrizione dell'ordinamento dei dati negli esempi di DirectX SDK.

-   [Variabili globali](#global-variables)
-   [Shader](#shaders)
-   [Gruppi, tecniche e passaggi](#groups-techniques-and-passes)

## <a name="global-variables"></a>Variabili globali

Analogamente alla procedura C standard, le variabili globali vengono dichiarate per prime all'inizio del file. Nella maggior parte dei casi, si tratta di variabili che verranno inizializzate da un'applicazione e quindi usate in un effetto. A volte vengono inizializzati e non vengono mai modificati, altre volte vengono aggiornati ogni frame. Proprio come le regole di ambito delle funzioni C, le variabili di effetto dichiarate all'esterno dell'ambito delle funzioni di effetto sono visibili in tutto l'effetto; Qualsiasi variabile dichiarata all'interno di una funzione di effetto è visibile solo all'interno di tale funzione.

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



La sintassi per le variabili di effetto è più dettagliata in Sintassi delle variabili degli effetti [(Direct3D 11).](d3d11-effect-variable-syntax.md) La sintassi per i campionatori di trama degli effetti è più dettagliata in [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

## <a name="shaders"></a>Shader

Gli shader sono piccoli programmi eseguibili. È possibile pensare agli shader come a incapsulare lo stato dello shader, poiché il codice HLSL implementa la funzionalità shader. Pipeline grafica fino a cinque diversi tipi di shader.

-   Vertex shader: operare sui dati dei vertici. Un vertice in restituisce un vertice.
-   Hull shader: operare sui dati delle patch. Fase del punto di controllo: una chiamata restituisce un punto di controllo. Per ogni fase di fork e join: una patch restituisce una quantità di dati costanti della patch.
-   Shader di dominio: operare su dati primitivi. Una primitiva può produrre 0, 1 o molte primitive.
-   Shader geometry: operare su dati primitivi. Una primitiva in può produrre 0, 1 o molte primitive.
-   Pixel shader: operare sui dati pixel. Un pixel in restituisce 1 pixel (a meno che il pixel non venga estratto da un rendering).

La pipeline di compute shader usa uno shader:

-   Shader di calcolo: operare su qualsiasi tipo di dati. L'output è indipendente dal numero di thread.

Gli shader sono funzioni locali e seguono le regole delle funzioni di stile C. Quando un effetto viene compilato, ogni shader viene compilato e un puntatore a ogni funzione shader viene archiviato internamente. Quando la compilazione ha esito positivo, viene restituita un'interfaccia ID3D11Effect. A questo punto l'effetto compilato è in un formato intermedio.

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



La sintassi per gli shader degli effetti è più dettagliata in Sintassi delle funzioni effetti [(Direct3D 11).](d3d11-effect-function-syntax.md)

## <a name="groups-techniques-and-passes"></a>Gruppi, tecniche e passaggi

Un gruppo è una raccolta di tecniche. Una tecnica è una raccolta di passaggi di rendering (deve essere presente almeno un passaggio). Ogni passaggio dell'effetto (simile nell'ambito a un singolo passaggio in un ciclo di rendering) definisce lo stato dello shader e qualsiasi altro stato della pipeline necessario per il rendering della geometria.

I gruppi sono facoltativi. Esiste un singolo gruppo senza nome che include tutte le tecniche globali. Tutti gli altri gruppi devono essere denominati.

Ecco un esempio di una tecnica (che include un passaggio) da BasicHLSL10.fx.


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



La sintassi per gli shader degli effetti è più dettagliata in Sintassi della tecnica degli effetti [(Direct3D 11).](d3d11-effect-technique-syntax.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 