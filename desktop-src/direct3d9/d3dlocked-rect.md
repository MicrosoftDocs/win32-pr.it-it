---
description: Descrive un'area rettangolare bloccata.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: Struttura D3DLOCKED_RECT (D3D9Types. h)
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
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530955"
---
# <a name="d3dlocked_rect-structure"></a>\_Struttura Rect D3DLOCKED

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

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di byte in una riga della superficie.

</dd> <dt>

**pBits**
</dt> <dd>

Tipo: **void \***

</dd> <dd>

Puntatore ai bit bloccati. Se è stato fornito un oggetto [**Rect**](/previous-versions//dd162897(v=vs.85)) alla chiamata [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , pBits verrà spostato in modo appropriato dall'inizio della superficie.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il pitch per i formati DXTn è diverso da quello restituito in DirectX 7. Fa ora riferimento al numero di byte in una riga di blocchi. Se, ad esempio, si dispone di una larghezza di 16, sarà presente un pitch di 4 blocchi (4 \* 8 per DXT1, 4 \* 16 per DXT2-5).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DSurface9:: LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
