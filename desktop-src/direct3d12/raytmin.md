---
description: Float che rappresenta il punto di partenza parametrico corrente per il raggio.
ms.assetid: ''
title: RayTMin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305063"
---
# <a name="raytmin"></a>RayTMin

Float che rappresenta il punto di partenza parametrico corrente per il raggio. 

## <a name="syntax"></a>Sintassi

```
float RayTMin();

```

## <a name="remarks"></a>Osservazioni

**RayTMin** definisce il punto iniziale del raggio in base alla formula seguente: Origin + (Direction * RayTMin).  L' *origine* e la *direzione* possono trovarsi nel mondo o nello spazio degli oggetti, il che comporta il punto di partenza di un mondo o uno spazio oggetti.

**RayTMin** viene specificato nella chiamata a [**TraceRay**](traceray-function.md)ed è costante per la durata della chiamata.




Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Intersezione shader**](intersection-shader.md)
* [**Lo shader manca**](miss-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




