---
title: AsDouble (funzione)
description: Reinterpreta un valore cast (valori a 2 32 bit) in un valore Double.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- funzione AsDouble HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa2c83ee01739a2e2ee9595d0a26e1bdb80fef1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045893"
---
# <a name="asdouble-function"></a>AsDouble (funzione)

Reinterpreta un valore cast (valori a 2 32 bit) in un valore Double.

## <a name="syntax"></a>Sintassi

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*lowbits* \[ in\]
</dt> <dd>

Tipo: **uint**

Modello a 32 bit basso del valore di input.

</dd> <dt>

*highbits* \[ in\]
</dt> <dd>

Tipo: **uint**

Modello a 32 bit elevato del valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **Double**

L'input (valori a 2 32 bit) viene rieseguito come Double.

## <a name="remarks"></a>Commenti

È disponibile anche la versione di overload seguente:

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

Se il valore di input è costituito da componenti a 2 32 bit, il tipo restituito conterrà un valore Double. Se il valore di input è costituito da componenti a 4 32 bit, il tipo restituito conterrà due Double. Se il valore di input è un tipo a 64 bit, il valore restituito avrà lo stesso numero di componenti del valore di input.

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

 

 




