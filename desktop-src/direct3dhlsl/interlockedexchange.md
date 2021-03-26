---
title: Funzione InterlockedExchange (riferimento HLSL)
description: Assegna il valore a dest e restituisce il valore originale.
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- Funzione InterlockedExchange HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c39dc4f68429fa3f070d446f998fd528a99af01
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2020
ms.locfileid: "104976583"
---
# <a name="interlockedexchange-function-hlsl-reference"></a>Funzione InterlockedExchange (riferimento HLSL)

Assegna il valore a dest e restituisce il valore originale.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedExchange(
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

Valore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione può essere eseguita solo su risorse con tipizzazione scalare e variabili di memoria condivisa. Esistono due possibili usi per questa funzione. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue l'operazione sul Registro di memoria condiviso a cui fa riferimento dest. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento dest. Questa operazione è disponibile solo se R è leggibile e scrivibile.

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      |  x   | x      |  x       | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




