---
title: Funzione Texture2D::GatherAlpha(S,float,int)
description: Restituisce i componenti alfa dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare. | Funzione Texture2D::GatherAlpha(S,float,int)
ms.assetid: 4c980e06-d768-479e-bee3-1b2541c23038
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
ms.openlocfilehash: 12ea7c643c8e86925163594856980c20aae09d61cd9421d6060449ed80da81f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789826"
---
# <a name="texture2dgatheralphasfloatint-function"></a>Funzione Texture2D::GatherAlpha(S,float,int)

Restituisce i componenti alfa dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare.

## <a name="syntax"></a>Sintassi

``` syntax
TemplateType GatherAlpha(
  in sampler s,
  in float2 location,
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

Tipo: **float2**

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

[Metodi GatherAlpha](texture2d-gatheralpha.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




