---
title: Funzione InterlockedExchange (informazioni di riferimento su HLSL)
description: Assegna value a dest e restituisce il valore originale.
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- HLSL della funzione InterlockedExchange
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3880a85af5658d0d50eb079c2dd1fc300e6a4de4b7f606688ab9d7a317cf321c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511321"
---
# <a name="interlockedexchange-function-hlsl-reference"></a>Funzione InterlockedExchange (informazioni di riferimento su HLSL)

Assegna value a dest e restituisce il valore originale.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedExchange(
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

Valore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione può essere eseguita solo su risorse di tipo scalare e variabili di memoria condivisa. Questa funzione può essere utilizzata in due modi. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue l'operazione sul registro di memoria condivisa a cui fa riferimento dest. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento dest. Questa operazione è disponibile solo quando R è leggibile e scrivibile.

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli shader superiori | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      |  x   | x      |  x       | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




