---
title: Funzione asdouble
description: Reinterpreta un valore cast (due valori a 32 bit) in un valore double.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- Funzione asdouble HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e191a2bf9ee7fb46337c3c7dfef7f8dea3525acf936ab745c07e7720f1ac509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626641"
---
# <a name="asdouble-function"></a>Funzione asdouble

Reinterpreta un valore cast (due valori a 32 bit) in un valore double.

## <a name="syntax"></a>Sintassi

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*lowbit* \[ Pollici\]
</dt> <dd>

Tipo: **uint**

Modello a 32 bit basso del valore di input.

</dd> <dt>

*highbits* \[ Pollici\]
</dt> <dd>

Tipo: **uint**

Modello a 32 bit elevato del valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **double**

L'input (due valori a 32 bit) viene ricastato come valore double.

## <a name="remarks"></a>Commenti

È disponibile anche la versione di overload seguente:

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

Se il valore di input è due componenti a 32 bit, il tipo restituito conterrà un valore double. Se il valore di input è quattro componenti a 32 bit, il tipo restituito conterrà due valori double. Se il valore di input è di tipo a 64 bit, il valore restituito avrà lo stesso numero di componenti del valore di input.

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modelli shader modello 5](d3d11-graphics-reference-sm5.md) e versioni successive | sì       |



 

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

 

 




