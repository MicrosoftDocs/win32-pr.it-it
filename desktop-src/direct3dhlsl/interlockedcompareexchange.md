---
title: Funzione InterlockedCompareExchange (informazioni di riferimento su HLSL)
description: Confronta in modo atomico la destinazione con il valore di confronto. Se sono identici, la destinazione viene sovrascritta con il valore di input. Il valore originale viene impostato sul valore originale della destinazione.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- Funzione InterlockedCompareExchange HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46cf8c3fb0e3bc0b21c5bf8bc3d946851ce213b765731518d252495250071228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119255"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a>Funzione InterlockedCompareExchange (informazioni di riferimento su HLSL)

Confronta in modo atomico la destinazione con il valore di confronto. Se sono identici, la destinazione viene sovrascritta con il valore di input. Il valore originale viene impostato sul valore originale della destinazione.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
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

*confrontare \_ il valore* \[ in\]
</dt> <dd>

Tipo: **T**

Valore di confronto.

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **T**

Valore di input.

</dd> <dt>

*valore \_ originale* \[ out\]
</dt> <dd>

Tipo: **T**

Valore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Confronta atomicamente il valore a cui fa  riferimento *dest* con il valore *compare \_*, archivia il valore nella posizione a cui fa riferimento *dest* se i valori corrispondono, restituisce il valore originale *di dest* nel *valore \_ originale.* Questa operazione può essere eseguita solo su **risorse tipiche int** o **uint** e variabili di memoria condivisa. Questa funzione può essere utilizzata in due modi. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue l'operazione sul registro di memoria condivisa a cui fa riferimento *dest*. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento *dest*. Questa operazione è disponibile solo quando R è leggibile e scrivibile.

> [!Note]  
> Se si chiama **InterlockedCompareExchange** in un ciclo [**for**](dx-graphics-hlsl-for.md) o [**while**](dx-graphics-hlsl-while.md) compute shader, per compilare correttamente, è necessario usare l'attributo **\[ allow \_ uav \_ condition \]** in tale ciclo.

 

### <a name="minimum-shader-model"></a>Modello shader minimo

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

 

 




