---
title: Funzione Texture2D::GatherCmpGreen(S,float,float,int)
description: Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il componente verde e un valore di confronto. | Funzione Texture2D::GatherCmpGreen(S,float,float,int)
ms.assetid: 5a11ce0c-56b2-460a-95d7-15688dd158ff
keywords:
- Funzione GatherCmpGreen HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44ebf3590a756ea0bb78e6cc9c636523cb584cdd862059418f7b7c9508bfecfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095121"
---
# <a name="texture2dgathercmpgreensfloatfloatint-function"></a>Funzione Texture2D::GatherCmpGreen(S,float,float,int)

Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il componente verde e un valore di confronto.

## <a name="syntax"></a>Sintassi

``` syntax
float4 GatherCmpGreen(
  in SamplerComparisonState s,
  in float2 location,
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

*location* \[ Pollici\]
</dt> <dd>

Tipo: **float2**

Coordinate di esempio (u,v).

</dd> <dt>

*confrontare \_ il valore* \[ in\]
</dt> <dd>

Tipo: **float**

Valore da confrontare con ogni valore campionato.

</dd> <dt>

*offset* \[ Pollici\]
</dt> <dd>

Tipo: **int2**

Offset applicato alla coordinata di trama prima del campionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **float4**

Un valore a quattro componenti, ogni componente è il risultato di un confronto per componente.

## <a name="remarks"></a>Commenti

Gli esempi di trama possono essere usati per l'interpolazione bilineare.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi GatherCmpGreen](texture2d-gathercmpgreen.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




