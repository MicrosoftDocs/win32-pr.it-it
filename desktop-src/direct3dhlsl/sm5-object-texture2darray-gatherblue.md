---
title: Funzione Texture2DArray::GatherBlue(S,float,int)
description: Restituisce i componenti blu dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare. | Funzione Texture2DArray::GatherBlue(S,float,int)
ms.assetid: f81596b5-afd1-4baf-b6c0-ca4661a3ef22
keywords:
- Funzione GatherBlue HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a81aef4d47b3113713f64093bb39567b566ad47969a937b70e4d000073b294a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724815"
---
# <a name="texture2darraygatherbluesfloatint-function"></a>Funzione Texture2DArray::GatherBlue(S,float,int)

Restituisce i componenti blu dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.

## <a name="syntax"></a>Sintassi

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **sampler**

Indice del campionatore in base zero.

</dd> <dt>

*location* \[ Pollici\]
</dt> <dd>

Tipo: **float3**

Coordinate di esempio (u,v).

</dd> <dt>

*offset* \[ Pollici\]
</dt> <dd>

Tipo: **int2**

Offset applicato alla coordinata della trama prima del campionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **TemplateType**

Valore a quattro componenti il cui tipo è uguale al tipo di modello.

## <a name="remarks"></a>Commenti

I campioni di trama possono essere usati per l'interpolazione bilineare.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi GatherBlue](texture2darray-gatherblue.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




