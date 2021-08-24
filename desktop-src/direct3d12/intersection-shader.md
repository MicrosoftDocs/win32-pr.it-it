---
description: Shader usato per implementare primitive di intersezione personalizzate per i raggi che intersecano un volume di delimitazione associato (rettangolo di selezione).
ms.assetid: ''
title: Shader di intersezione
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
ms.openlocfilehash: d7f9f81fdedae0fc6f6aa0448e6771c331af9c0d8924ab0f091d281565e4cfa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850881"
---
# <a name="intersection-shader"></a>Shader di intersezione

Shader usato per implementare primitive di intersezione personalizzate per i raggi che intersecano un volume di delimitazione associato (rettangolo di selezione). 

Lo shader di intersezione non ha accesso al payload del raggio, ma definisce gli attributi di intersezione per ogni hit tramite una chiamata a [**ReportHit**](reporthit-function.md).  La gestione di **ReportHit** può arrestare l'intersezione shader in anticipo, se il flag **ray RAY FLAG ACCEPT FIRST \_ \_ \_ \_ HIT_\AND \_ \END \_ SEARCH** è impostato o [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) viene chiamato da un qualsiasi hit shader.  In caso contrario, restituisce true se l'hit è stato accettato o false se l'hit è stato rifiutato.  Ciò significa che un hit shader, se presente, deve essere eseguito prima che il controllo restituisca in modo condizionale lo shader di intersezione.

## <a name="shader-type-attribute"></a>Attributo Tipo shader


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

 

 




