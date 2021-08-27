---
title: Funzione Texture2DArray::GatherAlpha(S,float,int)
description: Restituisce i componenti alfa dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare. | Funzione Texture2DArray::GatherAlpha(S,float,int)
ms.assetid: d7270277-53c1-4034-bf66-9a95bc1b51e4
keywords:
- Funzione GatherAlpha HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e79805ff931c6fe2da880c3ae090b72b87713b1c0547e6bafcf5986f07b810f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118221"
---
# <a name="texture2darraygatheralphasfloatint-function"></a>Funzione Texture2DArray::GatherAlpha(S,float,int)

Restituisce i componenti alfa dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.

## <a name="syntax"></a>Sintassi

``` syntax
TemplateType GatherAlpha(
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

[Metodi GatherAlpha](texture2darray-gatheralpha.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




