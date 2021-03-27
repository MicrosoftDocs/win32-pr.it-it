---
title: Funzione InterlockedMax (riferimento HLSL)
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
ms.openlocfilehash: 997641b086625532b99e3ae8d17be49cd71ae21f
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2020
ms.locfileid: "104398468"
---
# <a name="interlockedmax-function-hlsl-reference"></a>Funzione InterlockedMax (riferimento HLSL)

Esegue un massimo atomico garantito.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedMax(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*dest* \[ in\]
</dt> <dd>

Tipo: **R**

Indirizzo di destinazione.

</dd> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: **T**

Valore di input.

</dd> <dt>

*\_ valore originale* in \[ uscita\]
</dt> <dd>

Tipo: **T**

facoltativo. Valore di input originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione può essere eseguita solo su risorse tipizzate int e uint e variabili di memoria condivisa. Esistono due possibili usi per questa funzione. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue un numero massimo atomico del valore al registro di memoria condiviso a cui fa riferimento dest. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue un massimo atomico del valore nella posizione della risorsa a cui fa riferimento dest. La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest. Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




