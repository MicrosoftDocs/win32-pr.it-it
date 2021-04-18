---
description: Questi flag vengono utilizzati per controllare il modo in cui D3DX10ComputeNormalMap genera mappe normali. Qualsiasi numero di flag può essere o combinato in qualsiasi combinazione.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: Enumerazione D3DX10_NORMALMAP_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322954"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a>\_ \_ Enumerazione flag normalmap d3dx10

Questi flag vengono utilizzati per controllare il modo in cui [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) genera mappe normali. Qualsiasi numero di flag può essere o combinato in qualsiasi combinazione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10 \_ normalmap \_ mirror \_ U**
</dt> <dd>

Indica che i pixel al di fuori del bordo della trama sull'asse U devono essere rispecchiati, non a capo.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ normalmap \_ mirror \_ V**
</dt> <dd>

Indica che è necessario eseguire il mirroring dei pixel al di fuori del bordo della trama sull'asse V, senza eseguire il wrapping.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**\_Mirror normalmap \_ d3dx10**
</dt> <dd>

Uguale a D3DX10 \_ normalmap \_ mirror \_ U \| d3dx10 \_ normalmap \_ mirror \_ V.

</dd> <dt>

<span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ normalmap \_ INVERTSIGN**
</dt> <dd>

Inverte la direzione di ogni normale.

</dd> <dt>

<span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**\_ \_ Occlusione di calcolo normalmap d3dx10 \_**
</dt> <dd>

Calcola il termine di occlusione per pixel e lo codifica in alfa. Un valore alfa pari a 1 indica che il pixel non è nascosto in alcun modo, mentre un valore alfa pari a 0 indica che il pixel è completamente nascosto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




