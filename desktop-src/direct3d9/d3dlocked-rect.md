---
description: Descrive un'area rettangolare bloccata.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: D3DLOCKED_RECT struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b419483329e5461de5bc98b3a37b556e37138a055932b1d6c80d3a19b13ae516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988901"
---
# <a name="d3dlocked_rect-structure"></a>Struttura D3DLOCKED \_ RECT

Descrive un'area rettangolare bloccata.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a>Members

<dl> <dt>

**Passo**
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di byte in una riga della superficie.

</dd> <dt>

**pBits**
</dt> <dd>

Tipo: **\* void**

</dd> <dd>

Puntatore ai bit bloccati. Se è [**stato fornito**](/previous-versions//dd162897(v=vs.85)) un rect alla [**chiamata LockRect,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) i pBit verranno offset in modo appropriato dall'inizio della superficie.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il passo per i formati DXTn è diverso da quello restituito in DirectX 7. Ora fa riferimento al numero di byte in una riga di blocchi. Ad esempio, se si ha una larghezza di 16, si avrà un passo di 4 blocchi (4 8 per \* DXT1, 4 \* 16 per DXT2-5).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DSurface9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
