---
title: Enumerazione D3DX11_NORMALMAP_FLAG (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Opzioni di mappa normali. È possibile combinare un numero qualsiasi di questi flag usando un'operazione OR bit per bit.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- Enumerazione D3DX11_NORMALMAP_FLAG Direct3D 11
- Puntatore di enumerazione LPD3DX11_NORMALMAP_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235204"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>\_ \_ Enumerazione flag normalmap D3DX11

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Opzioni di mappa normali. È possibile combinare un numero qualsiasi di questi flag usando un'operazione OR bit per bit.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ normalmap \_ mirror \_ U**
</dt> <dd>

Indica che i pixel al di fuori del bordo della trama sull'asse U devono essere rispecchiati, non a capo.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ normalmap \_ mirror \_ V**
</dt> <dd>

Indica che è necessario eseguire il mirroring dei pixel al di fuori del bordo della trama sull'asse V, senza eseguire il wrapping.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**\_Mirror normalmap \_ D3DX11**
</dt> <dd>

Uguale a D3DX11 \_ normalmap \_ mirror \_ U \| D3DX11 \_ normalmap \_ mirror \_ V.

</dd> <dt>

<span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ normalmap \_ INVERTSIGN**
</dt> <dd>

Inverte la direzione di ogni normale.

</dd> <dt>

<span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**\_ \_ Occlusione di calcolo normalmap D3DX11 \_**
</dt> <dd>

Calcola il termine di occlusione per pixel e lo codifica in alfa. Un valore alfa pari a 1 indica che il pixel non è nascosto in alcun modo, mentre un valore alfa pari a 0 indica che il pixel è completamente nascosto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi flag vengono usati da [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





