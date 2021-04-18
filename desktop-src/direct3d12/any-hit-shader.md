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
# <a name="any-hit-shader"></a><span data-ttu-id="9c2ff-103">Qualsiasi hit shader</span><span class="sxs-lookup"><span data-stu-id="9c2ff-103">Any Hit Shader</span></span>

<span data-ttu-id="9c2ff-104">Shader richiamato quando le intersezioni del raggio non sono opache.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-104">A shader that is invoked when ray intersections are not opaque.</span></span> 

<span data-ttu-id="9c2ff-105">Tutti gli hit shader devono dichiarare un parametro di payload seguito da un parametro attributes.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-105">Any hit shaders must declare a payload parameter followed by an attributes parameter.</span></span> <span data-ttu-id="9c2ff-106">Ognuno di questi parametri deve essere un tipo di struttura definito dall'utente che corrisponde ai tipi utilizzati rispettivamente per [**TraceRay**](traceray-function.md) e [**ReportHit**](reporthit-function.md) oppure la [**struttura degli attributi di intersezione**](intersection-attributes.md) quando si utilizza l'intersezione del triangolo a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-106">Each of these parameters must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed function triangle intersection is used.</span></span>

<span data-ttu-id="9c2ff-107">Qualsiasi hit shader può effettuare i seguenti tipi di operazioni:</span><span class="sxs-lookup"><span data-stu-id="9c2ff-107">Any hit shaders may perform the following kinds of operations:</span></span>

*   <span data-ttu-id="9c2ff-108">Leggere e modificare il payload del raggio: (InOut payload_t rayPayload)</span><span class="sxs-lookup"><span data-stu-id="9c2ff-108">Read and modify the ray payload: (inout payload_t rayPayload)</span></span>
*   <span data-ttu-id="9c2ff-109">Leggere gli attributi di intersezione: (in attr_t attributi)</span><span class="sxs-lookup"><span data-stu-id="9c2ff-109">Read the intersection attributes: (in attr_t attributes)</span></span>
*   <span data-ttu-id="9c2ff-110">Call [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), che accetta il hit corrente, termina l' [eventuale hit shader](any-hit-shader.md), termina l' [intersezione dello shader](intersection-shader.md) , se presente, ed esegue lo [shader più vicino](closest-hit-shader.md) all'hit più vicino se è attivo.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-110">Call [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), which accepts the current hit, ends the [any hit shader](any-hit-shader.md), ends the [intersection shader](intersection-shader.md) if one is present, and executes the [closest hit shader](closest-hit-shader.md) on the closest hit so far if it is active.</span></span>
*   <span data-ttu-id="9c2ff-111">Chiamare [**IgnoreHit**](ignorehit-function.md), che termina l'eventuale hit shader e indica al sistema di continuare la ricerca dei riscontri, inclusa la restituzione del controllo a un'intersezione shader, se è attualmente in esecuzione, restituendo false dal sito di chiamata [**ReportHit**](reporthit-function.md)\*.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-111">Call [**IgnoreHit**](ignorehit-function.md), which ends the any hit shader and tells the system to continue searching for hits, including returning control to an intersection shader, if it is currently executing, returning false from the [**ReportHit**](reporthit-function.md)\* call site.</span></span> 
*   <span data-ttu-id="9c2ff-112">Restituire senza chiamare uno di questi intrinseci, che accetta l'hit corrente e indica al sistema di continuare la ricerca dei riscontri, incluso il controllo restituito all'intersezione shader, se presente, restituendo true al sito di chiamata [**ReportHit**](reporthit-function.md) per indicare che il hit è stato accettato.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-112">Return without calling either of these intrinsics, which accepts the current hit and tells the system to continue searching for hits, including returning control to the intersection shader if there is one, returning true at the [**ReportHit**](reporthit-function.md) call site to indicate that the hit was accepted.</span></span>

<span data-ttu-id="9c2ff-113">Anche se una chiamata a qualsiasi hit shader viene terminata da [**IgnoreHit**](ignorehit-function.md) o [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), tutte le modifiche apportate al payload del ray fino a questo punto devono essere conservate.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-113">Even if an any hit shader invocation is ended by [**IgnoreHit**](ignorehit-function.md) or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), any modifications made to the ray payload so far must still be retained.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="9c2ff-114">Attributo di tipo shader</span><span class="sxs-lookup"><span data-stu-id="9c2ff-114">Shader Type attribute</span></span>

```
[shader("anyhit")]
```

## <a name="example"></a><span data-ttu-id="9c2ff-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="9c2ff-115">Example</span></span>

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
