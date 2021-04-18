---
description: Shader che chiama TraceRay per generare raggi.
ms.assetid: ''
title: Shader di generazione del Ray
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
ms.openlocfilehash: 75d67293e489eee0f1d100002965c017de7c682c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305247"
---
# <a name="ray-generation-shader"></a>Shader di generazione del Ray

Shader che chiama [**TraceRay**](traceray-function.md) per generare raggi. Il payload del raggio iniziale definito dall'utente per ogni raggio viene fornito al sito di chiamata **TraceRay** .  [**CallShader**](callshader-function.md) può essere usato anche negli shader di generazione di Ray per richiamare [shader richiamabili](callable-shader.md).

**DispatchRays** richiama una griglia di chiamate dello shader di generazione dei Ray.  Ogni chiamata (thread) di uno shader di generazione dei Ray ne conosce la posizione nella griglia complessiva, può generare raggi arbitrari tramite [**TraceRay**](traceray-function.md)e opera indipendentemente da altre chiamate. Non esiste un ordine di esecuzione definito dei thread per quanto concerne l'uno rispetto all'altro.

## <a name="shader-type-attribute"></a>Attributo di tipo shader


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

 

 




