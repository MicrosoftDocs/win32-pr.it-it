---
description: Shader richiamato quando le intersezioni del raggio non sono opache.
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
ms.openlocfilehash: aad2f8b94f6ea53d500d285cac3555f5ff8b95f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304710"
---
# <a name="any-hit-shader"></a>Qualsiasi hit shader

Shader richiamato quando le intersezioni del raggio non sono opache. 

Tutti gli hit shader devono dichiarare un parametro di payload seguito da un parametro attributes. Ognuno di questi parametri deve essere un tipo di struttura definito dall'utente che corrisponde ai tipi utilizzati rispettivamente per [**TraceRay**](traceray-function.md) e [**ReportHit**](reporthit-function.md) oppure la [**struttura degli attributi di intersezione**](intersection-attributes.md) quando si utilizza l'intersezione del triangolo a funzione fissa.

Qualsiasi hit shader può effettuare i seguenti tipi di operazioni:

*   Leggere e modificare il payload del raggio: (InOut payload_t rayPayload)
*   Leggere gli attributi di intersezione: (in attr_t attributi)
*   Call [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), che accetta il hit corrente, termina l' [eventuale hit shader](any-hit-shader.md), termina l' [intersezione dello shader](intersection-shader.md) , se presente, ed esegue lo [shader più vicino](closest-hit-shader.md) all'hit più vicino se è attivo.
*   Chiamare [**IgnoreHit**](ignorehit-function.md), che termina l'eventuale hit shader e indica al sistema di continuare la ricerca dei riscontri, inclusa la restituzione del controllo a un'intersezione shader, se è attualmente in esecuzione, restituendo false dal sito di chiamata [**ReportHit**](reporthit-function.md)*. 
*   Restituire senza chiamare uno di questi intrinseci, che accetta l'hit corrente e indica al sistema di continuare la ricerca dei riscontri, incluso il controllo restituito all'intersezione shader, se presente, restituendo true al sito di chiamata [**ReportHit**](reporthit-function.md) per indicare che il hit è stato accettato.

Anche se una chiamata a qualsiasi hit shader viene terminata da [**IgnoreHit**](ignorehit-function.md) o [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), tutte le modifiche apportate al payload del ray fino a questo punto devono essere conservate.

## <a name="shader-type-attribute"></a>Attributo di tipo shader

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
