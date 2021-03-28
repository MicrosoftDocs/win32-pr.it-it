---
title: Funzione InterlockedCompareStore (riferimento HLSL)
description: Confronta in modo atomico la destinazione con il valore di confronto. Se sono identici, la destinazione viene sovrascritta con il valore di input.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- Funzione InterlockedCompareStore HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2020
ms.locfileid: "104398469"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a>Funzione InterlockedCompareStore (riferimento HLSL)

Confronta in modo atomico la destinazione con il valore di confronto. Se sono identici, la destinazione viene sovrascritta con il valore di input.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*dest* \[ in\]
</dt> <dd>

Tipo: **R**

Indirizzo di destinazione.

</dd> <dt>

*Confronta \_ valore* \[ in\]
</dt> <dd>

Tipo: **T**

Valore di confronto.

</dd> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: **T**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Confronta in modo atomico il valore a cui fa riferimento *dest* con *\_ valore di confronto* e archivia il *valore* nella posizione a cui fa riferimento *dest* se i valori corrispondono. Questa operazione può essere eseguita solo su risorse tipizzate **int** o **uint** e variabili di memoria condivisa. Esistono due possibili usi per questa funzione. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue l'operazione sul Registro di memoria condiviso a cui fa riferimento *dest*. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento *dest*.

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|  x     | x    |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




