---
title: countbits (funzione)
description: Conta il numero di bit (per componente) nell'intero di input.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- funzione countbits HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d3cd63502c6217e6fb0b0ff17685b2d2b5bf25
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045876"
---
# <a name="countbits-function"></a>countbits (funzione)

Conta il numero di bit (per componente) nell'intero di input.

## <a name="syntax"></a>Sintassi

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: **uint**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint**

Numero di bit.

## <a name="remarks"></a>Commenti

Sono disponibili anche le seguenti versioni di overload:

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




