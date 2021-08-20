---
title: Funzione Texture2D::GatherRed(S,float,int)
description: Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto. | Funzione Texture2D::GatherRed(S,float,int)
ms.assetid: 6d2d1556-d52f-4625-93ca-34da399f9a8b
keywords:
- Funzione GatherRed HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 879ba1cdad400a065fae46bd858db5569390ae0ae2a2ad338bfb9faed62bbdca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508640"
---
# <a name="texture2dgatherredsfloatint-function"></a>Funzione Texture2D::GatherRed(S,float,int)

Per quattro valori texel che verrebbero usati in un'operazione di filtro bi lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.

## <a name="syntax"></a>Sintassi

``` syntax
TemplateType GatherRed(
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

[Metodi GatherRed](texture2d-gatherred.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




