---
description: Shader utilizzato per implementare primitive di intersezione personalizzate per i raggi che intersecano un volume di delimitazione associato (rettangolo di delimitazione).
ms.assetid: ''
title: Intersezione shader
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
ms.openlocfilehash: f20d9ceb90b716ca5e5c04fb796a8b20f535825d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305248"
---
# <a name="intersection-shader"></a><span data-ttu-id="05871-103">Intersezione shader</span><span class="sxs-lookup"><span data-stu-id="05871-103">Intersection Shader</span></span>

<span data-ttu-id="05871-104">Shader utilizzato per implementare primitive di intersezione personalizzate per i raggi che intersecano un volume di delimitazione associato (rettangolo di delimitazione).</span><span class="sxs-lookup"><span data-stu-id="05871-104">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span> 

<span data-ttu-id="05871-105">L'intersezione shader non ha accesso al payload del raggio, ma definisce gli attributi di intersezione per ogni hit through di una chiamata a [**ReportHit**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="05871-105">The intersection shader does not have access to the ray payload, but defines the intersection attributes for each hit through a call to [**ReportHit**](reporthit-function.md).</span></span>  <span data-ttu-id="05871-106">La gestione di **ReportHit** può arrestare l'intersezione degli shader in anticipo, se il **flag Ray flag \_ Ray \_ accetta \_ prima \_ HIT_ \AND \_ \END \_ Search** è impostato oppure [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) viene chiamato da un qualsiasi hit shader.</span><span class="sxs-lookup"><span data-stu-id="05871-106">The handling of **ReportHit** may stop the intersection shader early, if the ray flag **RAY\_FLAG\_ACCEPT\_FIRST\_HIT_\AND\_\END\_SEARCH** is set, or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) is called from an any hit shader.</span></span>  <span data-ttu-id="05871-107">In caso contrario, restituisce true se il hit è stato accettato o false se l'hit è stato rifiutato.</span><span class="sxs-lookup"><span data-stu-id="05871-107">Otherwise, it returns true if the hit was accepted or false if the hit was rejected.</span></span>  <span data-ttu-id="05871-108">Ciò significa che qualsiasi hit shader, se presente, deve essere eseguito prima che il controllo torni in modo condizionale all'intersezione shader.</span><span class="sxs-lookup"><span data-stu-id="05871-108">This means that an any hit shader, if present, must execute before control conditionally returns to the intersection shader.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="05871-109">Attributo di tipo shader</span><span class="sxs-lookup"><span data-stu-id="05871-109">Shader Type attribute</span></span>


```
[shader("intersection")]
```



## <a name="example"></a><span data-ttu-id="05871-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="05871-110">Example</span></span>

```
struct CustomPrimitiveDef { ... };
struct MyAttributes { ... };
struct CustomIntersectionIterator {...};
void InitCustomIntersectionIterator(CustomIntersectionIterator it) {...}
bool IntersectCustomPrimitiveFrontToBack(
    CustomPrimitiveDef prim,
    inout CustomIntersectionIterator it,
    float3 origin, float3 dir,
    float rayTMin, inout float curT,
    out MyAttributes attr);

[shader("intersection")]
void intersection_main()
{
    float THit = RayTCurrent();
    MyAttributes attr;
    CustomIntersectionIterator it;
    InitCustomIntersectionIterator(it); 
    while(IntersectCustomPrimitiveFrontToBack(
            CustomPrimitiveDefinitions[LocalConstants.PrimitiveIndex],
            it, ObjectRayOrigin(), ObjectRayDirection(), 
            RayTMin(), THit, attr))
    {
        // Exit on the first hit.  Note that if the ray has
        // RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH or an
        // anyhit shader is used and calls AcceptHitAndEndSearch(),
        // that would also fully exit this intersection shader (making
        // the “break” below moot in that case).        
        if (ReportHit(THit, /*hitKind*/ 0, attr) && (RayFlags() &  RAY_FLAG_FORCE_OPAQUE))
            break;
    }
}
```

 

 




