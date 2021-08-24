---
title: Come progettare uno shader di dominio
description: Questo argomento illustra come progettare uno shader di dominio.
ms.assetid: 329d4eb9-8886-401d-8fb4-39e06886998f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46733bc9147f67cf33a127d8254f16c5813d8ebc2f0cb96c2071ae15589e34bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566181"
---
# <a name="how-to-design-a-domain-shader"></a>Procedura: Progettare uno shader di dominio

Uno shader di dominio è il terzo di tre fasi che funzionano insieme per implementare la [funzionalità a più livelli.](direct3d-11-advanced-stages-tessellation.md) Il domain shader genera la geometria della superficie dai punti di controllo trasformati da uno shader con scafo e dalle coordinate UV. Questo argomento illustra come progettare uno shader di dominio.

Uno shader di dominio viene richiamato una volta per ogni punto generato dal tessellatore di funzioni fisse. Gli input sono le coordinate UV W del punto sulla patch, nonché tutti i dati di output dello hull shader, inclusi i punti di controllo e le \[ \] costanti patch. L'output è un vertice definito nel modo desiderato. Se l'output viene inviato al pixel shader, l'output deve includere una posizione (con una semantica SV \_ Position).

**Per progettare uno shader di dominio**

1.  Definire l'attributo di dominio.

    ```
    [domain("quad")]
    ```

    

    Il dominio è definito per una patch quad.

2.  Dichiarare la posizione sulla carena con il [valore del sistema di posizione](/windows/desktop/direct3dhlsl/sv-domainlocation) del dominio.

    -   Per una patch quad, usare float2.
    -   Per una tri patch, usare float3 (per le coordinate barycentriche)
    -   Per un'isolinea, usare float2.

    Di conseguenza, il percorso del dominio per una patch quad è simile al seguente:

    ```
    float2 UV : SV_DomainLocation
    ```

    

3.  Definire gli altri input.

    Gli altri input provengono dallo shader hull e sono definiti dall'utente. Sono inclusi i punti di controllo di input per patch, di cui possono essere presenti da 1 a 32 punti, e i dati costanti della patch di input.

    I punti di controllo sono definiti dall'utente, in genere con una struttura come questa (definita in [How To: Design a Hull Shader](direct3d-11-advanced-stages-hull-shader-design.md)):

    ```
    const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch
    ```

    

    Anche i dati delle costanti di patch sono definiti dall'utente e potrebbero essere simili a questo (definito in [Procedura: Progettare uno shader con struttura):](direct3d-11-advanced-stages-hull-shader-design.md)

    ```
    HS_CONSTANT_DATA_OUTPUT input
    ```

    

4.  Aggiungere codice definito dall'utente per calcolare gli output. che costituisce il corpo dello shader del dominio.

    Questa struttura contiene output di shader di dominio definiti dall'utente.

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

    

    La funzione accetta ogni uve di input (dal tessellatore) e valuta la patch di Bézier in questa posizione.

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

    

    La funzione viene richiamata una volta per ogni punto generato dal tessellatore di funzioni fisse. Poiché questo esempio usa una patch quad, la posizione del dominio di input ([SV \_ DomainLocation](/windows/desktop/direct3dhlsl/sv-domainlocation)) è float2 (UV); una patch tri avrebbe una posizione di input float3 (coordinate UVW barycentric) e una isoline avrebbe una posizione di dominio di input float2.

    Gli altri input per la funzione provengono direttamente dallo hull shader. In questo esempio si tratta di 16 punti di controllo ognuno dei quali è un PUNTO DI CONTROLLO **BEZIER \_ \_**, nonché di dati costanti di patch (**HS \_ CONSTANT DATA \_ \_ OUTPUT**). L'output è un vertice contenente tutti i dati desiderati, **\_ output DS** in questo esempio.

Dopo aver progettato uno shader di dominio, [vedere Procedura: Creare un domain shader.](direct3d-11-advanced-stages-domain-shader-create.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Cenni preliminari sull'a tessellazione](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 