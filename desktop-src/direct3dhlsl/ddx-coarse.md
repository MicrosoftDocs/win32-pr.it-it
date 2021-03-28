---
title: funzione ddx_coarse
description: Calcola una derivata parziale con precisione bassa rispetto alla coordinata x dello spazio dello schermo.
ms.assetid: 5719f45d-b2ae-4916-8f31-c2797b661814
keywords:
- funzione ddx_coarse HLSL
topic_type:
- apiref
api_name:
- ddx_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f9d4805a1d516a5d8980fcd8209fd6733fe86c4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045875"
---
# <a name="ddx_coarse-function"></a>\_funzione grossolana DDX

Calcola una derivata parziale con precisione bassa rispetto alla coordinata x dello spazio dello schermo.

## <a name="syntax"></a>Sintassi

``` syntax
float ddx_coarse(
  in float value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: **float**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **float**

Derivato parziale di precisione bassa del *valore*.

## <a name="remarks"></a>Commenti

Sono disponibili anche le seguenti versioni di overload:

``` syntax
float2 ddx_coarse(float2 value);
float3 ddx_coarse(float3 value);
float4 ddx_coarse(float4 value);
```

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




