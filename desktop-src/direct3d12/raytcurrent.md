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
# <a name="raytcurrent"></a>RayTCurrent

Valore float che rappresenta il punto finale parametrico corrente per il raggio.  

## <a name="syntax"></a>Sintassi

```
float RayTCurrent();

```


## <a name="remarks"></a>Osservazioni

**RayTCurrent** definisce il punto finale corrente del raggio in base alla formula seguente: Origin + (Direction * RayTCurrent).  L' *origine* e la *direzione* possono trovarsi nel mondo o nello spazio degli oggetti, che determina un punto finale di un mondo o di un oggetto.

**RayTCurrent** viene inizializzato nella chiamata Call [**TraceRay**](traceray-function.md) con il valore [**RayDesc:: tmax**](raydesc.md) , quindi viene aggiornato durante la query di traccia mentre le intersezioni vengono segnalate (in qualsiasi hit) e accettate.

Nell' [intersezione shader](intersection-shader.md), rappresenta la distanza fino all'intersezione più vicina rilevata finora.  Verrà aggiornato dopo () al valore di SETI specificato se il hit è stato accettato.

In [qualsiasi hit shader](any-hit-shader.md), rappresenta la distanza dell'intersezione corrente da segnalare.

Nello [shader più vicino](closest-hit-shader.md), rappresenta la distanza dall'intersezione più vicina accettata.

Nel [mancato shader](miss-shader.md), è uguale a *TMAX* passato alla chiamata **TraceRay** .


Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Intersezione shader**](intersection-shader.md)
* [**Lo shader manca**](miss-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




