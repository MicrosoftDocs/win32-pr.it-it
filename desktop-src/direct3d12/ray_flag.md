---
description: Flag passati alla funzione TraceRay per eseguire l'override della trasparenza, dell'eliminazione e del comportamento iniziale.
ms.assetid: ''
title: Enumerazione RAY_FLAG
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
ms.openlocfilehash: 31d6a002e5f3f4eeb5f86e671be0904d61cb916d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305068"
---
# <a name="ray_flag-enumeration"></a><span data-ttu-id="deefe-103">\_Enumerazione flag Ray</span><span class="sxs-lookup"><span data-stu-id="deefe-103">RAY\_FLAG enumeration</span></span>

<span data-ttu-id="deefe-104">Flag passati alla funzione [**TraceRay**](traceray-function.md) per eseguire l'override della trasparenza, dell'eliminazione e del comportamento iniziale.</span><span class="sxs-lookup"><span data-stu-id="deefe-104">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="deefe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="deefe-105">Syntax</span></span>


```
enum RAY_FLAG : uint
{
    RAY_FLAG_NONE                            = 0x00,
    RAY_FLAG_FORCE_OPAQUE                    = 0x01,
    RAY_FLAG_FORCE_NON_OPAQUE                = 0x02,
    RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH = 0x04,
    RAY_FLAG_SKIP_CLOSEST_HIT_SHADER         = 0x08,
    RAY_FLAG_CULL_BACK_FACING_TRIANGLES      = 0x10,
    RAY_FLAG_CULL_FRONT_FACING_TRIANGLES     = 0x20,
    RAY_FLAG_CULL_OPAQUE                     = 0x40,
    RAY_FLAG_CULL_NON_OPAQUE                 = 0x80,
}; 
```



## <a name="constants"></a><span data-ttu-id="deefe-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="deefe-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="deefe-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**\_flag Ray \_ None**</span><span class="sxs-lookup"><span data-stu-id="deefe-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**RAY\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="deefe-108">Non è stata selezionata alcuna opzione.</span><span class="sxs-lookup"><span data-stu-id="deefe-108">No options selected.</span></span>

</dd> <dt>

<span data-ttu-id="deefe-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**\_flag Ray \_ Force \_ opaco**</span><span class="sxs-lookup"><span data-stu-id="deefe-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**RAY\_FLAG\_FORCE\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="deefe-110">Tutte le intersezioni primitive con raggio rilevate in un raytrace vengono considerate opache.</span><span class="sxs-lookup"><span data-stu-id="deefe-110">All ray-primitive intersections encountered in a raytrace are treated as opaque.</span></span>  <span data-ttu-id="deefe-111">Quindi, nessun hit shader verrà eseguito indipendentemente dal fatto che la geometria di hit specifichi il flag di \_ geometria D3D12 RAYTRACING \_ \_ \_ opaco e indipendentemente dai flag di istanza nell'istanza che è stata raggiunta.</span><span class="sxs-lookup"><span data-stu-id="deefe-111">So no any hit shaders will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>

<span data-ttu-id="deefe-112">Questo flag si escludono a vicenda con il \_ flag Ray \_ Force \_ non \_ opaco, l' \_ abbattimento dei flag del raggio \_ \_ opaco e l'eliminazione del flag di raggio \_ \_ \_ non \_ opaco.</span><span class="sxs-lookup"><span data-stu-id="deefe-112">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_NON\_OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="deefe-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**\_flag Ray \_ Force \_ non \_ opaco**</span><span class="sxs-lookup"><span data-stu-id="deefe-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**RAY\_FLAG\_FORCE\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="deefe-114">Tutte le intersezioni primitive con raggio rilevate in un raytrace vengono considerate non opache.</span><span class="sxs-lookup"><span data-stu-id="deefe-114">All ray-primitive intersections encountered in a raytrace are treated as non-opaque.</span></span>  <span data-ttu-id="deefe-115">Quindi, qualsiasi hit shader, se presente, verrà eseguito indipendentemente dal fatto che la geometria di hit specifichi il \_ flag di geometria D3D12 RAYTRACING \_ \_ \_ opaco e indipendentemente dai flag di istanza nell'istanza che è stata raggiunta.</span><span class="sxs-lookup"><span data-stu-id="deefe-115">So any hit shaders, if present, will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>
<span data-ttu-id="deefe-116">Questo flag si escludono a vicenda con il flag di raggio \_ \_ FORCE_ \OPAQUE, l' \_ abbattimento del flag di Ray \_ \_ opaco e l' \_ \_ abbattimento dei flag \_ dei raggi \_</span><span class="sxs-lookup"><span data-stu-id="deefe-116">This flag is mutually exclusive with RAY\_FLAG\_FORCE_\OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="deefe-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**\_flag raggio \_ accetta \_ primo \_ hit \_ e \_ fine \_ ricerca**</span><span class="sxs-lookup"><span data-stu-id="deefe-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**RAY\_FLAG\_ACCEPT\_FIRST\_HIT\_AND\_END\_SEARCH**</span></span>
</dt> <dd>

