---
title: Texture2DMSArray::sample. Funzione operatore
description: Restituisce una variabile di risorsa di sola lettura. | Texture2DMSArray::sample. Funzione operatore
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: 09ac18e7830dfe6b18718deed56e8495ba476dcedcb8290eab4e16aa0d7f24fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508326"
---
# <a name="texture2dmsarraysampleoperator----function"></a>Texture2DMSArray::sample. Funzione operatore

Restituisce una variabile di risorsa di sola lettura.

## <a name="syntax"></a>Sintassi

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
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

Tipo: **uint3**

Posizione dell'indice. Il primo e il secondo componente contengono le coordinate (x, y). Il terzo componente indica la sezione di matrice desiderata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di risorsa di sola lettura.

## <a name="remarks"></a>Commenti

### <a name="usage-example"></a>Esempio di utilizzo


```
Texture2DMSArray<float4, 4> alpha;

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

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




