---
description: Uno shader che viene richiamato quando è abilitato e l'hit più vicino è stato determinato o la ricerca di intersezione del raggio è terminata.
ms.assetid: ''
title: Hit shader più vicino
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 347ad66dce0a81b929d5dc3c82051bf84226e723
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305195"
---
# <a name="closest-hit-shader"></a>Hit shader più vicino

Uno shader che viene richiamato quando è abilitato e l'hit più vicino è stato determinato o la ricerca di intersezione del raggio è terminata. Questo shader è il punto in cui si verificheranno in genere l'ombreggiatura della superficie e la generazione di raggi aggiuntivi.  L'hit shader più vicino deve dichiarare un parametro di payload, seguito da un parametro attributes.  Ogni deve essere un tipo di struttura definito dall'utente che corrisponde ai tipi utilizzati rispettivamente per [**TraceRay**](traceray-function.md) e [**ReportHit**](reporthit-function.md) oppure la [**struttura degli attributi di intersezione**](intersection-attributes.md) quando viene utilizzata l'intersezione del triangolo a funzione fissa.

## <a name="shader-type-attribute"></a>Attributo di tipo shader


```
[shader("closesthit")]
```



## <a name="example"></a>Esempio

```
[shader("closesthit")]
void closesthit_main(inout MyPayload payload, in MyAttributes attr)
{
    CallShader( ... );  // maybe
    // update payload for surface
    // trace reflection
    float3 worldRayOrigin = WorldRayOrigin() + WorldRayDirection() * RayTCurrent();
    float3 worldNormal = mul(attr.normal, (float3x3)ObjectToWorld3x4());
    RayDesc reflectedRay = { worldRayOrigin, SceneConstants.Epsilon,
                             ReflectRay(WorldRayDirection(), worldNormal),
                             SceneConstants.TMax };
    TraceRay(MyAccelerationStructure,
             SceneConstants.RayFlags,
             SceneConstants.InstanceInclusionMask,
             SceneConstants.RayContributionToHitGroupIndex,
             SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
             SceneConstants.MissShaderIndex,
             reflectedRay,
             payload);
    // Combine final contributions into ray payload
    // this ray query is now complete.
    // Alternately, could look at data in payload result based on that make other TraceRay
    // calls.  No constraints on the code structure.
}

```

 

 




