---
title: firstbithigh (funzione)
description: Ottiene la posizione del primo bit impostato a partire dal bit di ordine più alto e lavorando verso il basso, per componente.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- Funzione firstbithigh HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c62b6f090126887930415fc408da4f4a6c17bc4a99429db61fd298960c07e6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949701"
---
# <a name="firstbithigh-function"></a>firstbithigh (funzione)

Ottiene la posizione del primo bit impostato a partire dal bit di ordine più alto e lavorando verso il basso, per componente.

## <a name="syntax"></a>Sintassi

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Posizione del primo bit impostato.

## <a name="remarks"></a>Commenti

Per un intero con segno, il primo bit significativo è zero per un numero negativo.

Sono disponibili anche le versioni di overload seguenti:

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

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

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 