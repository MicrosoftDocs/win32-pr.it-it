---
description: Definisce le impostazioni utilizzate per i calcoli del frame tangente della mesh.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Enumerazione D3DXTANGENT (D3dx9mesh. h)
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
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322580"
---
# <a name="d3dxtangent-enumeration"></a>Enumerazione D3DXTANGENT

Definisce le impostazioni utilizzate per i calcoli del frame tangente della mesh.

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

<span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT a \_ capo automatico \_ U**
</dt> <dd>

I valori delle coordinate di trama nella direzione u sono compresi tra 0 e 1. In questo caso verrà scelto un set di coordinate di trama che riduce al minimo il perimetro del triangolo. Vedere [wrapping della trama (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ Wrap \_ V**
</dt> <dd>

I valori delle coordinate di trama nella direzione v sono compresi tra 0 e 1. In questo caso verrà scelto un set di coordinate di trama che riduce al minimo il perimetro del triangolo. Vedere [wrapping della trama (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT a \_ capo \_ UV**
</dt> <dd>

I valori delle coordinate di trama nelle direzioni u e v sono compresi tra 0 e 1. In questo caso verrà scelto un set di coordinate di trama che riduce al minimo il perimetro del triangolo. Vedere [wrapping della trama (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ dont \_ normalizzare i \_ parziali**
</dt> <dd>

Non normalizzare le derivazioni parziali rispetto alle coordinate di trama. Se non normalizzato, la scala dei derivati parziali è proporzionale alla scala del modello 3D divisa per la scala del triangolo nello spazio (u, v). Questo valore di scala fornisce una misura del grado di estensione della trama in una determinata direzione. La lunghezza del vettore risultante è una somma ponderata delle lunghezze dei derivati parziali.

</dd> <dt>

<span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ dont \_ ORTHOGONALIZE**
</dt> <dd>

Non trasformare le coordinate di trama in coordinate cartesiane ortogonali. Si escludono a vicenda con D3DXTANGENT \_ ORTHOGONALIZE \_ \_ e D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ V.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**\_ORTHOGONALIZE D3DXTANGENT \_ da \_ V**
</dt> <dd>

Calcolare la derivata parziale per quanto concerne la coordinata di trama v in modo indipendente per ogni vertice, quindi calcolare la derivata parziale per quanto riguarda il prodotto incrociato del derivato parziale rispetto a v e il vettore normale. Si escludono a vicenda con D3DXTANGENT \_ dont \_ ORTHOGONALIZE e D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ U.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**\_ORTHOGONALIZE D3DXTANGENT \_ da \_ U**
</dt> <dd>

Calcolare la derivata parziale per quanto concerne la coordinata di trama u in modo indipendente per ogni vertice, quindi calcolare la derivata parziale rispetto a v come prodotto incrociato del vettore normale e la derivata parziale rispetto all'utente. Si escludono a vicenda con D3DXTANGENT \_ dont \_ ORTHOGONALIZE e D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ V.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT \_ ponderato \_ per \_ area**
</dt> <dd>

Ponderare la direzione del vettore calcolato per vertice normale o parziale derivato in base alle aree dei triangoli collegati al vertice. Si escludono a vicenda con D3DXTANGENT \_ Weight \_ uguale a.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT \_ peso \_ uguale**
</dt> <dd>

Calcola un vettore normale a lunghezza di unità per ogni triangolo della mesh di input. Si escludono a vicenda con D3DXTANGENT \_ Weight \_ by \_ area.

</dd> <dt>

<span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ vento \_ CW**
</dt> <dd>

I vertici vengono ordinati in senso orario intorno a ogni triangolo. La direzione del vettore normale calcolata è quindi invertita di 180 gradi dalla direzione calcolata utilizzando l'ordine dei vertici in senso antiorario.

</dd> <dt>

<span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ Calcola \_ normali**
</dt> <dd>

Calcolare il vettore normale per vertice per ogni triangolo della mesh di input e ignorare i vettori normali già presenti nella mesh di input.

</dd> <dt>

<span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ genera \_ sul \_ posto**
</dt> <dd>

I risultati vengono archiviati nella mesh di input originale e la mesh di output non viene utilizzata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




