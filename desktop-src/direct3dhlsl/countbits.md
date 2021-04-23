---
title: countbits (funzione)
description: Conta il numero di bit (per componente) impostati nell'intero di input.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- Funzione countbits HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 357aceca6e2aea261a9e94212b58ff6308c99560
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925624"
---
# <a name="countbits-function"></a>countbits (funzione)

Conta il numero di bit (per componente) impostati nell'intero di input.

## <a name="syntax"></a>Sintassi

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **uint**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint**

Numero di bit.

## <a name="remarks"></a>Commenti

Sono disponibili anche le versioni di overload seguenti:

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli di shader superiori | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




