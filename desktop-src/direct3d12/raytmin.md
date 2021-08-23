---
description: Valore float che rappresenta il punto iniziale parametrico corrente per il raggio.
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
ms.openlocfilehash: 5429574480cfda071dfec93cea771211bab578bdaecb4513c76f43c4d820b22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989481"
---
# <a name="raytmin"></a>RayTMin

Valore float che rappresenta il punto iniziale parametrico corrente per il raggio. 

## <a name="syntax"></a>Sintassi

```
float RayTMin();

```

## <a name="remarks"></a>Osservazioni

**RayTMin** definisce il punto iniziale del raggio in base alla formula seguente: Origine + (Direzione * RayTMin).  *L'origine* *e la* direzione possono essere nello spazio del mondo o dell'oggetto, con il risultato di un punto iniziale dello spazio oggetto o di un mondo.

**RayTMin** viene specificato nella chiamata a [**TraceRay**](traceray-function.md)ed è costante per la durata della chiamata.




Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Hit Shader più vicino**](closest-hit-shader.md)
* [**Shader di intersezione**](intersection-shader.md)
* [**Miss Shader**](miss-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Direct3D 12 Raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




