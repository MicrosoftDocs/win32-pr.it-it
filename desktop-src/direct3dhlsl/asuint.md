---
title: Funzione asuint
description: Reinterpreta il modello di bit di un valore a 64 bit come due interi senza segno a 32 bit.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- Funzione asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02f0df4d31ca978b8b58b50cd0c91710056aa9ac0f3cac1ae370a4edba6a9edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626591"
---
# <a name="asuint-function"></a>Funzione asuint

Reinterpreta il modello di bit di un valore a 64 bit come due interi senza segno a 32 bit.

## <a name="syntax"></a>Sintassi

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **double**

Valore di input.

</dd> <dt>

*lowbit* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Modello a 32 bit basso del *valore*.

</dd> <dt>

*highbits* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Modello a 32 bit alto del *valore*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione è una versione alternativa della [**funzione intrinseca asuint**](dx-graphics-hlsl-asuint.md) disponibile nei modelli shader precedenti ed è stata introdotta per Shader Model 5. La funzione originale (riconosciuta nel compilatore HLSL dalla firma diversa) rimane disponibile per Shader Model 5.

### <a name="minimum-shader-model"></a>Modello shader minimo

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

[**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




