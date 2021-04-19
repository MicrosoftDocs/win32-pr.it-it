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
# <a name="closest-hit-shader"></a><span data-ttu-id="d7f5e-103">Hit shader più vicino</span><span class="sxs-lookup"><span data-stu-id="d7f5e-103">Closest Hit Shader</span></span>

<span data-ttu-id="d7f5e-104">Uno shader che viene richiamato quando è abilitato e l'hit più vicino è stato determinato o la ricerca di intersezione del raggio è terminata.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-104">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span> <span data-ttu-id="d7f5e-105">Questo shader è il punto in cui si verificheranno in genere l'ombreggiatura della superficie e la generazione di raggi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-105">This shader is where surface shading and additional ray generation will typically occur.</span></span>  <span data-ttu-id="d7f5e-106">L'hit shader più vicino deve dichiarare un parametro di payload, seguito da un parametro attributes.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-106">Closest hit shaders must declare a payload parameter, followed by an attributes parameter.</span></span>  <span data-ttu-id="d7f5e-107">Ogni deve essere un tipo di struttura definito dall'utente che corrisponde ai tipi utilizzati rispettivamente per [**TraceRay**](traceray-function.md) e [**ReportHit**](reporthit-function.md) oppure la [**struttura degli attributi di intersezione**](intersection-attributes.md) quando viene utilizzata l'intersezione del triangolo a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-107">Each must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed-function triangle intersection is used.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="d7f5e-108">Attributo di tipo shader</span><span class="sxs-lookup"><span data-stu-id="d7f5e-108">Shader Type attribute</span></span>


```
[shader("closesthit")]
```



## <a name="example"></a><span data-ttu-id="d7f5e-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="d7f5e-109">Example</span></span>

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

 

 




