---
title: asuint (funzione)
description: Reinterpreta lo schema di bit di un valore a 64 bit come due interi senza segno a 32 bit.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- funzione asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045892"
---
# <a name="asuint-function"></a>asuint (funzione)

Reinterpreta lo schema di bit di un valore a 64 bit come due interi senza segno a 32 bit.

## <a name="syntax"></a>Sintassi

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: **Double**

Valore di input.

</dd> <dt>

*lowbits* \[ out\]
</dt> <dd>

Tipo: **uint**

Modello a 32 bit basso di *value*.

</dd> <dt>

*highbits* \[ out\]
</dt> <dd>

Tipo: **uint**

Modello a 32 bit elevato di *value*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione è una versione alternativa della funzione intrinseca [**asuint**](dx-graphics-hlsl-asuint.md) disponibile nei modelli shader precedenti ed è stata introdotta per il modello di shader 5. La funzione originale, riconosciuta nel compilatore HLSL con la firma diversa, rimane disponibile per il modello di shader 5.

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

[**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




