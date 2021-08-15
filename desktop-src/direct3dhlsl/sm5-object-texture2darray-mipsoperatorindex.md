---
title: Texture2DArray::mips. Funzione operatore
description: Restituisce una variabile di risorsa di sola lettura. | Texture2DArray::mips. Funzione operatore
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
keywords:
- Mips. Funzione operatore HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5dff48f721e45ef7853c125b1d7d0d32d5cb311a3dbc3b31d4100f3038a8fdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724592"
---
# <a name="texture2darraymipsoperator----function"></a>Texture2DArray::mips. Funzione operatore

Restituisce una variabile di risorsa di sola lettura.

## <a name="syntax"></a>Sintassi

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*mipSlice* \[ Pollici\]
</dt> <dd>

Tipo: **uint**

Indice della sezione mip.

</dd> <dt>

*pos* \[ Pollici\]
</dt> <dd>

Tipo: **uint3**

Posizione dell'indice. Il primo e il secondo componente contengono le coordinate (x, y). Il terzo componente indica la sezione di matrice desiderata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di risorsa di sola lettura.

## <a name="remarks"></a>Commenti

### <a name="usage-example"></a>Esempio di utilizzo


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




