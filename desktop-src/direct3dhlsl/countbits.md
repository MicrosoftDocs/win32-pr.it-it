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
ms.openlocfilehash: 5f3816152b91fd03348e64c7a36dd41e8b620bd5e5ef8f4463538c44ef974485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793969"
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

 

 




