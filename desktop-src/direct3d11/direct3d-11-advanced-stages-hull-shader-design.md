---
title: Come progettare uno hull shader
description: Questo argomento illustra come progettare uno hull shader.
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79021d6a5c03b057defdeae0d506898831ab740d11d2e105242ff53b1b39e9bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046639"
---
# <a name="how-to-design-a-hull-shader"></a>Procedura: Progettare uno shader di tipo hull

Uno hull shader è la prima di tre fasi che si uniscono per implementare la [tessellazione](direct3d-11-advanced-stages-tessellation.md) (le altre due fasi sono il tessellatore e uno shader di dominio). Questo argomento illustra come progettare uno hull shader.

Uno shader con scafo richiede due funzioni: lo shader principale e una funzione costante patch. Lo hull shader implementa i calcoli su ogni punto di controllo. Lo hull shader chiama anche la funzione costante patch che implementa i calcoli su ogni patch.

Dopo aver progettato uno hull shader, vedere [Procedura: Creare](direct3d-11-advanced-stages-hull-shader-create.md) uno hull shader per informazioni su come creare uno hull shader.

**Per progettare uno hull shader**

1.  Definire il controllo di input e i punti di controllo di output dello shader.

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

    

    Per un dominio quad, [ \_ TessFactor SV](/windows/desktop/direct3dhlsl/sv-tessfactor) definisce 4 fattori a tessellazione bordi (per sfasare i bordi), poiché il tessellatore di funzione fissa deve sapere quanto a tessellare. Gli output necessari sono diversi per i domini triangolo e isolineo.

    Il tessellatore di funzioni fisse non controlla altri output di hull shader, ad esempio altri dati costanti della patch o uno qualsiasi dei punti di controllo. Lo shader del dominio, che viene richiamato per ogni punto generato dal tessellatore di funzioni fisse, vede come input tutti i punti di controllo di output dello hull shader e tutti i dati costanti della patch di output. Lo shader valuta la patch nella relativa posizione.

3.  Definire una funzione costante patch. Una funzione costante patch viene eseguita una volta per ogni patch per calcolare tutti i dati costanti per l'intera patch(a differenza dei dati dei singoli punti di controllo, che vengono calcolati nello shader della struttura).

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

    -   Un input specifica una variabile contenente un ID patch ed è identificato dal valore di sistema **\_ SV PrimitiveID** (vedere [la semantica](../direct3dhlsl/dx-graphics-hlsl-semantics.md) nel modello shader 4).
    -   Un parametro di input è il punto di controllo di input, dichiarato in **VS \_ CONTROL POINT \_ \_ OUTPUT** in questo esempio. Una funzione patch può visualizzare tutti i punti di controllo di input per ogni patch. In questo esempio sono presenti 32 punti di controllo per ogni patch.
    -   Come minimo, la funzione deve calcolare i fattori a tessellazione per patch per la fase del tessellatore identificati con [SV \_ TessFactor.](/windows/desktop/direct3dhlsl/sv-tessfactor) Un dominio quad richiede quattro fattori a tessellazione per gli bordi e due fattori aggiuntivi (identificati da [SV \_ InsideTessFactor)](/windows/desktop/direct3dhlsl/sv-insidetessfactor)per l'applicazione del tessellamento all'interno della patch. Il tessellatore di funzioni fisse non controlla altri output di hull shader, ad esempio i dati costanti della patch o uno qualsiasi dei punti di controllo.
    -   Gli output sono in genere definiti da una struttura ed è identificato da **HS \_ CONSTANT DATA \_ \_ OUTPUT** in questo esempio. La struttura dipende dal tipo di dominio e sarebbe diversa per i domini triangolo o isolineo.

    Viene invece richiamato uno shader di dominio per ogni punto generato dal tessellatore di funzioni fisse e deve visualizzare i punti di controllo di output e i dati costanti della patch di output (entrambi dello shader hull) per valutare una patch nella relativa posizione.

4.  Definire uno hull shader. Uno hull shader identifica le proprietà di una patch, inclusa una funzione costante patch. Uno hull shader viene richiamato una volta per ogni punto di controllo di output.

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

    

    Uno hull shader usa gli attributi seguenti:

    -   Attributo [di](/windows/desktop/direct3dhlsl/sm5-attributes-domain) dominio.
    -   Attributo [di partizionamento.](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning)
    -   Attributo [outputtopology.](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology)
    -   Attributo [outputcontrolpoints.](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints)
    -   Attributo [patchconstantfunc.](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) Uno hull shader calcola i punti di controllo di output. In questo esempio sono presenti 16 punti di controllo di Bézier di output.

Tutti i punti di controllo di input (identificati da **VS \_ CONTROL POINT \_ \_ OUTPUT)** sono visibili a ogni chiamata dello shader di tipo hull shader. In questo esempio sono presenti 32 punti di controllo di input.

Uno hull shader viene richiamato una volta per ogni punto di controllo di output (identificato con [ \_ SV OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) per ogni patch (identificata con \_ SV PrimitiveID). Lo scopo di questo particolare shader è calcolare l'output *i*, che è stato definito come un punto di controllo BEZIER (in questo esempio sono definiti 16 punti di controllo di output dai punti di controllo di output).

Uno hull shader esegue una routine una volta per ogni patch (funzione costante patch) per calcolare come minimo i dati costanti della patch (fattori a tessellazione). Separatamente, uno hull shader esegue una funzione costante di patch (denominata SubDToBezierConstantsHS) in ogni patch per calcolare i dati costanti della patch, ad esempio i fattori a suddivisione a zigoma per la fase a tessellatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Cenni preliminari sull'a tessellazione](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 