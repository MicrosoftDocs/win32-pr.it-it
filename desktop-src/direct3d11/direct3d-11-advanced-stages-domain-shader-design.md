---
title: Come progettare un Domain shader
description: In questo argomento viene illustrato come progettare un Domain shader.
ms.assetid: 329d4eb9-8886-401d-8fb4-39e06886998f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a01d6b006c5ffe3afa355abe5e662cb96aa1391
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118047"
---
# <a name="how-to-design-a-domain-shader"></a>Procedura: progettare un Domain shader

Un Domain shader è il terzo di tre fasi che interagiscono per implementare lo [schema a mosaico](direct3d-11-advanced-stages-tessellation.md). Il Domain shader genera la geometria della superficie dai punti di controllo trasformati da uno scafo dello shader e dalle coordinate UV. In questo argomento viene illustrato come progettare un Domain shader.

Un Domain shader viene richiamato una volta per ogni punto generato dalla funzione fissa mosaico. Gli input sono le \[ coordinate UV W \] del punto della patch, nonché tutti i dati di output dello scafo shader, inclusi i punti di controllo e le costanti di patch. L'output è un vertice definito nel modo desiderato. Se l'output viene inviato al pixel shader, l'output deve includere una posizione (indicata con una \_ semantica di posizione SV).

**Per progettare un Domain shader**

1.  Definire l'attributo di dominio.

    ```
    [domain("quad")]
    ```

    

    Il dominio è definito per una patch quad.

2.  Dichiarare il percorso sullo scafo con il valore del sistema del [percorso del dominio](/windows/desktop/direct3dhlsl/sv-domainlocation) .

    -   Per una patch quad, usare un float2.
    -   Per una patch Tri, usare float3 (per le coordinate baricentrica)
    -   Per un, usare un float2.

    Il percorso del dominio per una patch Quad è pertanto simile al seguente:

    ```
    float2 UV : SV_DomainLocation
    ```

    

3.  Definire gli altri input.

    Gli altri input provengono dallo scafo dello shader e sono definiti dall'utente. Sono inclusi i punti di controllo di input per la patch, tra i quali possono essere presenti da 1 a 32 punti e i dati costanti della patch di input.

    I punti di controllo sono definiti dall'utente, in genere con una struttura come questa (definita in [procedura: progettare uno scafo shader](direct3d-11-advanced-stages-hull-shader-design.md)):

    ```
    const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch
    ```

    

    Anche i dati delle costanti patch sono definiti dall'utente e possono avere un aspetto simile al seguente (definito in [procedura: progettare uno scafo shader](direct3d-11-advanced-stages-hull-shader-design.md)):

    ```
    HS_CONSTANT_DATA_OUTPUT input
    ```

    

4.  Aggiungere codice definito dall'utente per calcolare gli output; Ciò costituisce il corpo dello shader del dominio.

    Questa struttura contiene output di Domain shader definiti dall'utente.

    ```
    struct DS_OUTPUT
    {
        float3 vNormal    : NORMAL;
        float2 vUV        : TEXCOORD;
        float3 vTangent   : TANGENT;
        float3 vBiTangent : BITANGENT;
        
        float4 vPosition  : SV_POSITION;
    };
    ```

    

    La funzione accetta ogni UV di input (mosaico) e valuta la patch di Bezier in questa posizione.

    ```
    [domain("quad")]
    DS_OUTPUT BezierEvalDS( HS_CONSTANT_DATA_OUTPUT input, 
                            float2 UV : SV_DomainLocation,
                            const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch )
    {
        DS_OUTPUT Output;

        // Insert code to compute the output here.

        return Output;    
    }
    ```

    

    La funzione viene richiamata una volta per ogni punto generato dalla funzione fissa mosaico. Poiché in questo esempio viene usata una patch quad, il percorso del dominio di input ([SV \_ DomainLocation](/windows/desktop/direct3dhlsl/sv-domainlocation)) è un float2 (UV). una patch Tri avrà un percorso di input float3 (UVW baricentrica coordinate) e un percorso di dominio float2 input.

    Gli altri input per la funzione provengono direttamente dallo scafo dello shader. In questo esempio si tratta di 16 punti di controllo ognuno dei quali è un **\_ \_ punto di controllo Bezier**, nonché i dati delle costanti patch (**\_ \_ \_ output di dati costanti HS**). L'output è un vertice che contiene i dati desiderati, in questo esempio l' **\_ output di DS** .

Dopo aver progettato un Domain shader, vedere [procedura: creare un Domain shader](direct3d-11-advanced-stages-domain-shader-create.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Panoramica dello schema a mosaico](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 