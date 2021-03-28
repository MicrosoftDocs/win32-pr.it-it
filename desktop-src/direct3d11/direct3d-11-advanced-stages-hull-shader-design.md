---
title: Come progettare un Hull shader
description: In questo argomento viene illustrato come progettare un Hull shader.
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece816ae33e7f4ecf4d024098e7741f197c423f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993376"
---
# <a name="how-to-design-a-hull-shader"></a>Procedura: progettare un Hull shader

Un Hull shader è il primo di tre fasi che interagiscono per implementare lo [schema a mosaico](direct3d-11-advanced-stages-tessellation.md) (le altre due fasi sono mosaico e Domain shader). In questo argomento viene illustrato come progettare un Hull shader.

Uno scafo shader richiede due funzioni, la principale Hull shader e una funzione costante patch. Hull shader implementa i calcoli in ogni punto di controllo; Hull shader chiama anche la funzione Constant patch che implementa i calcoli in ogni patch.

Dopo aver progettato uno Hull shader, vedere [procedura: creare uno scafo shader](direct3d-11-advanced-stages-hull-shader-create.md) per informazioni su come creare un Hull shader.

**Per progettare uno Hull shader**

1.  Definire i punti di controllo di output e controllo input Hull shader.

    ```
    // Input control point
    struct VS_CONTROL_POINT_OUTPUT
    {
        float3 vPosition : WORLDPOS;
        float2 vUV       : TEXCOORD0;
        float3 vTangent  : TANGENT;
    };

    // Output control point
    struct BEZIER_CONTROL_POINT
    {
        float3 vPosition    : BEZIERPOS;
    };
    ```

    

2.  Definire i dati costanti della patch di output.

    ```
    // Output patch constant data.
    struct HS_CONSTANT_DATA_OUTPUT
    {
        float Edges[4]        : SV_TessFactor;
        float Inside[2]       : SV_InsideTessFactor;
        
        float3 vTangent[4]    : TANGENT;
        float2 vUV[4]         : TEXCOORD;
        float3 vTanUCorner[4] : TANUCORNER;
        float3 vTanVCorner[4] : TANVCORNER;
        float4 vCWts          : TANWEIGHTS;
    };
    ```

    

    Per un dominio quad, [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) definisce 4 fattori a mosaico perimetrale (per conteggiarla suddividerla i bordi), perché la funzione fissa mosaico deve conoscere la quantità di conteggiarla suddividerla. Gli output necessari sono diversi per il triangolo e i domini di deoline.

    La funzione fissa mosaico non esamina altri output di Hull shader, ad esempio altri dati della costante patch o uno dei punti di controllo. Il Domain shader, che viene richiamato per ogni punto che la funzione fissa mosaico genera, vedrà come input tutti i punti di controllo di output di Hull shader e tutti i dati costanti della patch di output. lo shader valuta la patch nella posizione.

3.  Definire una funzione costante patch. Una funzione costante patch viene eseguita una volta per ogni patch per calcolare i dati costanti per l'intera patch, anziché i dati del punto di controllo, che vengono calcolati nello scafo dello shader.

    ```
    
    #define MAX_POINTS 32

    // Patch Constant Function
    HS_CONSTANT_DATA_OUTPUT SubDToBezierConstantsHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip,
        uint PatchID : SV_PrimitiveID )
    {   
        HS_CONSTANT_DATA_OUTPUT Output;

        // Insert code to compute Output here
        
        return Output;
    }
    ```

    

    Le proprietà della funzione costante patch includono:

    -   Un input specifica una variabile contenente un ID patch ed è identificato dal valore di sistema **SV \_ PrimitiveID** (vedere [semantica](../direct3dhlsl/dx-graphics-hlsl-semantics.md) in Shader Model 4).
    -   Un parametro di input è i punti di controllo di input, dichiarati nell'output del punto di controllo di Visual Studio in questo esempio. **\_ \_ \_** Una funzione patch può visualizzare tutti i punti di controllo di input per ogni patch, in questo esempio sono presenti 32 punti di controllo per patch.
    -   Come minimo, è necessario che la funzione calcoli i fattori a mosaico per patch per la fase mosaico identificati con [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor). Un dominio Quad richiede quattro fattori a mosaico per i bordi e due fattori aggiuntivi (identificati da [SV \_ InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) per tessellating all'interno della patch. La funzione fissa mosaico non esamina altri output di Hull shader, ad esempio i dati della costante patch o uno dei punti di controllo.
    -   Gli output vengono in genere definiti da una struttura e vengono identificati dall' **\_ \_ \_ output dei dati costanti HS** in questo esempio. la struttura dipende dal tipo di dominio e sarebbe diversa per i domini triangolo o oline.

    Un Domain shader viene richiamato per ogni punto che la funzione fissa mosaico genera e deve visualizzare i punti di controllo dell'output e i dati costanti della patch di output (entrambi dallo scafo) per valutare una patch nella relativa posizione.

4.  Definire un Hull shader. Uno scafo shader identifica le proprietà di una patch, inclusa una funzione costante patch. Un Hull shader viene richiamato una volta per ogni punto di controllo dell'output.

    ```
    [domain("quad")]
    [partitioning("integer")]
    [outputtopology("triangle_cw")]
    [outputcontrolpoints(16)]
    [patchconstantfunc("SubDToBezierConstantsHS")]
    BEZIER_CONTROL_POINT SubDToBezierHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip, 
        uint i : SV_OutputControlPointID,
        uint PatchID : SV_PrimitiveID )
    {
        VS_CONTROL_POINT_OUTPUT Output;

        // Insert code to compute Output here.
        
        return Output;
    }
    ```

    

    Uno Hull shader usa i seguenti attributi:

    -   Attributo di [dominio](/windows/desktop/direct3dhlsl/sm5-attributes-domain) .
    -   Attributo di [partizionamento](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) .
    -   Attributo [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) .
    -   Attributo [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) .
    -   Attributo [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) . Uno scafo shader calcola i punti di controllo di output. in questo esempio sono presenti 16 punti di controllo di Bezier di output.

Tutti i punti di controllo di input (identificati dall'output del punto di controllo di Visual Studio) sono visibili per ogni chiamata a Hull shader. **\_ \_ \_** In questo esempio sono presenti 32 punti di controllo di input.

Un Hull shader viene richiamato una volta per ogni punto di controllo dell'output (identificato con [SV \_ OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) per ogni patch (identificato con SV \_ PrimitiveID). Lo scopo di questo particolare shader consiste nel calcolare l' *i*/o di output, che è stato definito come un punto di controllo di Bezier (in questo esempio sono presenti 16 punti di controllo di output definiti da outputcontrolpoints).

Uno Hull shader esegue una routine una volta per patch (funzione costante patch) per calcolare i dati di una costante di patch (come minimo i fattori a mosaico). Separatamente, un Hull shader esegue una funzione costante patch (denominata SubDToBezierConstantsHS) in ogni patch per calcolare i dati di una costante patch, ad esempio i fattori a mosaico per la fase mosaico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Panoramica dello schema a mosaico](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 