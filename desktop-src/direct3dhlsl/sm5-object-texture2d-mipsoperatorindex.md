---
title: Texture2D::mips. Funzione operatore
description: Restituisce una variabile di risorsa di sola lettura. | Texture2D::mips. Funzione operatore
ms.assetid: 201996a7-741f-4457-ab77-9cd653f3682b
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
ms.openlocfilehash: 0d8c915c340e69eedc8b66a1665b6e600c0134b66cb6cd81fe6b803681e5fdeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789497"
---
# <a name="texture2dmipsoperator----function"></a>Texture2D::mips. Funzione operatore

Restituisce una variabile di risorsa di sola lettura.

## <a name="syntax"></a>Sintassi

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
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

Tipo: **uint2**

Posizione dell'indice. Contiene le coordinate (x, y).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di risorsa di sola lettura.

## <a name="remarks"></a>Commenti

### <a name="usage-example"></a>Esempio di utilizzo


```
Texture2D<float4> tex;
uint mip = 2;
uint2 pos_xy = {123, 456};
float4 f = tex.mips[mip][pos_xy];
        
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




