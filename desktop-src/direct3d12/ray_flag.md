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
# <a name="ray_flag-enumeration"></a>\_Enumerazione flag Ray

Flag passati alla funzione [**TraceRay**](traceray-function.md) per eseguire l'override della trasparenza, dell'eliminazione e del comportamento iniziale.

## <a name="syntax"></a>Sintassi


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



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**\_flag Ray \_ None**
</dt> <dd>

Non è stata selezionata alcuna opzione.

</dd> <dt>

<span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**\_flag Ray \_ Force \_ opaco**
</dt> <dd>

Tutte le intersezioni primitive con raggio rilevate in un raytrace vengono considerate opache.  Quindi, nessun hit shader verrà eseguito indipendentemente dal fatto che la geometria di hit specifichi il flag di \_ geometria D3D12 RAYTRACING \_ \_ \_ opaco e indipendentemente dai flag di istanza nell'istanza che è stata raggiunta.

Questo flag si escludono a vicenda con il \_ flag Ray \_ Force \_ non \_ opaco, l' \_ abbattimento dei flag del raggio \_ \_ opaco e l'eliminazione del flag di raggio \_ \_ \_ non \_ opaco.


</dd> <dt>

<span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**\_flag Ray \_ Force \_ non \_ opaco**
</dt> <dd>

Tutte le intersezioni primitive con raggio rilevate in un raytrace vengono considerate non opache.  Quindi, qualsiasi hit shader, se presente, verrà eseguito indipendentemente dal fatto che la geometria di hit specifichi il \_ flag di geometria D3D12 RAYTRACING \_ \_ \_ opaco e indipendentemente dai flag di istanza nell'istanza che è stata raggiunta.
Questo flag si escludono a vicenda con il flag di raggio \_ \_ FORCE_ \OPAQUE, l' \_ abbattimento del flag di Ray \_ \_ opaco e l' \_ \_ abbattimento dei flag \_ dei raggi \_


</dd> <dt>

<span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**\_flag raggio \_ accetta \_ primo \_ hit \_ e \_ fine \_ ricerca**
</dt> <dd>

La prima intersezione della primitiva Ray rilevata in un raytrace causa automaticamente la chiamata di **AcceptHitAndEndSearch** immediatamente dopo l'eventuale hit shader, incluso se non è presente alcun hit shader. 
 
L'unica eccezione è rappresentata dal fatto che il precedente qualsiasi hit shader chiama **IgnoreHit**, nel qual caso il raggio continua a influire in modo tale che il prossimo hit diventi un altro candidato come primo hit.  Per applicare questa eccezione, è necessario che l'eventuale hit shader venga effettivamente eseguito.  Quindi, se l'hit shader viene ignorato perché il hit viene considerato opaco, ad esempio a causa di un flag RAY \_ \_ Force \_ Opaque o D3D12 \_ RAYTRACING \_ Geometry \_ flag \_ Opaque o D3D12 \_ RAYTRACING flag di \_ istanza \_ \_ opaco impostato, viene chiamato **AcceptHitAndEndSearch** .

Se al primo hit è presente un hit shader più vicino, viene richiamato a meno che non \_ sia presente anche il flag di raggio \_ Skip the \_ Closer \_ hit \_ shader.  Il primo hit trovato è considerato "più vicino", anche se potrebbero non essere state visitate altre potenziali riscontri che potrebbero essere più vicini al raggio.

Un utilizzo tipico di questo flag è per le ombreggiature, in cui è necessario trovare solo un singolo hit.


</dd> <dt>

<span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**FLAG di raggio che \_ \_ Ignora l' \_ \_ hit shader più vicino \_**
</dt> <dd>

Anche se è stato eseguito il commit di almeno un hit e il gruppo di hit per il hit più vicino contiene uno shader più vicino, ignorare l'esecuzione dello shader. 

</dd> <dt>

<span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**FLAG dei raggi per l' \_ \_ abbattimento di un \_ \_ \_ triangoli rivolti**
</dt> <dd>

Consente l'abbattimento dei triangoli rivolti verso il retro. Vedere **\_ flag di \_ istanza \_ di D3D12 RAYTRACING** per la selezione dei triangoli di cui è stato eseguito il backup, per istanza.

Per le istanze che specificano il flag di istanza di D3D12 \_ RAYTRACING flag di selezione \_ \_ \_ triangolo \_ \_ disabilitato, questo flag non ha alcun effetto.

Sui tipi geometry diversi dai \_ \_ triangoli di tipo geometrico D3D12 RAYTRACING \_ \_ , questo flag non ha alcun effetto.

Questo flag si escludono a vicenda con \_ i \_ \_ triangoli anteriori per l'abbattimento dei flag di raggio \_ \_ .


</dd> <dt>

<span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**\_flag raggio \_ abbattimento \_ \_ \_ triangoli front-end**
</dt> <dd>

Consente l'abbattimento dei triangoli anteriori. Vedere **\_ flag di \_ istanza \_ di D3D12 RAYTRACING** per la selezione dei triangoli di cui è stato eseguito il backup, per istanza.

Per le istanze che specificano il flag di istanza di D3D12 \_ RAYTRACING flag di selezione \_ \_ \_ triangolo \_ \_ disabilitato, questo flag non ha alcun effetto.

Sui tipi geometry diversi dai \_ \_ triangoli di tipo geometrico D3D12 RAYTRACING \_ \_ , questo flag non ha alcun effetto.

Questo flag si escludono reciprocamente con i \_ \_ \_ \_ triangoli rivolti al ritorno al contrassegno dei flag \_ .


</dd> <dt>

<span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**\_ \_ opacità dell'eliminazione del flag raggio \_**
</dt> <dd>

Esegue l'eliminazione di tutte le primitive considerate opache in base ai relativi flag di geometria e di istanza.

Questo flag si escludono a vicenda con il flag di raggio \_ \_ Force \_ opaque, il \_ flag Ray \_ Force \_ non \_ opaco e l' \_ abbattimento del flag di raggio \_ \_ non \_ opaco.


</dd> <dt>

<span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**\_eliminazione contrassegno \_ flag \_ non \_ opaco**
</dt> <dd>

Esegue l'eliminazione di tutte le primitive considerate non opache in base ai relativi flag di geometria e istanza.

Questo flag si escludono a vicenda con il flag di raggio \_ \_ Force \_ opaque, Ray \_ flag \_ Force \_ non \_ opaco e Ray \_ flag \_ abbattity \_ opaque.


</dd>

## <a name="requirements"></a>Requisiti



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




