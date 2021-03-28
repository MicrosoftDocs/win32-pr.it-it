---
title: 'Texture2DMS:: Sample. Funzione operator'
description: "Recupera un valore dalla risorsa nella posizione e nell'indice di esempio forniti. | Texture2DMS:: Sample. Funzione operator"
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- esempio. Funzione operator HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234885"
---
# <a name="texture2dmssampleoperator----function"></a>Texture2DMS:: Sample. Funzione operator

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

*sampleSlice* \[ in\]
</dt> <dd>

Tipo: **uint**

Indice della sezione di esempio.

</dd> <dt>

*pos* \[ in\]
</dt> <dd>

Tipo: **uint2**

Posizione dell'indice. I componenti contengono le coordinate (x, y).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di sola lettura di una risorsa.

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



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




