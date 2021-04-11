---
description: Descrive una casella bloccata (volume).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: Struttura D3DLOCKED_BOX (D3D9Types. h)
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
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235072"
---
# <a name="d3dlocked_box-structure"></a>\_Struttura D3DLOCKED box

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

Offset dei byte dal bordo sinistro di una riga al bordo sinistro della riga successiva.

</dd> <dt>

**SlicePitch**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset di byte dalla parte superiore sinistra di una sezione alla parte superiore sinistra della sezione più profonda successiva.

</dd> <dt>

**pBits**
</dt> <dd>

Tipo: **void \***

</dd> <dd>

Puntatore all'inizio della casella del volume. Se è stato specificato un [**D3DBOX**](d3dbox.md) per la chiamata all'archivio protetto, pBits verrà spostato in modo appropriato dall'inizio del volume.

</dd> </dl>

## <a name="remarks"></a>Commenti

I volumi possono essere visualizzati come organizzati in sezioni di larghezza x superfici 2D di altezza in pila per ottenere una larghezza x altezza x volume profondità. Per altre informazioni, vedere [risorse di trama del volume (Direct3D 9)](volume-texture-resources.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DVolume9:: archivio protetto**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**IDirect3DVolumeTexture9:: archivio protetto**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
