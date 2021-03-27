---
title: funzione ddx_fine
description: Calcola una derivata parziale a precisione elevata rispetto alla coordinata x dello spazio dello schermo. | funzione ddx_fine
ms.assetid: 41062d6f-2b7f-4594-a6de-da37ded5d444
keywords:
- funzione ddx_fine HLSL
topic_type:
- apiref
api_name:
- ddx_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c1a579ba5899cf4d3ac3f25ef5a40337f6291977
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982082"
---
# <a name="ddx_fine-function"></a>\_funzione DDX fine

Calcola una derivata parziale a precisione elevata rispetto alla coordinata x dello spazio dello schermo.

## <a name="syntax"></a>Sintassi

``` syntax
float ddx_fine(
  in float value
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

Derivato parziale di precisione elevata del *valore*.

## <a name="remarks"></a>Commenti

Sono disponibili anche le seguenti versioni di overload:

``` syntax
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
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

 

 




