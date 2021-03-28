---
title: Funzione InterlockedCompareExchange (riferimento HLSL)
description: Confronta in modo atomico la destinazione con il valore di confronto. Se sono identici, la destinazione viene sovrascritta con il valore di input. Il valore originale è impostato sul valore originale della destinazione.
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
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2020
ms.locfileid: "104993317"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a>Funzione InterlockedCompareExchange (riferimento HLSL)

Confronta in modo atomico la destinazione con il valore di confronto. Se sono identici, la destinazione viene sovrascritta con il valore di input. Il valore originale è impostato sul valore originale della destinazione.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
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

*Confronta \_ valore* \[ in\]
</dt> <dd>

Tipo: **T**

Valore di confronto.

</dd> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: **T**

Valore di input.

</dd> <dt>

*\_ valore originale* in \[ uscita\]
</dt> <dd>

Tipo: **T**

Valore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Confronta in modo atomico il valore a cui fa *riferimento dest* con *\_ valore di confronto*, archivia il *valore* nella posizione a cui fa riferimento *dest* se i valori corrispondono, restituisce il valore originale di *dest* nel *\_ valore originale*. Questa operazione può essere eseguita solo su risorse tipizzate **int** o **uint** e variabili di memoria condivisa. Esistono due possibili usi per questa funzione. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue l'operazione sul Registro di memoria condiviso a cui fa riferimento *dest*. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento *dest*. Questa operazione è disponibile solo se R è leggibile e scrivibile.

> [!Note]  
> Se si chiama **InterlockedCompareExchange** in un ciclo [**for**](dx-graphics-hlsl-for.md) o [**while**](dx-graphics-hlsl-while.md) compute shader, per la corretta compilazione è necessario usare l'attributo **\[ allow \_ \_ Condition \] UAV** in quel ciclo.

 

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

 

 