<span data-ttu-id="deefe-118">La prima intersezione della primitiva Ray rilevata in un raytrace causa automaticamente la chiamata di **AcceptHitAndEndSearch** immediatamente dopo l'eventuale hit shader, incluso se non è presente alcun hit shader.</span><span class="sxs-lookup"><span data-stu-id="deefe-118">The first ray-primitive intersection encountered in a raytrace automatically causes **AcceptHitAndEndSearch** to be called immediately after the any hit shader, including if there is no any hit shader.</span></span> 
 
<span data-ttu-id="deefe-119">L'unica eccezione è rappresentata dal fatto che il precedente qualsiasi hit shader chiama **IgnoreHit**, nel qual caso il raggio continua a influire in modo tale che il prossimo hit diventi un altro candidato come primo hit.</span><span class="sxs-lookup"><span data-stu-id="deefe-119">The only exception is when the preceding any hit shader calls **IgnoreHit**, in which case the ray continues unaffected such that the next hit becomes another candidate to be the first hit.</span></span>  <span data-ttu-id="deefe-120">Per applicare questa eccezione, è necessario che l'eventuale hit shader venga effettivamente eseguito.</span><span class="sxs-lookup"><span data-stu-id="deefe-120">For this exception to apply, the any hit shader has to actually be executed.</span></span>  <span data-ttu-id="deefe-121">Quindi, se l'hit shader viene ignorato perché il hit viene considerato opaco, ad esempio a causa di un flag RAY \_ \_ Force \_ Opaque o D3D12 \_ RAYTRACING \_ Geometry \_ flag \_ Opaque o D3D12 \_ RAYTRACING flag di \_ istanza \_ \_ opaco impostato, viene chiamato **AcceptHitAndEndSearch** .</span><span class="sxs-lookup"><span data-stu-id="deefe-121">So if the any hit shader is skipped because the hit is treated as opaque (e.g. due to RAY\_FLAG\_FORCE\_OPAQUE or D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE or D3D12\_RAYTRACING\_INSTANCE\_FLAG\_OPAQUE being set), then **AcceptHitAndEndSearch** is called.</span></span>

<span data-ttu-id="deefe-122">Se al primo hit è presente un hit shader più vicino, viene richiamato a meno che non \_ sia presente anche il flag di raggio \_ Skip the \_ Closer \_ hit \_ shader.</span><span class="sxs-lookup"><span data-stu-id="deefe-122">If a closest hit shader is present at the first hit, it gets invoked unless RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER is also present.</span></span>  <span data-ttu-id="deefe-123">Il primo hit trovato è considerato "più vicino", anche se potrebbero non essere state visitate altre potenziali riscontri che potrebbero essere più vicini al raggio.</span><span class="sxs-lookup"><span data-stu-id="deefe-123">The one hit that was found is considered “closest”, even though other potential hits that might be closer on the ray may not have been visited.</span></span>

<span data-ttu-id="deefe-124">Un utilizzo tipico di questo flag è per le ombreggiature, in cui è necessario trovare solo un singolo hit.</span><span class="sxs-lookup"><span data-stu-id="deefe-124">A typical use for this flag is for shadows, where only a single hit needs to be found.</span></span>


</dd> <dt>

<span data-ttu-id="deefe-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**FLAG di raggio che \_ \_ Ignora l' \_ \_ hit shader più vicino \_**</span><span class="sxs-lookup"><span data-stu-id="deefe-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER**</span></span>
</dt> <dd>

<span data-ttu-id="deefe-126">Anche se è stato eseguito il commit di almeno un hit e il gruppo di hit per il hit più vicino contiene uno shader più vicino, ignorare l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="deefe-126">Even if at least one hit has been committed, and the hit group for the closest hit contains a closest hit shader, skip execution of that shader.</span></span> 

