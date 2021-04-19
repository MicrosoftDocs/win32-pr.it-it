---
description: Recupera l'indice generato automaticamente della primitiva all'interno della geometria all'interno dell'istanza della struttura di accelerazione di livello inferiore.
ms.assetid: ''
title: PrimitiveIndex
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrimitiveIndex
api_type:
- NA
ms.openlocfilehash: d6d1e8ba338a3fb567b583b42074210b514ef360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305069"
---
# <a name="primitiveindex-function"></a>PrimitiveIndex (funzione)

Recupera l'indice generato automaticamente della primitiva all'interno della geometria all'interno dell'istanza della struttura di accelerazione di livello inferiore.

## <a name="syntax"></a>Sintassi

```
uint PrimitiveIndex();
```

## <a name="remarks"></a>Osservazioni

Per **i \_ \_ \_ \_ triangoli del tipo di geometria RAYTRACING di D3D12**, questo è l'indice del triangolo all'interno dell'oggetto Geometry.

Per **la \_ \_ \_ \_ \_ primitiva \_ procedurale di tipo Geometry RAYTRACING D3D12**, questo è l'indice nella matrice AABB che definisce l'oggetto Geometry.

Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Intersezione shader**](intersection-shader.md)

## <a name="see-also"></a>Vedi anche

* [Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
