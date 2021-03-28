---
title: 'Funzione Texture2DArray:: Gather (S, float, int)'
description: "Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare. | Funzione Texture2DArray:: Gather (S, float, int)"
ms.assetid: b0355158-01c8-45a1-bb5d-29a8c43b1685
keywords:
- Raccolta HLSL funzione
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46866df18a0836b311443a3dd411d74dfa7fb126
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995328"
---
# <a name="texture2darraygathersfloatint-function"></a>Funzione Texture2DArray:: Gather (S, float, int)

Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.

## <a name="syntax"></a>Sintassi

``` syntax
TemplateType Gather(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **Sampler**

Indice del campionatore in base zero.

</dd> <dt>

*posizione* \[ in\]
</dt> <dd>

Tipo: **float3**

Coordinate di esempio (u, v).

</dd> <dt>

*offset* \[ in\]
</dt> <dd>

Tipo: **int2**

Offset applicato alle coordinate di trama prima del campionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **TemplateType**

Valore a quattro componenti il cui tipo corrisponde al tipo di modello.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di raccolta](texture2darray-gather.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




