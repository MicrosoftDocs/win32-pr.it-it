---
description: Ottiene la posizione corrente entro la larghezza, l'altezza e la profondità ottenute con il valore intrinseco di sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) .
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
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2020
ms.locfileid: "106300640"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex 

Ottiene la posizione corrente entro la larghezza, l'altezza e la profondità ottenute con il valore intrinseco di sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) .

## <a name="syntax"></a>Sintassi

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>Osservazioni

Questa funzione può essere chiamata dai seguenti tipi di shader raytracing.

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Richiamabile shader**](callable-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Intersezione shader**](intersection-shader.md)
* [**Lo shader manca**](miss-shader.md)
* [**Shader di generazione del Ray**](ray-generation-shader.md)

## <a name="see-also"></a>Vedi anche

* [Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
