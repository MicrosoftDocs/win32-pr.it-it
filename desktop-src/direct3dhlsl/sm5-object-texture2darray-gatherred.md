---
title: 'Funzione Texture2DArray:: GatherRed (S, float, int)'
description: "Restituisce i componenti rossi dei quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare. | Funzione Texture2DArray:: GatherRed (S, float, int)"
ms.assetid: cb9c21ef-87f4-4c32-b41a-9fc7478713a6
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
ms.openlocfilehash: 431d08b77d13540bb48621a6d5ec76f4c775f796
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995549"
---
# <a name="texture2darraygatherredsfloatint-function"></a>Funzione Texture2DArray:: GatherRed (S, float, int)

Restituisce i componenti rossi dei quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.

## <a name="syntax"></a>Sintassi

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **Sampler**

Indice del campionatore in base zero.

</dd> <dt>

*posizione* \[ in\]
</dt> <dd>

Tipo: **float3**

Coordinate di esempio (u, v).

</dd> <dt>

*offset* \[ in\]
</dt> <dd>

Tipo: **int2**

Offset applicato alla coordinata di trama prima del campionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **TemplateType**

Valore a quattro componenti il cui tipo corrisponde al tipo di modello.

## <a name="remarks"></a>Commenti

Gli esempi di trama possono essere usati per l'interpolazione bilineare.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi GatherRed](texture2darray-gatherred.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




