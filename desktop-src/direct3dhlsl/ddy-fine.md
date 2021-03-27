---
title: funzione ddy_fine
description: Calcola una derivata parziale a precisione elevata rispetto alla coordinata x dello spazio dello schermo. | funzione ddy_fine
ms.assetid: 29fcdbc9-470b-4b5b-b18c-f75dd2c87920
keywords:
- funzione ddy_fine HLSL
topic_type:
- apiref
api_name:
- ddy_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a4cb297180a4988cb049ccebfa4f82571c4655c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995774"
---
# <a name="ddy_fine-function"></a>\_funzione ddy fine

Calcola una derivata parziale a precisione elevata rispetto alla coordinata x dello spazio dello schermo.

## <a name="syntax"></a>Sintassi

``` syntax
float ddy_fine(
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
float2 ddy_fine(float2 value);
float3 ddy_fine(float3 value);
float4 ddy_fine(float4 value);  
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

 

 




