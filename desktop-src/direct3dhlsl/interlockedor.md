---
title: Funzione InterlockedOr (informazioni di riferimento su HLSL)
description: Esegue un'operazione atomica garantita o .
ms.assetid: ecbe6b2f-8eff-41d7-9ca3-4487c9ffeaf6
keywords:
- Funzione InterlockedOr HLSL
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c426237ec112a08fb7d422181a0efcd9ec0277d0628eda780492dae568ffaf38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854251"
---
# <a name="interlockedor-function-hlsl-reference"></a>Funzione InterlockedOr (informazioni di riferimento su HLSL)

Esegue un'operazione atomica garantita o .

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedOr(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*dest* \[ Pollici\]
</dt> <dd>

Tipo: **R**

Indirizzo di destinazione.

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **T**

Valore di input.

</dd> <dt>

*valore \_ originale* \[ out\]
</dt> <dd>

Tipo: **T**

facoltativo. Valore di input originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione può essere eseguita solo su risorse tipiche int o uint e variabili di memoria condivisa. Questa funzione può essere utilizzata in due modi. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue un'operazione atomica o di valore nel registro di memoria condivisa a cui fa riferimento dest. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue un'operazione atomica o di valore nel percorso della risorsa a cui fa riferimento dest. La funzione di overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest. Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modelli shader modello 5](d3d11-graphics-reference-sm5.md) e versioni successive | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




