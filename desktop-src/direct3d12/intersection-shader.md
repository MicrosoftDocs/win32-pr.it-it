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
# <a name="intersection-shader"></a>Intersezione shader

Shader utilizzato per implementare primitive di intersezione personalizzate per i raggi che intersecano un volume di delimitazione associato (rettangolo di delimitazione). 

L'intersezione shader non ha accesso al payload del raggio, ma definisce gli attributi di intersezione per ogni hit through di una chiamata a [**ReportHit**](reporthit-function.md).  La gestione di **ReportHit** può arrestare l'intersezione degli shader in anticipo, se il **flag Ray flag \_ Ray \_ accetta \_ prima \_ HIT_ \AND \_ \END \_ Search** è impostato oppure [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) viene chiamato da un qualsiasi hit shader.  In caso contrario, restituisce true se il hit è stato accettato o false se l'hit è stato rifiutato.  Ciò significa che qualsiasi hit shader, se presente, deve essere eseguito prima che il controllo torni in modo condizionale all'intersezione shader.

## <a name="shader-type-attribute"></a>Attributo di tipo shader


```
[shader("intersection")]
```



## <a name="example"></a>Esempio

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

 

 




