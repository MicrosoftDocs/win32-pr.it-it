---
description: Shader richiamato quando le intersezioni dei raggi non sono opache.
ms.assetid: ''
title: Qualsiasi hit shader
ms.date: 05/31/2018
ms.topic: reference
ms.localizationpriority: low
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 127c12c6d87ca76ddac5b5c5e013414c96651e56ee762156e7435811ff275a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124386"
---
# <a name="any-hit-shader"></a>Qualsiasi hit shader

Shader richiamato quando le intersezioni dei raggi non sono opache. 

Gli hit shader devono dichiarare un parametro di payload seguito da un parametro di attributi. Ognuno di questi parametri deve essere un tipo di struttura definito dall'utente che [](intersection-attributes.md) corrisponde ai tipi usati rispettivamente per [**TraceRay**](traceray-function.md) e [**ReportHit**](reporthit-function.md) oppure la struttura degli attributi di intersezione quando viene usata l'intersezione di triangoli di funzioni fisse.

Qualsiasi hit shader può eseguire i tipi di operazioni seguenti:

*   Leggere e modificare il payload di ray: (inout payload_t rayPayload)
*   Leggere gli attributi di intersezione: (negli attr_t di intersezione)
*   Chiamare [**AcceptHitAndEndSearch,**](accepthitandendsearch-function.md)che accetta l'hit corrente, termina [l'hit shader,](any-hit-shader.md)termina l'intersezione [shader](intersection-shader.md) se è presente ed esegue l'hit [shader](closest-hit-shader.md) più vicino nell'hit più vicino fino a questo momento se è attivo.
*   Chiamare [**IgnoreHit**](ignorehit-function.md), che termina l'hit shader e indica al sistema di continuare la ricerca di riscontri, inclusa la restituzione del controllo a uno shader di intersezione, se è in esecuzione, che restituisce false dal sito di chiamata [**ReportHit**](reporthit-function.md)*. 
*   Restituisce senza chiamare una di queste funzioni intrinseche, che accetta l'hit corrente e indica al sistema di continuare la ricerca di riscontri, inclusa la restituzione del controllo allo shader di intersezione, se presente, che restituisce true nel sito di chiamata [**ReportHit**](reporthit-function.md) per indicare che l'hit è stato accettato.

Anche se una chiamata di hit shader viene terminata da [**IgnoreHit**](ignorehit-function.md) o [**AcceptHitAndEndSearch,**](accepthitandendsearch-function.md)tutte le modifiche apportate al payload del raggio fino a questo momento devono essere mantenute.

## <a name="shader-type-attribute"></a>Attributo Tipo shader

```
[shader("anyhit")]
```

## <a name="example"></a>Esempio

```
[shader("anyhit")]
void anyhit_main( inout MyPayload payload, in MyAttributes attr )
{
    float3 hitLocation = ObjectRayOrigin() + ObjectRayDirection() * RayTCurrent();
    float alpha = computeAlpha(hitLocation, attr, ...);

    // Processing shadow and only care if a hit is registered?
    if (TerminateShadowRay(alpha))
        AcceptHitAndEndSearch(); // aborts function

    // Save alpha contribution and ignoring hit?
    if (SaveAndIgnore(payload, RayTCurrent(), alpha, attr, ...))
        IgnoreHit(); // aborts function

    // do something else
    // return to accept and update closest hit
}
```
