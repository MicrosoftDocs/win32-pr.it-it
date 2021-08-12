---
title: D3DX11_NORMALMAP_FLAG enumerazione (D3DX11tex.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Opzioni mappa normali. È possibile combinare qualsiasi numero di questi flag usando un'operazione OR bit per bit.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- D3DX11_NORMALMAP_FLAG enumerazione Direct3D 11
- LPD3DX11_NORMALMAP_FLAG puntatore di enumerazione Direct3D 11
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
ms.openlocfilehash: dbea7c787ac2e2aa7d988e052e2ca548a49a338c9b9f981ce73d51c40e0b4edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300650"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>Enumerazione D3DX11 \_ NORMALMAP \_ FLAG

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Opzioni mappa normali. È possibile combinare qualsiasi numero di questi flag usando un'operazione OR bit per bit.

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

<span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ NORMALMAP \_ MIRROR \_ U**
</dt> <dd>

Indica che i pixel all'esterno del bordo della trama sull'asse U devono essere rispecchiati, senza ritorno a capo.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ NORMALMAP \_ MIRROR \_ V**
</dt> <dd>

Indica che i pixel al di fuori del bordo della trama sull'asse V devono essere rispecchiati, senza ritorno a capo.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11 \_ NORMALMAP \_ MIRROR**
</dt> <dd>

Uguale a D3DX11 \_ NORMALMAP \_ MIRROR U \_ \| D3DX11 \_ NORMALMAP MIRROR \_ \_ V.

</dd> <dt>

<span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ NORMALMAP \_ INVERTSIGN**
</dt> <dd>

Inverte la direzione di ogni normale.

</dd> <dt>

<span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**OCCLUSIONE DI CALCOLO D3DX11 \_ NORMALMAP \_ \_**
</dt> <dd>

Calcola il termine di occlusione per pixel e lo codifica in alfa. Un valore alfa di 1 indica che il pixel non viene nascosto in alcun modo e un valore alfa 0 indica che il pixel è completamente nascosto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi flag vengono usati da [**D3DX11ComputeNormalMap.**](d3dx11computenormalmap.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





