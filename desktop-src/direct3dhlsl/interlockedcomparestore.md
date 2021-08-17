---
title: Funzione InterlockedCompareStore (informazioni di riferimento su HLSL)
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
ms.openlocfilehash: 7dbf13629b9c3b9b38cc3bd72a8a992ab40bd09c0333c155a7c109f71466f23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119245"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a>Funzione InterlockedCompareStore (informazioni di riferimento su HLSL)

Confronta in modo atomico la destinazione con il valore di confronto. Se sono identici, la destinazione viene sovrascritta con il valore di input.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*dest* \[ Pollici\]
</dt> <dd>

Tipo: **R**

Indirizzo di destinazione.

</dd> <dt>

*confrontare \_ il valore* \[ in\]
</dt> <dd>

Tipo: **T**

Valore di confronto.

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **T**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Confronta atomicamente il valore a cui fa riferimento *dest* con il valore *compare \_* e archivia *il* valore nella posizione a cui fa riferimento *dest* se i valori corrispondono. Questa operazione può essere eseguita solo su **risorse tipiche int** o **uint** e variabili di memoria condivisa. Questa funzione può essere utilizzata in due modi. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue l'operazione sul registro di memoria condivisa a cui fa riferimento *dest*. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento *dest*.

### <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modelli shader modello 5](d3d11-graphics-reference-sm5.md) e versioni successive | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|  x     | x    |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




