---
description: I valori di larghezza, altezza e profondità dalla struttura D3D12_DISPATCH_RAYS_DESC specificata nella chiamata DispatchRays di origine.
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: e35c967ad831c82912d2962da72d9ad17eab1c15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305311"
---
# <a name="dispatchraysdimensions"></a>DispatchRaysDimensions

I valori di larghezza, altezza e profondità della struttura **D3D12 di \_ distribuzione dei \_ raggi \_** di recapito specificata nella chiamata [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) di origine.

## <a name="syntax"></a>Sintassi

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a>Osservazioni

Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Richiamabile shader**](callable-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Intersezione shader**](intersection-shader.md)
* [**Lo shader manca**](miss-shader.md)
* [**Shader di generazione del Ray**](ray-generation-shader.md)

## <a name="see-also"></a>Vedi anche

* [Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
