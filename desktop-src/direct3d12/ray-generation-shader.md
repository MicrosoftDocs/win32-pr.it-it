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
# <a name="ray-generation-shader"></a><span data-ttu-id="0e2d0-103">Shader di generazione del Ray</span><span class="sxs-lookup"><span data-stu-id="0e2d0-103">Ray Generation Shader</span></span>

<span data-ttu-id="0e2d0-104">Shader che chiama [**TraceRay**](traceray-function.md) per generare raggi.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-104">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span> <span data-ttu-id="0e2d0-105">Il payload del raggio iniziale definito dall'utente per ogni raggio viene fornito al sito di chiamata **TraceRay** .</span><span class="sxs-lookup"><span data-stu-id="0e2d0-105">The initial user-defined ray payload for each ray is provided to the **TraceRay** call site.</span></span>  <span data-ttu-id="0e2d0-106">[**CallShader**](callshader-function.md) può essere usato anche negli shader di generazione di Ray per richiamare [shader richiamabili](callable-shader.md).</span><span class="sxs-lookup"><span data-stu-id="0e2d0-106">[**CallShader**](callshader-function.md) may also be used in ray generation shaders to invoke [callable shaders](callable-shader.md).</span></span>

<span data-ttu-id="0e2d0-107">**DispatchRays** richiama una griglia di chiamate dello shader di generazione dei Ray.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-107">**DispatchRays** invokes a grid of ray generation shader invocations.</span></span>  <span data-ttu-id="0e2d0-108">Ogni chiamata (thread) di uno shader di generazione dei Ray ne conosce la posizione nella griglia complessiva, può generare raggi arbitrari tramite [**TraceRay**](traceray-function.md)e opera indipendentemente da altre chiamate.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-108">Each invocation (thread) of a ray generation shader knows its location in the overall grid, can generate arbitrary rays via [**TraceRay**](traceray-function.md), and operates independently of other invocations.</span></span> <span data-ttu-id="0e2d0-109">Non esiste un ordine di esecuzione definito dei thread per quanto concerne l'uno rispetto all'altro.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-109">There is no defined order of execution of threads with respect to each other.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="0e2d0-110">Attributo di tipo shader</span><span class="sxs-lookup"><span data-stu-id="0e2d0-110">Shader Type attribute</span></span>


```
[shader("raygeneration")]
```



## <a name="example"></a><span data-ttu-id="0e2d0-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="0e2d0-111">Example</span></span>

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

 

 




