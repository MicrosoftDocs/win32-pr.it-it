---
description: Definisce le impostazioni usate per i calcoli dei fotogrammi tangenti della mesh.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Enumerazione D3DXTANGENT (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 5d6e57d2027a7366ec2b82ac7bd82aae4275d489c17f1922684e3ca6232be940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749771"
---
# <a name="d3dxtangent-enumeration"></a>Enumerazione D3DXTANGENT

Definisce le impostazioni usate per i calcoli dei fotogrammi tangenti della mesh.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ WRAP \_ U**
</dt> <dd>

I valori delle coordinate della trama nella direzione u sono compresi tra 0 e 1. In questo caso verrà scelto un set di coordinate di trama che riduce al minimo il perimetro del triangolo. Vedere [Disposizione delle trame (Direct3D 9).](texture-wrapping.md)

</dd> <dt>

<span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ WRAP \_ V**
</dt> <dd>

I valori delle coordinate della trama nella direzione v sono compresi tra 0 e 1. In questo caso verrà scelto un set di coordinate di trama che riduce al minimo il perimetro del triangolo. Vedere [Disposizione delle trame (Direct3D 9).](texture-wrapping.md)

</dd> <dt>

<span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ WRAP \_ UV**
</dt> <dd>

I valori delle coordinate della trama in entrambe le direzioni sono compresi tra 0 e 1. In questo caso verrà scelto un set di coordinate di trama che riduce al minimo il perimetro del triangolo. Vedere [Disposizione delle trame (Direct3D 9).](texture-wrapping.md)

</dd> <dt>

<span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ NON \_ NORMALIZZA \_ PARZIALI**
</dt> <dd>

Non normalizzare i derivati parziali rispetto alle coordinate della trama. Se non normalizzato, la scala dei derivati parziali è proporzionale alla scala del modello 3D divisa per la scala del triangolo nello spazio (u, v). Questo valore di scala fornisce una misura della quantità di estensione della trama in una determinata direzione. La lunghezza del vettore risultante è una somma ponderata delle lunghezze dei derivati parziali.

</dd> <dt>

<span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ DONT \_ ORTHOGONALIZE**
</dt> <dd>

Non trasformare le coordinate della trama in coordinate cartesiane ortogonali. Si escludono a vicenda con D3DXTANGENT \_ ORTHOGONALIZE FROM you e \_ \_ D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ V.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ V**
</dt> <dd>

Calcolare la derivata parziale rispetto alla coordinata di trama v in modo indipendente per ogni vertice e quindi calcolare la derivata parziale rispetto all'utente come prodotto incrociato della derivata parziale rispetto a v e al vettore normale. Si escludono a vicenda con D3DXTANGENT \_ DONT \_ ORTHOGONALIZE e D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U**
</dt> <dd>

Calcolare la derivata parziale rispetto alla coordinata di trama u in modo indipendente per ogni vertice e quindi calcolare la derivata parziale rispetto a v come prodotto incrociato del vettore normale e della derivata parziale rispetto all'utente. Si escludono a vicenda con D3DXTANGENT \_ DONT \_ ORTHOGONALIZE e D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ V.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**PESO D3DXTANGENT \_ \_ PER \_ AREA**
</dt> <dd>

Ponderare la direzione del vettore derivato normale o parziale calcolato per vertice in base alle aree dei triangoli collegati a tale vertice. Si escludono a vicenda con D3DXTANGENT \_ WEIGHT \_ EQUAL.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**PESO D3DXTANGENT \_ \_ UGUALE**
</dt> <dd>

Calcolare un vettore normale di lunghezza unità per ogni triangolo della mesh di input. Si escludono a vicenda con D3DXTANGENT \_ WEIGHT \_ BY \_ AREA.

</dd> <dt>

<span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ WIND \_ CW**
</dt> <dd>

I vertici vengono ordinati in senso orario intorno a ogni triangolo. La direzione del vettore normale calcolata viene quindi invertita di 180 gradi rispetto alla direzione calcolata usando l'ordinamento dei vertici in senso antiorario.

</dd> <dt>

<span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ CALCULATE \_ NORMALS**
</dt> <dd>

Calcolare il vettore normale per vertice per ogni triangolo della mesh di input e ignorare tutti i vettori normali già presenti nella mesh di input.

</dd> <dt>

<span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**GENERAZIONE D3DXTANGENT \_ \_ SUL \_ POSTO**
</dt> <dd>

I risultati vengono archiviati nella mesh di input originale e la mesh di output non viene usata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




