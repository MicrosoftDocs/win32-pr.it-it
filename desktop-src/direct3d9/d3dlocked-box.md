---
description: Descrive una casella bloccata (volume).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: D3DLOCKED_BOX struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: deb83c71eb9fe9fa5c69667e6dc48187144fa5c18e1daf084e4a04c1fd213744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750991"
---
# <a name="d3dlocked_box-structure"></a>Struttura D3DLOCKED \_ BOX

Descrive una casella bloccata (volume).

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a>Members

<dl> <dt>

**RowPitch**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset di byte dal bordo sinistro di una riga al bordo sinistro della riga successiva.

</dd> <dt>

**SlicePitch**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dei byte dall'alto a sinistra di una sezione all'angolo superiore sinistro della sezione più profonda successiva.

</dd> <dt>

**pBit**
</dt> <dd>

Tipo: **\* void**

</dd> <dd>

Puntatore all'inizio della casella del volume. Se alla chiamata LockBox è stato fornito un [**D3DBOX,**](d3dbox.md) i pBit verranno offset in modo appropriato dall'inizio del volume.

</dd> </dl>

## <a name="remarks"></a>Commenti

I volumi possono essere visualizzati come organizzati in sezioni di larghezza x altezza superfici 2D impilate per creare un volume larghezza x altezza x profondità. Per altre informazioni, vedere [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DVolume9::LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**IDirect3DVolumeTexture9::LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
