---
description: I valori di larghezza, altezza e profondità D3D12_DISPATCH_RAYS_DESC struttura specificata nella chiamata DispatchRays di origine.
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
ms.openlocfilehash: 4f68b7bdd5f5ea92074b366b9f981f490a9801079b29def17ba66770abd3c5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989491"
---
# <a name="dispatchraysdimensions"></a>DispatchRaysDimensions

Valori di larghezza, altezza e profondità della struttura **D3D12 \_ DISPATCH \_ RAYS \_ DESC** specificata nella chiamata [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) di origine.

## <a name="syntax"></a>Sintassi

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a>Osservazioni

Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Shader chiamabile**](callable-shader.md)
* [**Hit Shader più vicino**](closest-hit-shader.md)
* [**Shader di intersezione**](intersection-shader.md)
* [**Miss Shader**](miss-shader.md)
* [**Shader di generazione di raggi**](ray-generation-shader.md)

## <a name="see-also"></a>Vedi anche

* [Informazioni di riferimento su Direct3D 12 Raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
