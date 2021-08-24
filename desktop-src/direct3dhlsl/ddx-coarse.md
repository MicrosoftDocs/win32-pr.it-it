---
title: ddx_coarse funzione
description: Calcola una derivata parziale a bassa precisione rispetto alla coordinata x dello spazio dello schermo.
ms.assetid: 5719f45d-b2ae-4916-8f31-c2797b661814
keywords:
- ddx_coarse funzione HLSL
topic_type:
- apiref
api_name:
- ddx_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d5521da56804156485fcacb37b43cbf27d8d4b3659cbced918eaea2c12b308ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855371"
---
# <a name="ddx_coarse-function"></a>Funzione grosso modo \_ ddx

Calcola una derivata parziale a bassa precisione rispetto alla coordinata x dello spazio dello schermo.

## <a name="syntax"></a>Sintassi

``` syntax
float ddx_coarse(
  in float value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **float**

Derivazione parziale a precisione bassa del *valore*.

## <a name="remarks"></a>Commenti

Sono disponibili anche le versioni di overload seguenti:

``` syntax
float2 ddx_coarse(float2 value);
float3 ddx_coarse(float3 value);
float4 ddx_coarse(float4 value);
```

### <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modelli shader modello 5](d3d11-graphics-reference-sm5.md) e versioni successive | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




