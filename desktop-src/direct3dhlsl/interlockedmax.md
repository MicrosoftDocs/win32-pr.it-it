---
title: Funzione InterlockedMax (informazioni di riferimento su HLSL)
description: Esegue un massimo atomico garantito.
ms.assetid: ea2c67ef-3133-424d-9cc3-81da79aee87e
keywords:
- Funzione InterlockedMax HLSL
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 48b38baead9acbd12fc0b04205565b2968bdb9196e7ce0ca0b14c8bc7a48a770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982081"
---
# <a name="interlockedmax-function-hlsl-reference"></a>Funzione InterlockedMax (informazioni di riferimento su HLSL)

Esegue un massimo atomico garantito.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedMax(
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

Questa operazione può essere eseguita solo su risorse tipiche int e uint e variabili di memoria condivisa. Questa funzione può essere utilizzata in due modi. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue un numero massimo atomico di valore nel registro di memoria condivisa a cui fa riferimento dest. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue un massimo atomico di valore per il percorso della risorsa a cui fa riferimento dest. La funzione di overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest. Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli shader superiori | sì       |



 

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

 

 




