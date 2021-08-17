---
title: Funzione Texture2DArray::GatherCmpRed(S,float,float,int)
description: Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il componente rosso e un valore di confronto. | Funzione Texture2DArray::GatherCmpRed(S,float,float,int)
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
ms.openlocfilehash: aea723bbcdc2822adb8084cbdb5feff155165158d3abaf872a96259a77accdcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724612"
---
# <a name="texture2darraygathercmpredsfloatfloatint-function"></a>Funzione Texture2DArray::GatherCmpRed(S,float,float,int)

Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il componente rosso e un valore di confronto.

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

*location* \[ Pollici\]
</dt> <dd>

Tipo: **float3**

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

[Metodi GatherCmpRed](texture2darray-gathercmpred.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




