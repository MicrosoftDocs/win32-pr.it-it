---
title: 'Funzione Texture2D:: GatherAlpha (S, float, int)'
description: "Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare. | Funzione Texture2D:: GatherAlpha (S, float, int)"
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
ms.openlocfilehash: 36561e6bc16a84e0a377292ededf58df3c15f800
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981815"
---
# <a name="texture2dgatheralphasfloatint-function"></a>Funzione Texture2D:: GatherAlpha (S, float, int)

Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare.

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

Tipo: **Sampler**

Indice del campionatore in base zero.

</dd> <dt>

*posizione* \[ in\]
</dt> <dd>

Tipo: **float2**

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

[Metodi GatherAlpha](texture2d-gatheralpha.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




