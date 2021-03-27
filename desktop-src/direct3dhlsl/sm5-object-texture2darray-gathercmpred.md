---
title: 'Funzione Texture2DArray:: GatherCmpRed (S, float, float, int)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto. | Funzione Texture2DArray:: GatherCmpRed (S, float, float, int)"
ms.assetid: aa7fadf8-fe96-406a-9c93-9ae0c59ef087
keywords:
- Funzione GatherCmpRed HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cf0f7094c7e535a84e6d8fd6ba7e87bb702dbfd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995512"
---
# <a name="texture2darraygathercmpredsfloatfloatint-function"></a>Funzione Texture2DArray:: GatherCmpRed (S, float, float, int)

Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.

## <a name="syntax"></a>Sintassi

``` syntax
float4 GatherCmpRed(
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

[Metodi GatherCmpRed](texture2darray-gathercmpred.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




