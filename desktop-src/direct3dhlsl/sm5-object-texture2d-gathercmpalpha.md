---
title: Funzione Texture2D::GatherCmpAlpha(S,float,float,int)
description: Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto del relativo componente alfa con un valore di confronto. | Funzione Texture2D::GatherCmpAlpha(S,float,float,int)
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
keywords:
- Funzione GatherCmpAlpha HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f6e350ed14482646562121d910a8bd35f30403acf8dbde7df249ee1bc6ca800a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789604"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a>Funzione Texture2D::GatherCmpAlpha(S,float,float,int)

Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto del relativo componente alfa con un valore di confronto.

## <a name="syntax"></a>Sintassi

``` syntax
float4 GatherCmpAlpha(
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

[Metodi GatherCmpAlpha](texture2d-gathercmpalpha.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




