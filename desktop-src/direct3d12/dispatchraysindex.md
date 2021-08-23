---
description: Ottiene la posizione corrente all'interno della larghezza, dell'altezza e della profondità ottenuta con il valore di sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) intrinseco.
title: 'DispatchRaysIndex '
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: 1b40987c76f42d41d74b7cb3d41f35cc20bd5a6ac1414ae9b010cedcfa7ef9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124166"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex 

Ottiene la posizione corrente all'interno della larghezza, dell'altezza e della profondità ottenuta con il valore di sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) intrinseco.

## <a name="syntax"></a>Sintassi

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>Osservazioni

Questa funzione può essere chiamata dai tipi di shader raytracing seguenti.

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Shader chiamabile**](callable-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Intersection Shader**](intersection-shader.md)
* [**Miss Shader**](miss-shader.md)
* [**Ray Generation Shader**](ray-generation-shader.md)

## <a name="see-also"></a>Vedi anche

* [Informazioni di riferimento su HLSL per Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
