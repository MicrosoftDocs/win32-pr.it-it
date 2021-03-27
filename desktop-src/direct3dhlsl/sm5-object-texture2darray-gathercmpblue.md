---
title: 'Funzione Texture2DArray:: GatherCmpBlue (S, float, float, int)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto. | Funzione Texture2DArray:: GatherCmpBlue (S, float, float, int)"
ms.assetid: 5fa23e27-368a-4c55-b6d6-33506c932a43
keywords:
- Funzione GatherCmpBlue HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c645333cc45c6de55a609439445936f65b85f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761710"
---
# <a name="texture2darraygathercmpbluesfloatfloatint-function"></a>Funzione Texture2DArray:: GatherCmpBlue (S, float, float, int)

Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente blu e un valore di confronto.

## <a name="syntax"></a>Sintassi

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **SamplerComparisonState**

Indice del campionatore in base zero.

</dd> <dt>

*posizione* \[ in\]
</dt> <dd>

Tipo: **float3**

Coordinate di esempio (u, v).

</dd> <dt>

*Confronta \_ valore* \[ in\]
</dt> <dd>

Tipo: **float**

Valore da confrontare con ogni valore campionato.

</dd> <dt>

*offset* \[ in\]
</dt> <dd>

Tipo: **int2**

Offset applicato alla coordinata di trama prima del campionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **float4**

Un valore a quattro componenti, ogni componente è il risultato di un confronto per ogni componente.

## <a name="remarks"></a>Commenti

Gli esempi di trama possono essere usati per l'interpolazione bilineare.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi GatherCmpBlue](texture2darray-gathercmpblue.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




