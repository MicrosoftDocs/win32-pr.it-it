---
description: Shader che chiama TraceRay per generare raggi.
ms.assetid: ''
title: Shader di generazione di raggi
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
ms.openlocfilehash: fdc177040cac7324545172319c318d07cded6dba42cfeed4756a7afaa88439aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123713"
---
# <a name="ray-generation-shader"></a>Shader di generazione di raggi

Shader che chiama [**TraceRay per**](traceray-function.md) generare raggi. Il payload del raggio definito dall'utente iniziale per ogni raggio viene fornito al sito di chiamata **TraceRay.**  [**CallShader può**](callshader-function.md) essere usato anche negli shader di generazione di raggi per richiamare [gli shader chiamabili.](callable-shader.md)

**DispatchRays** richiama una griglia di chiamate ray generation shader.  Ogni chiamata (thread) di uno shader di generazione di raggi conosce la posizione nella griglia generale, può generare raggi arbitrari tramite [**TraceRay**](traceray-function.md)e opera indipendentemente da altre chiamate. Non esiste un ordine definito di esecuzione dei thread l'uno rispetto all'altro.

## <a name="shader-type-attribute"></a>Attributo Tipo shader


```
[shader("raygeneration")]
```



## <a name="example"></a>Esempio

```
struct SceneConstantStructure { ... };
ConstantBuffer<SceneConstantStructure> SceneConstants;
RaytracingAccelerationStructure MyAccelerationStructure : register(t3);
struct MyPayload { ... };

[shader("raygeneration")]
void raygen_main()
{
    RayDesc myRay = {
        SceneConstants.CameraOrigin,
        SceneConstants.TMin,
        computeRayDirection(SceneConstants.LensParams, DispatchRaysIndex(), 
                            DispatchRaysDimensions()),
        SceneConstants.TMax};
    MyPayload payload = { ... };    // init payload
    TraceRay(
        MyAccelerationStructure,
        SceneConstants.RayFlags,
        SceneConstants.InstanceInclusionMask,
        SceneConstants.RayContributionToHitGroupIndex,
        SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
        SceneConstants.MissShaderIndex,
        myRay,
        payload);
    WriteFinalPixel(DispatchRaysIndex(), payload);
}
```

 

 