</dd> <dt>

<span data-ttu-id="deefe-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**FLAG dei raggi per l' \_ \_ abbattimento di un \_ \_ \_ triangoli rivolti**</span><span class="sxs-lookup"><span data-stu-id="deefe-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="deefe-128">Consente l'abbattimento dei triangoli rivolti verso il retro.</span><span class="sxs-lookup"><span data-stu-id="deefe-128">Enables culling of back facing triangles.</span></span> <span data-ttu-id="deefe-129">Vedere **\_ flag di \_ istanza \_ di D3D12 RAYTRACING** per la selezione dei triangoli di cui è stato eseguito il backup, per istanza.</span><span class="sxs-lookup"><span data-stu-id="deefe-129">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="deefe-130">Per le istanze che specificano il flag di istanza di D3D12 \_ RAYTRACING flag di selezione \_ \_ \_ triangolo \_ \_ disabilitato, questo flag non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="deefe-130">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="deefe-131">Sui tipi geometry diversi dai \_ \_ triangoli di tipo geometrico D3D12 RAYTRACING \_ \_ , questo flag non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="deefe-131">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="deefe-132">Questo flag si escludono a vicenda con \_ i \_ \_ triangoli anteriori per l'abbattimento dei flag di raggio \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="deefe-132">This flag is mutually exclusive with RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="deefe-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**\_flag raggio \_ abbattimento \_ \_ \_ triangoli front-end**</span><span class="sxs-lookup"><span data-stu-id="deefe-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="deefe-134">Consente l'abbattimento dei triangoli anteriori.</span><span class="sxs-lookup"><span data-stu-id="deefe-134">Enables culling of front facing triangles.</span></span> <span data-ttu-id="deefe-135">Vedere **\_ flag di \_ istanza \_ di D3D12 RAYTRACING** per la selezione dei triangoli di cui è stato eseguito il backup, per istanza.</span><span class="sxs-lookup"><span data-stu-id="deefe-135">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="deefe-136">Per le istanze che specificano il flag di istanza di D3D12 \_ RAYTRACING flag di selezione \_ \_ \_ triangolo \_ \_ disabilitato, questo flag non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="deefe-136">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="deefe-137">Sui tipi geometry diversi dai \_ \_ triangoli di tipo geometrico D3D12 RAYTRACING \_ \_ , questo flag non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="deefe-137">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="deefe-138">Questo flag si escludono reciprocamente con i \_ \_ \_ \_ triangoli rivolti al ritorno al contrassegno dei flag \_ .</span><span class="sxs-lookup"><span data-stu-id="deefe-138">This flag is mutually exclusive with RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="deefe-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**\_ \_ opacità dell'eliminazione del flag raggio \_**</span><span class="sxs-lookup"><span data-stu-id="deefe-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**RAY\_FLAG\_CULL\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="deefe-140">Esegue l'eliminazione di tutte le primitive considerate opache in base ai relativi flag di geometria e di istanza.</span><span class="sxs-lookup"><span data-stu-id="deefe-140">Culls all primitives that are considered opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="deefe-141">Questo flag si escludono a vicenda con il flag di raggio \_ \_ Force \_ opaque, il \_ flag Ray \_ Force \_ non \_ opaco e l' \_ abbattimento del flag di raggio \_ \_ non \_ opaco.</span><span class="sxs-lookup"><span data-stu-id="deefe-141">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="deefe-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**\_eliminazione contrassegno \_ flag \_ non \_ opaco**</span><span class="sxs-lookup"><span data-stu-id="deefe-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**RAY\_FLAG\_CULL\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="deefe-143">Esegue l'eliminazione di tutte le primitive considerate non opache in base ai relativi flag di geometria e istanza.</span><span class="sxs-lookup"><span data-stu-id="deefe-143">Culls all primitives that are considered non-opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="deefe-144">Questo flag si escludono a vicenda con il flag di raggio \_ \_ Force \_ opaque, Ray \_ flag \_ Force \_ non \_ opaco e Ray \_ flag \_ abbattity \_ opaque.</span><span class="sxs-lookup"><span data-stu-id="deefe-144">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_OPAQUE.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="deefe-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="deefe-145">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="deefe-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="deefe-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deefe-147">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="deefe-147">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




