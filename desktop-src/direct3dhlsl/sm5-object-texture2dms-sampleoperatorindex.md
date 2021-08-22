---
title: Texture2DMS::sample. Funzione operatore
description: Recupera un valore dalla risorsa nella posizione e nell'indice di esempio forniti. | Texture2DMS::sample. Funzione operatore
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- Esempio. Funzione operatore HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f5d7082ee72c49d3aa4be131491151b1bab65502e6fe85884b2a03573c497b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508473"
---
# <a name="texture2dmssampleoperator----function"></a>Texture2DMS::sample. Funzione operatore

Recupera un valore dalla risorsa nella posizione e nell'indice di esempio forniti.

## <a name="syntax"></a>Sintassi

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*sampleSlice* \[ Pollici\]
</dt> <dd>

Tipo: **uint**

Indice della sezione di esempio.

</dd> <dt>

*pos* \[ Pollici\]
</dt> <dd>

Tipo: **uint2**

Posizione dell'indice. I componenti contengono le coordinate (x, y).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di risorsa di sola lettura.

## <a name="remarks"></a>Commenti

### <a name="usage-example"></a>Esempio di utilizzo


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




