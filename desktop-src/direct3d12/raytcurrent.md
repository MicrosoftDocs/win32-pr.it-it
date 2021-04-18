---
description: Valore float che rappresenta il punto finale parametrico corrente per il raggio.
ms.assetid: ''
title: RayTCurrent
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 4f090bab88c6be671ca0614255fd7bdebb0d1549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305065"
---
# <a name="raytcurrent"></a><span data-ttu-id="21341-103">RayTCurrent</span><span class="sxs-lookup"><span data-stu-id="21341-103">RayTCurrent</span></span>

<span data-ttu-id="21341-104">Valore float che rappresenta il punto finale parametrico corrente per il raggio.</span><span class="sxs-lookup"><span data-stu-id="21341-104">A float representing the current parametric ending point for the ray.</span></span>  

## <a name="syntax"></a><span data-ttu-id="21341-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21341-105">Syntax</span></span>

```
float RayTCurrent();

```


## <a name="remarks"></a><span data-ttu-id="21341-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="21341-106">Remarks</span></span>

<span data-ttu-id="21341-107">**RayTCurrent** definisce il punto finale corrente del raggio in base alla formula seguente: Origin + (Direction \* RayTCurrent).</span><span class="sxs-lookup"><span data-stu-id="21341-107">**RayTCurrent** defines the current ending point of the ray according to the following formula: Origin + (Direction \* RayTCurrent).</span></span>  <span data-ttu-id="21341-108">L' *origine* e la *direzione* possono trovarsi nel mondo o nello spazio degli oggetti, che determina un punto finale di un mondo o di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="21341-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space ending point.</span></span>

<span data-ttu-id="21341-109">**RayTCurrent** viene inizializzato nella chiamata Call [**TraceRay**](traceray-function.md) con il valore [**RayDesc:: tmax**](raydesc.md) , quindi viene aggiornato durante la query di traccia mentre le intersezioni vengono segnalate (in qualsiasi hit) e accettate.</span><span class="sxs-lookup"><span data-stu-id="21341-109">**RayTCurrent** is initialized in the call [**TraceRay**](traceray-function.md) call with the [**RayDesc::TMax**](raydesc.md) value and then is updated during the trace query as intersections are reported (in the any hit), and accepted.</span></span>

<span data-ttu-id="21341-110">Nell' [intersezione shader](intersection-shader.md), rappresenta la distanza fino all'intersezione più vicina rilevata finora.</span><span class="sxs-lookup"><span data-stu-id="21341-110">In the [intersection shader](intersection-shader.md), it represents the distance to the closest intersection found so far.</span></span>  <span data-ttu-id="21341-111">Verrà aggiornato dopo () al valore di SETI specificato se il hit è stato accettato.</span><span class="sxs-lookup"><span data-stu-id="21341-111">It will be updated after () to the THit value provided if the hit was accepted.</span></span>

<span data-ttu-id="21341-112">In [qualsiasi hit shader](any-hit-shader.md), rappresenta la distanza dell'intersezione corrente da segnalare.</span><span class="sxs-lookup"><span data-stu-id="21341-112">In the [any hit shader](any-hit-shader.md), it represents the distance to the current intersection being reported.</span></span>

<span data-ttu-id="21341-113">Nello [shader più vicino](closest-hit-shader.md), rappresenta la distanza dall'intersezione più vicina accettata.</span><span class="sxs-lookup"><span data-stu-id="21341-113">In the [closest hit shader](closest-hit-shader.md), it represents the distance to the closest intersection accepted.</span></span>

<span data-ttu-id="21341-114">Nel [mancato shader](miss-shader.md), è uguale a *TMAX* passato alla chiamata **TraceRay** .</span><span class="sxs-lookup"><span data-stu-id="21341-114">In the [miss shader](miss-shader.md), it is equal to *TMax* passed to the **TraceRay** call.</span></span>


<span data-ttu-id="21341-115">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:</span><span class="sxs-lookup"><span data-stu-id="21341-115">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="21341-116">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="21341-116">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="21341-117">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="21341-117">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="21341-118">**Intersezione shader**</span><span class="sxs-lookup"><span data-stu-id="21341-118">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="21341-119">**Lo shader manca**</span><span class="sxs-lookup"><span data-stu-id="21341-119">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="21341-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21341-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21341-121">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="21341-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




