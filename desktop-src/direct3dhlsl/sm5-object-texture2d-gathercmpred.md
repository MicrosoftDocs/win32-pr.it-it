---
title: Funzione Texture2D::GatherCmpRed(S,float,float,int)
description: Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto. | Funzione Texture2D::GatherCmpRed(S,float,float,int)
ms.assetid: bd5fdd3b-c1b0-4cb0-aec5-9fe020420e6c
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
ms.openlocfilehash: 07786eb41dfd45ce911717ee17b14c4694ab1972115b92a79076aef358ab0ad6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095091"
---
# <a name="texture2dgathercmpredsfloatfloatint-function"></a>Funzione Texture2D::GatherCmpRed(S,float,float,int)

Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.

## <a name="syntax"></a>Sintassi

``` syntax
float4 GatherCmpRed(
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

Offset applicato alla coordinata della trama prima del campionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **float4**

Valore a quattro componenti, ogni componente è il risultato di un confronto per componente.

## <a name="remarks"></a>Commenti

I campioni di trama possono essere usati per l'interpolazione bilineare.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi GatherCmpRed](texture2d-gathercmpred.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




